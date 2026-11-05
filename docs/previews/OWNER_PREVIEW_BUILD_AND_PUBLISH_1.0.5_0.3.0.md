# Owner release and recovery guide — Desktop 1.0.5 / GIS Hosts and Python SDK 0.3.0

**As verified 5 November 2026:** both `v1.0.5-preview.1` and `geoai-hosts-v0.3.0-preview.1` exist as draft records with **zero uploaded assets**. The native Windows build is complete, including a 1,408,242,136-byte MSI. The upload stage—not the compiler—failed; a full rebuild is unnecessary if both original build manifests and hashes still agree.

## Resume the existing native build and publish

From Windows PowerShell 7 in `C:\Users\GKMA\Downloads\Apps\world-twin-agents`:

```powershell
git pull --ff-only origin ui/premium-glass-workstation-20261030
node --test tests/release-publication-contract.test.mjs
.\.venv\Scripts\python.exe -m pytest -q tests/unit/test_preview_release_pipeline.py
pwsh -NoProfile -File .\scripts\releases\build-and-publish-previews.ps1 -Publish -PublishExisting
```

The script compares `host-v2-build-report.json` and `host-plugin-build.json` against the six original native binaries and original compiled commit `64452231cabee5d1e6b6124923c25d1b2d5ebea9`, rechecks MSI ProductVersion 1.0.5, and verifies that subsequent source changes were limited to release tooling and generated ArcGIS bin/obj outputs. It refuses reuse after any other application code changes.

For each existing draft, Python coordinates a numeric GitHub release ID; `scripts/releases/upload-preview-asset.ps1` uses authenticated PowerShell `Invoke-RestMethod -InFile` for the large MSI and other binary files. It resumes matching uploaded files but never deletes or overwrites mismatches. Every remote asset must report the expected size, upload state and SHA-256 digest, including `release-evidence.json` and `SHA256SUMS.txt`.

**Only after all remote files verify:** both GitHub releases are changed to `draft=false`, `prerelease=true`, `make_latest=false`; their public links are verified and the README, changelog, release notes and detailed preview Markdown are synchronized to the public repository. No stable signed updater is implied.

If an upload fails, the drafts remain intact. Inspect the PowerShell HTTP error and retry the same resumable command rather than rebuilding or promoting empty releases.

## Build outputs and publication evidence

- `build/geoai-host-v2/` — authentic Esri add-in, ArcGIS/QGIS ZIPs, SDK source ZIP and wheel, build reports.
- `apps/desktop/src-tauri/target/release/bundle/msi/AGOT Desktop_1.0.5_x64_en-US.msi` — original compiled Windows x64 installer.
- `build/public-preview-publish/staged-assets/` — renamed, hash-checked copies for GitHub.
- `build/public-preview-publish/generated-notes/` — generated Desktop/Hosts release notes and source evidence.
- `build/public-preview-publish/public-preview-publisher-report.json` and `windows-preview-build-report.json` — final status and failure details.

[Complete files and SHA-256](PREVIEW_CANDIDATE_ASSETS_1.0.5_0.3.0.json) · [Publication checklist](RELEASE_1.0.5_0.3.0_PUBLICATION_CHECKLIST.md).

## Install and test without AGOT Desktop

Build only the independent host packages if the full AGOT MSI is not needed:

    pwsh -NoProfile -File .\scripts\build-install-gis-host-v2.ps1 -SkipAGOTDesktop -InstallQGISDefaultProfile

Run non-mutating local model/GIS presence diagnostics:

    pwsh -NoProfile -File .\scripts\releases\verify-standalone-host-runtime.ps1 -OllamaModelId <exact-installed-model-ID>

ArcGIS Pro 3.7: open the GeoTwins dock → Standalone GeoAI tab → local proposal GP tool → exact source SHA review → local execution tool. A separately running Ollama and tool-capable model are needed for AI plans; AGOT Desktop must stay closed during standalone testing. The other Native GIS tab can run its non-AI tools without any model.

QGIS: install ZIP → Standalone AI → enter actual installed model ID → select owned layers, enter instruction, propose -> review Plan -> approve native QGIS Processing. Source metadata/typed operation planning stays on localhost; geometry never enters Ollama. Native GIS tab can run without Ollama.

Optional connected mode: start matching AGOT MSI, run scripts/verify-gis-host-pairing.ps1 and scripts/acceptance/verify-connected-fullstack.py (with authenticated test token) and repeat independently approved host plans.

## Stable-release prohibitions

Do not replace public experimental preview tags with stable tags; do not claim the model/GIS tests passed unless actual recorded host evidence exists; do not publish a signed automatic updater without a real matching Tauri signature; do not silently relicense QGIS plugin code. Full Windows/host/real-model field acceptance remains necessary.
