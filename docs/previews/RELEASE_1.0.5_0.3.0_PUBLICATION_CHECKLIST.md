# AGOT Desktop 1.0.5 / GIS Hosts SDK 0.3.0 — public prerelease checklist

**Verified 5 November 2026:** Both `v1.0.5-preview.1` and `geoai-hosts-v0.3.0-preview.1` are **public experimental prereleases**, no longer drafts. GitHub reports **3 Desktop assets** (MSI, release-evidence.json, SHA256SUMS.txt) and **7 host/SDK assets** (five binaries, evidence, checksums), all with uploaded status, sizes and SHA-256 digests. The older 1.0.4 and 0.1.0 previews remain available.

**Exact source used for binary compilation:** [`64452231cabee5d1e6b6124923c25d1b2d5ebea9`](https://github.com/aerocorp13/world-twin-agents/commit/64452231cabee5d1e6b6124923c25d1b2d5ebea9).

## Required files

| Release | Binaries | Additional required evidence |
|---|---|---|
| AGOT Desktop 1.0.5 | `AGOT.Desktop_1.0.5_x64_en-US.msi` (1,408,242,136 bytes) | `release-evidence.json`, `SHA256SUMS.txt` |
| GIS Hosts / SDK 0.3.0 | `GeoTwins.GeoAI.ArcGISPro.esriAddInX`, `geotwins_geoai_arcgis_pro_0.3.0.zip`, `geotwins_geoai_qgis_0.3.0.zip`, `geotwins_geoai_python_sdk_0.3.0.zip`, `geotwins_geoai_sdk-0.3.0-py3-none-any.whl` | `release-evidence.json`, `SHA256SUMS.txt` |

See [candidate asset names, byte lengths and SHA-256 values](PREVIEW_CANDIDATE_ASSETS_1.0.5_0.3.0.json) recorded in the Windows build's draft notes. All six recorded binary hashes now match the independently reported GitHub public asset SHA-256 digests.

## Release process and retained verification record

1. From the original Windows build checkout, read `build/geoai-host-v2/host-v2-build-report.json` and `host-plugin-build.json`; verify the exact source SHA, successful tests/native build, MSI 1.0.5 ProductVersion and all six artifact SHA-256 hashes.
2. Use the current `scripts/releases/build-and-publish-previews.ps1 -Publish -PublishExisting`. The publication code uses numeric draft release IDs. The large MSI is uploaded by `scripts/releases/upload-preview-asset.ps1` using authenticated PowerShell `Invoke-RestMethod -InFile` rather than the failing Python file-object request.
3. Verify each GitHub asset name, byte count, `uploaded` state and digest against the recorded files. Confirm `release-evidence.json` and `SHA256SUMS.txt` on both release records.
4. Only after all assets verify, set both releases to **public experimental prereleases**: `draft=false`, `prerelease=true`, `make_latest=false`. No stable updater or signed `latest.json` is implied.
5. The anonymous public pages were verified, and public README/CHANGELOG/release notes are maintained alongside these preview documents.

### Owner command

```powershell
cd "C:\Users\GKMA\Downloads\Apps\world-twin-agents"
git pull --ff-only origin ui/premium-glass-workstation-20261030
node --test tests/release-publication-contract.test.mjs
.\.venv\Scripts\python.exe -m pytest -q tests/unit/test_preview_release_pipeline.py
pwsh -NoProfile -File .\scripts\releases\build-and-publish-previews.ps1 -Publish -PublishExisting
```

Historical recovery rule: a draft remains intact if an upload fails, and the publisher can resume identical assets. **The present 1.0.5/0.3.0 releases have already been successfully published.** Do not rerun this historical upload command to create duplicates; use the verified public release links above.

## Preview documentation

- [Desktop 1.0.5 release notes](AGOT_DESKTOP_1.0.5_PREVIEW_1.md)
- [QGIS, ArcGIS Pro and Python SDK 0.3.0 release notes](GEOAI_HOSTS_0.3.0_PREVIEW_1.md)
- [Candidate checksum inventory](PREVIEW_CANDIDATE_ASSETS_1.0.5_0.3.0.json)
- [Previous preview channel policy](CHANNELS_AND_RELEASE_NOTES.md)

**Limits:** Windows clean installation, upgrade continuity, ArcGIS Pro licensed execution, QGIS native execution, real local-model tool calls and numerical scientific accuracy remain subject to installed-host testing. The QGIS plugin includes a restricted evaluation license; the GitHub preview is not an official QGIS Plugin Directory release.
