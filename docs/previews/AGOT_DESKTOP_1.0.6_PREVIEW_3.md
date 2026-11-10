# AGOT Desktop 1.0.6 — Preview 3

**Status: candidate; not published until a complete Windows MSI is built, inspected and hash-verified.** Same installed application version **1.0.6**, new prerelease tag **`v1.0.6-preview.3`**. Experimental Windows x64, not a stable, signed updater or field-certified release.

## What changed since Preview 2

- **Public-profile isolation:** Fresh installations use a separate `runtime-public-v1` per-Windows-account application-data root, an exclusive desktop runtime profile and credentials, and bundled **PostgreSQL 17 + PostGIS** with database `agot_public`. This does not adopt the developer's old `runtime-v1` database or system PostgreSQL 16/17/18 services. Existing personal database bytes are preserved, not imported or deleted.
- **Clean first launch:** Home opens without restoring the developer's previous map, West Africa tests, selected projects or Dockview tabs. Projects and datasets require deliberate create/open/import actions. Development fixtures are disabled for the public profile.
- **Database diagnostics:** Settings reads the active PostgreSQL/PostGIS versions, database identity and actual record counts from the authenticated local service.
- **Project-first Home:** Real recent projects, create/open workspace, Save, Save As, Export `.agotproject`, and useful Learn/task entrypoints. A clean user sees an empty project list, not fabricated examples.
- **Dockable Ask GeoAI:** A right-edge or floating tool for source-bound review/approval and returned GIS results, sharing the existing registered AGOT geoprocessing executor rather than an unrestricted secondary executor. Cloud transfer requires consent.
- **Guided and Professional task entry:** Same backend operations, source permissions, saved results and processing history. The UI exposes task-oriented access without hiding professional GIS parameters.
- **Source-bound mission:** Explicitly pin a verified World → Simulation → Twin → 3D study/scene pair to the managed project. A missing study or scene ID blocks pinning; permissions and source identity must be rechecked on reopen.
- **Package privacy guard:** The MSI build rejects PostgreSQL cluster data, credentials and operator GIS exports. It now distinguishes a legitimate pgAdmin/Azure dependency directory named `profiles` from AGOT operator profile data, addressing the Preview 3 build failure.
- **Build regression fixes:** Restored accessible Recent projects and Save As labels; TypeScript mission callback now safely narrows nullable persisted IDs.

## What is **not** claimed

- This Markdown is a **source change record**, not an installed-Windows acceptance certificate.
- Native QGIS/ArcGIS Pro agent execution, model-provider breadth, GPU simulation accuracy, signed Tauri updates and complete production readiness remain separately verified workstreams.
- SDK/GeoAI Hosts 0.7.0 are **not** included in this Desktop-only release. Previously published 0.6.0 host packages are separate and must not be renamed.
- A same-version `1.0.6` MSI can have Windows Installer repair/reinstall behavior instead of a true version upgrade. Preview 2 → Preview 3 replacement must be tested on Windows without deleting user data.

## Build, verification and publication

1. Check out the clean exact source commit from PR #21 and run `npm test`, `npm run typecheck`, `npm run typecheck:desktop` plus the Python privacy tests.
2. Build a native Windows x64 MSI with `scripts/build-desktop.ps1 -Bundle msi -Jobs 2`. The mandatory resource scanner must pass. Do **not** use `-SkipTests` for public release evidence.
3. Run the Preview 3 publisher, which reopens the original completed `artifacts.json` and `build.log`, validates that the MSI was produced from the recorded source SHA, inspects MSI ProductVersion 1.0.6, calculates a SHA-256 and checks the upload against GitHub's independent digest.
4. Stage an experimental GitHub prerelease with `v1.0.6-preview.3`, release notes, `SHA256SUMS.txt`, `release-evidence.json` and the actual MSI. Do not publish if any asset, source hash, test transcript or metadata check fails.
5. On successful publication, the publisher copies this Markdown into public `AGOT-Releases/docs/previews/AGOT_DESKTOP_1.0.6_PREVIEW_3.md` and updates the public README's preview pointer. This step requires GitHub write authorization.

**Binary size, exact source SHA and SHA-256 must come from the completed native build and cannot be filled in ahead of time.**
