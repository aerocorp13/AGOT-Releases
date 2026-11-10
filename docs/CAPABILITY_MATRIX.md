# AGOT public preview capability and evidence matrix

**Evidence review: 10 November 2026.** Version numbers here describe **published evaluation assets**, not a promise that every visible AGOT tool, plugin or SDK function has passed an installed workstation test. A private draft development change is not a new public build. Use [current installation instructions](INSTALLATION.md) and the exact tagged GitHub assets.

## Current verified publication baseline

| Channel | Published artifact and exact evidence | Source baseline | Release status |
| --- | --- | --- | --- |
| Desktop 1.0.6 Preview 2 | [Windows x64 MSI](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.6-preview.2), **1,416,188,896 bytes**, SHA-256 `59ae2b13f2bddfb7cff5abea1fa090814b572eeeb87fd38bf20211a6182f4df3` | `9a0aa8b41cb7b7339a72296fdd9f6a48374ca77d` | Public experimental prerelease; recorded unsigned |
| Independent GeoAI Hosts / Python SDK 0.6.0 Preview 1 | [Five published files](https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.6.0-preview.1): QGIS ZIP, native ArcGIS `.esriAddInX`, ArcGIS Python ZIP, SDK wheel/source ZIP; [per-file hashes](previews/GEOAI_HOSTS_0.6.0_PREVIEW_1.md) | `756133f85b21e3e3a1cac3f6c2109683f983f72c` | Public experimental prerelease; release body reports **114 source/contract tests**; installed native hosts not certified |
| Next development | [Draft PR #21](https://github.com/aerocorp13/world-twin-agents/pull/21) | Head observed `756133f85b21e3e3a1cac3f6c2109683f983f72c` | Open/unmerged draft; may contain source code not shipped in Desktop 1.0.6 |

The Desktop 1.0.6 release is **not** compiled from the later 0.6.0 host commit. Do not combine their test claims or retroactively apply improvements to an already-published installer.

## Customer-facing capability matrix

| Workflow or interface | What exists in source/release documentation | What still requires independent acceptance |
| --- | --- | --- |
| Project/Home and document workstation | Projects, real recent-project list, launcher, map, saved workspace layout and multiple specialist pages in source | First-use navigation is overcrowded; simplify Home; verify save/restore, keyboard and high-DPI accessibility in installed Windows app |
| Guided GIS tasks | Seven task choices in `CustomerTaskLauncher.tsx` open existing workspaces | **Navigation only**, not a plain-English task to actual output; user must still traverse expert tools |
| Map, vector edit, measurements and GIS analysis | Registered source-based operations, editing, project layers, analysis UI and persisted GIS job pathways | Per-operation real input/output geometry and CRS, correct overlay selection, map attachment, export and reopen on actual reference datasets |
| GeoAI ask/workflow | Source includes model readiness, a workbench, typed workflow/grant/receipt code, evidence and multiple agent subviews | Eight top-level GeoAI sub-tabs and separated question UI remain confusing; one persistent Ask dock and genuine model → approved tool → persisted output are not field-certified |
| Model provider options | SDK source documents Ollama and optional compatible local/cloud provider adapters with explicit consent and guardrails | Model/tool-call compatibility, installed selection, native response routing, VRAM constraints, cloud consent and secrets handling for each actual provider |
| QGIS GeoAI 0.6.0 | Public QGIS ZIP, source-side dock/native Processing/tool-plan integration | Real installed QGIS plugin loading, dock layout, native model planning, approval, output layer and reopen, including mismatched QGIS versions |
| ArcGIS Pro GeoAI 0.6.0 | Public .NET `.esriAddInX`, Python toolbox ZIP, source-side ArcPy and receipt paths | Compatible licensed ArcGIS Pro runtime, green icon correctness, real plan/approve/ArcPy, pinned chat results, saved layer and reconnect |
| Portable Python SDK / MCP | Installable 0.6.0 wheel and source ZIP; restricted discovery/approval boundaries in private source | Actual installed SDK-to-host interoperability, versioned transport, agent failure/replan, provider selection and safe restart/no replay |
| Worlds and scenario versions | Source-documented immutable WorldVersion membership, scenario/fork lineage and governed dataset changes | Full real project → immutable World → controlled numerical study → persistent Twin and multiple 3D renderers, with source/rights proof |
| Simulation and flood exposure | Existing durable model/study pathways and source provenance in development | No blanket claim of field-calibrated flood risk or physically validated model outputs; require qualified source/units/reference datasets |
| 3D MapLibre / Three / Cesium | Source-documented renderer integration and distinct view engines | Installed Windows WebGL/8GB GPU/LOD/terrain, CRS and vertical datum accuracy, save/reopen and source identity across views |
| Desktop and host updates | Public website can discover independent versioned GitHub Releases | Website refresh is **not** a signed desktop updater and does **not** update QGIS/ArcGIS installations; clean installs and in-place upgrades remain separate gates |
| Linux/macOS / official plugin marketplaces | Plans and development exploration | No published native Linux/macOS binary, App Store approval or official QGIS Directory listing established by current assets |

## Evidence categories — never collapse these

**PUBLISHED** = authentic versioned downloadable file with exact byte identity and public metadata.

**SOURCE-IMPLEMENTED** = corresponding private source code or documented design exists; not necessarily compiled into the named release.

**SOURCE-TESTED** = an automated test/report exists for the exact source SHA; does **not** prove the result in a native installed GIS application.

**NATIVE-VERIFIED** = a running installed Windows/QGIS/ArcGIS instance executed a genuine tool and independently checked an output, source/CRS, approval, count/checksum and reopen.

**CUSTOMER-ACCEPTED / SCIENTIFICALLY VALIDATED** = real workflow/usability signoff, valid measurement/uncertainty and domain reference acceptance; not asserted for the above previews.

## Release gates for proposed 1.0.7 Desktop and 0.7.0 SDK/Hosts

1. Declutter Home and expose a single keyboard-accessible, project-aware **Ask GeoAI** composer everywhere, without deleting the professional GIS controls.
2. Make a novice task actually run: select real source layers → generated **typed** registered plan → review original effects → human approve → native QGIS/ArcGIS/AGOT tool → persisted result visible on map → save and reopen.
3. Treat missing data, offline local models, source drift, invalid CRS, empty legitimate outputs, cancellation, native engine failures and reconnect as explicit states; revise and reapprove any changed operation without a replayed effect.
4. Preserve the same exact source IDs, rights, results and receipts in Guided, Professional and plugin workflows.
5. Execute source/contract, disposable PostGIS, installed QGIS and licensed ArcGIS, Windows UI/clean upgrade, signing/update and GPU/scientific gates **separately**. Sign only after establishing release identity; do not label a checksum as an Authenticode signature.
6. Publish complete version-specific Markdown release notes, install/upgrade guides, five host package SHA-256 values, known issues, model/privacy limits and website deep links. Verify the deployed site separately.

Read the [main 1.0.7 / 0.7.0 UX roadmap](roadmaps/AGOT_1.0.7_GEOAI_HOSTS_0.7.0_UX_RECOVERY.md) and the [source-grounded component audit and test plan](roadmaps/AGOT_1.0.7_0.7.0_SOURCE_UI_AUDIT_20261110.md) before adding more GeoAI tabs or SDK surfaces.

## Historical previews

- [Desktop 1.0.5](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.5-preview.1) and [GeoAI Hosts 0.5.0](https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-host-v0.5.0) remain available for reproducible comparisons.
- The older [Preview 3](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3) used product version **1.0.2** despite its `v1.0.1-preview.3` tag. This historical mismatch is preserved rather than silently renamed.

Do not post customer datasets, private credentials or confidential host logs in public issues. Report sanitized failures with [GitHub Issues](https://github.com/aerocorp13/AGOT-Releases/issues).
