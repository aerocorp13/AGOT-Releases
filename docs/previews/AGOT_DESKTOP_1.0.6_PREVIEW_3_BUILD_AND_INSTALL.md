# AGOT Desktop 1.0.6 Preview 3 — Windows build and installation verification

**Candidate only — MSI not yet published.** This is not an installer download page. The public preview continues to be [Preview 2](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.6-preview.2) until an actual Preview 3 release has passed its build and upload checks.

## Builder

The source branch is [PR #21](https://github.com/aerocorp13/world-twin-agents/pull/21). The native Windows 11 workstation must have the pinned desktop Python 3.12 environment, the normal Rust/Visual Studio build toolchain, a valid local GDAL/PROJ runtime and GitHub CLI authenticated with release-repository write access.

From PowerShell 7 in the source checkout:

```powershell
git checkout ui/premium-glass-workstation-20261030
git pull origin ui/premium-glass-workstation-20261030

# Tests, exact-source native MSI build, local staging. Does NOT publish.
# ReuseFrozenRuntime avoids repeating the already frozen Python backend only if its source manifest matches.
.\scripts\releases\build-and-publish-desktop-v106-preview3.ps1 -ReuseFrozenRuntime -Jobs 2

# After inspecting successful build evidence, publish verified bytes and docs.
.\scripts\releases\build-and-publish-desktop-v106-preview3.ps1 -UseExistingBuild -Publish
```

To perform both stages in one operation, use `-Jobs 2 -Publish`, but no release is created when tests, MSI packaging, privacy inspection or build evidence fails. The script reuses the existing source-aware `publish_desktop_existing.py` publisher, the exact `artifacts.json` build receipt, Windows MSI ProductVersion inspection and GitHub draft/hash verification.

## What is distributed

- A **Windows x64 MSI**, still with **ProductVersion 1.0.6** and a new prerelease tag `v1.0.6-preview.3`.
- Attached `release-evidence.json`, `SHA256SUMS.txt` and `PREVIEW_3_CHANGES.md`, calculated from the actual build and uploaded only after the native checks pass.
- No developer's database, PostgreSQL cluster data, sample projects, runtime credentials or previously open personal tabs.
- No separate 0.7.0 SDK or native QGIS/ArcGIS plugins; those require their own verification and release process.

## First-run validation

After obtaining the **actual** Preview 3 release MSI, verify its downloaded SHA-256 against `SHA256SUMS.txt`. Install using a clean Windows user profile; open AGOT and verify Home has no previous projects, West Africa maps or restored tabs. Open Settings and check the live local PostGIS version and `agot_public` database identity. Import/create one real project, close and reopen to check persistence. Verify a separate Windows account cannot see the first account's project. Before replacing an existing Preview 2 MSI, back up data and test same-version MSI repair/reinstall behavior; Preview 3 is **not** a new Windows Installer ProductVersion.

**No installed Windows test evidence is asserted by this document.** Source and MSI verification do not certify geoprocessing accuracy, third-party cloud authorization, 3D renderer behavior or full host/plugin integration.

## Changes

Read [AGOT Desktop 1.0.6 Preview 3 changelog](AGOT_DESKTOP_1.0.6_PREVIEW_3.md) for the detailed feature and privacy-fix list. Once the MSI is actually published, the verified release page is https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.6-preview.3.
