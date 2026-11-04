# AGOT Desktop 1.0.4 — experimental Windows preview 1

**Channel:** v1.0.4-preview.1 (prerelease, not stable or an automatic updater).  
**Release:** https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.4-preview.1  
**Product:** Windows x64 desktop workstation. Primary development target: Windows 11.

## Binary integrity
- File: **AGOT.Desktop_1.0.4_x64_en-US.msi**
- Size: **1,408,192,984 bytes** (approximately 1.31 GiB)
- SHA-256: **1d02e66348cbde2d4c4157d096987c3659f9d87709789f3f7429ba8702899770**
- Authenticode at build inspection: **NotSigned**.
- The local checkout at upload was a997e9acfa601868620c6c6f79bd851a3ea17cda; this is **not** an independently attested exact binary provenance commit.

Run PowerShell Get-FileHash with -Algorithm SHA256 on the downloaded MSI and compare the entire hash. Run Get-AuthenticodeSignature separately. A GitHub checksum is not a code-signing certificate, and Windows SmartScreen may warn.

## Install for nonproduction evaluation
1. Download the MSI from GitHub release **Assets**, not the generated Source code ZIP.
2. Back up local AGOT projects, configured data folders, and any historic version. Preview 3 data may be in the user application data directory under af.agot.desktop/runtime-v1.
3. Prepare Windows 11 x64, WebView2 and sufficient free storage; avoid production workstations or irreplaceable GIS projects.
4. Close previous AGOT processes; run the MSI; inspect Windows signing warnings, do not bypass enterprise policy.
5. Launch the desktop, verify backend and GIS runtime startup, and test import, edit, geoprocess and reopen using authorized disposable datasets.
6. Test versions and Worlds, actual GeoAI provider connections and approval flow, source rights, 3D data and model inference only where configured.
7. Record failures and sanitized logs in GitHub Issues or send private security reports to admin@geotwins.org.

## Not yet accepted
The most recent source-side local report listed unresolved backend/PostGIS tests. Clean-machine installation, upgrades from 1.0.2 and earlier, project preservation, signed Tauri updater trust and runtime GPU/scientific correctness were **not** proven by building this MSI. Product-level claims remain experimental. No automatic updater latest.json or signed MSI .sig is provided.

## Acceptance
See [preview test matrix](PREVIEW_ACCEPTANCE_20261105.md), [installation](../INSTALLATION.md), [security](../../SECURITY.md). The preview is for voluntary manual testing; the published release page indicates whether it is actually available yet.
