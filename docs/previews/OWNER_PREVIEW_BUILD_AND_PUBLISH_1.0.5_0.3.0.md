<!-- Source specification only. No MSI, add-in or public 1.0.5/0.3.0 release has yet been uploaded by this docs commit. -->

**STATUS: SOURCE IMPLEMENTED, BINARIES NOT YET PUBLISHED.** The Windows owner build and real GIS host acceptance are required before the tags/downloads can go live.

# Owner release procedure — AGOT Desktop 1.0.5 + standalone GIS SDK 0.3.0

## One command: full Windows build and public experimental prereleases

From the PR #21 checkout on the Windows 11 workstation:

1. Close AGOT, ArcGIS Pro and QGIS so binaries and Python plugin files are not locked.
2. Install Visual Studio 2026 / .NET SDK 10; keep licensed ArcGIS Pro 3.7, QGIS 3.44, Python 3.12, Rust, Node 22, WebView2 and the canonical AGOT desktop/PostGIS build prerequisites available.
3. Authenticate GitHub CLI using gh auth login. The account needs write permission to the **aerocorp13/AGOT-Releases** repository (both Contents and Releases).
4. Ensure your branch has no uncommitted changes and pull the latest source:

    git checkout ui/premium-glass-workstation-20261030
    git pull --ff-only origin ui/premium-glass-workstation-20261030

5. Build everything locally first, without publication:

    pwsh -NoProfile -File .\scripts\releases\build-and-publish-previews.ps1

6. Publish both **complete PUBLIC GitHub experimental PRERELEASES**, with real MSI, Esri add-in, both GIS host ZIPs and SDK wheel/source ZIP:

    pwsh -NoProfile -File .\scripts\releases\build-and-publish-previews.ps1 -Publish

The publisher runs npm typechecks/tests, host SDK tests and the existing canonical Windows runtime + MSI build. It refuses a dirty or stale source SHA, mismatched ProductVersion or package version, missing or stale artifact, failed test, bad .NET 10 add-in, failed upload or mismatched GitHub asset inventory. An existing release tag is never overwritten. The publisher first stages complete uploads as temporary drafts, checks them, updates AGOT-Releases Markdown and finally publishes as **isDraft=false, isPrerelease=true**. On failure it attempts to clean up ONLY new drafts from its own invocation. Neither release is marked stable.

If the source baseline origin/main is absent, fetch origin/main first. Detailed generated notes use the exact source commit and all local built artifact hashes.

## What the publisher produces

Build: build/geoai-host-v2, with full native host binaries, companion, SDK and optional matching AGOT MSI.

Staged local artifacts and generated release notes:
- build/public-preview-publish/staged-assets/desktop/
- build/public-preview-publish/staged-assets/hosts/
- build/public-preview-publish/generated-notes/desktop-notes.md
- build/public-preview-publish/generated-notes/hosts-notes.md
- build/public-preview-publish/generated-notes/release-evidence.json
- build/public-preview-publish/public-preview-publisher-report.json
- build/public-preview-publish/windows-preview-build-report.json

Each release has SHA256SUMS.txt, release-evidence.json, detailed Markdown and real binary files. The cloned AGOT-Releases main branch receives docs/previews/AGOT_DESKTOP_1.0.5_PREVIEW_N.md and GEOAI_HOSTS_0.3.0_PREVIEW_N.md, updated README, CHANGELOG, RELEASE_NOTES and channel notes. Historical published releases are retained.

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
