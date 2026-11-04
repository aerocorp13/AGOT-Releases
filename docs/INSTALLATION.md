# Install, verify and evaluate AGOT Desktop

**Using the newer experimental 1.0.4 MSI?** Read [Preview 1.0.4 installation and limitations](previews/AGOT_DESKTOP_1.0.4_PREVIEW_1.md) and [next-day acceptance](previews/PREVIEW_ACCEPTANCE_20261105.md). The following 1.0.2 hash and instructions are for historical Preview 3 only.

These instructions are for **AGOT Desktop 1.0.2 — Public Preview 3** on Windows x64. It is a pre-release evaluation build; back up important data and prefer a non-critical computer or test environment.

## 1. Download the real asset

Go to the [Preview 3 GitHub release](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3) and use its **Assets** section. Download:

- **File:** `AGOT.Desktop_1.0.2_x64_en-US.msi`
- **Published byte size:** 1,394,453,352
- **GitHub asset digest (SHA-256):** `07203740b2e9196cef0d6216f6a6bfff4fa9b11fbdc86cfa273850ba0cbd0a20`
- **Product / Windows installer version:** 1.0.2
- **Release tag:** `v1.0.1-preview.3`

Do not mistake the small GitHub auto-generated source ZIP for the AGOT desktop application; this public repository is distribution documentation only.

## 2. Check integrity and signing separately

Open PowerShell in the installer directory:

```powershell
Get-FileHash -LiteralPath ".\AGOT.Desktop_1.0.2_x64_en-US.msi" -Algorithm SHA256
Get-AuthenticodeSignature -FilePath ".\AGOT.Desktop_1.0.2_x64_en-US.msi" | Format-List Status,SignerCertificate,StatusMessage
```

Compare the entire output hash against the **GitHub-published digest** above. A matching digest checks the downloaded bytes against GitHub's asset record; it does not establish malware-free content or author identity. Review the PowerShell signing result yourself. **Code signing was not independently verified for this release.** Windows SmartScreen may warn about unsigned or unfamiliar software.

If the hash differs, **do not run the installer**. Redownload from the official asset and report the issue privately.

## 3. Prepare the environment

- Windows x64, targeting Windows 11; full Windows 10 and clean-machine coverage is not confirmed.
- Adequate disk space for an approximately 1.30 GiB download, installation and local data.
- **Microsoft Edge WebView2 Runtime**. The installer may need network access to obtain it if absent.
- Local GIS/runtime/PostGIS components packaged or configured for the selected workflow.
- Optional internet connectivity for online basemaps, imagery providers and external services.
- Optional separately configured local LLM/model service for those GeoAI functions; a compatible user-provided ONNX checkpoint for segmentation.

No blanket promise of universal hardware compatibility, no-internet operation or automatically available model services is made.

## 4. Install and first run

1. Close running AGOT Desktop processes.
2. Back up any older project data first.
3. Run the MSI and follow Windows Installer prompts. Check the publisher/signing result instead of ignoring unfamiliar prompts.
4. Launch AGOT Desktop and check whether the local GIS backend and required services report available.
5. Start with authorized test layers and simple supported mapping operations. Introduce Worlds, approved GeoAI and 3D/model steps only after confirming their requirements.

## 5. Before upgrading from an older preview

- Close AGOT Desktop.
- Back up local projects and any custom data directory.
- **Default workspace identified in Preview 3 notes:** `%APPDATA%\af.agot.desktop\runtime-v1`. A configured override may store data elsewhere.
- Record current installer version and project IDs.
- Do not rely on in-place upgrade compatibility or automatic restoration unless you have verified it with your own environment. Stable application identity is an engineering prerequisite, not complete data migration acceptance.
- Keep safe copies and test open/reopen behavior after upgrade.

There is **no verified automatic desktop updater**. New public releases on geotwins.org or GitHub do not update installed copies.

## 6. Report a reproducible problem

Share the version, Windows edition/build, exact MSI filename, attempted task, source format and CRS (if applicable), whether the service/model was configured, and sanitized error or log text. **Never post passwords, access tokens, sensitive location datasets, personal records or private project archives.**

Email: [admin@geotwins.org](mailto:admin@geotwins.org). Security concerns: [SECURITY.md](../SECURITY.md). Known blockers: [QUALITY_AND_LIMITATIONS.md](QUALITY_AND_LIMITATIONS.md).
