# AGOT Desktop — public release notes

This page describes **published Windows installers**, not all code present in AGOT's private development repository. Release times are UTC. Each version is a public preview and remains subject to native acceptance testing.

| Channel | Publication | Product version | GitHub tag | Published MSI |
| --- | --- | --- | --- | --- |
| **1.0.5 experimental public preview** | **5 Nov 2026, 16:51 UTC** | **1.0.5** | [v1.0.5-preview.1](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.5-preview.1) | `AGOT.Desktop_1.0.5_x64_en-US.msi` · 1,408,242,136 bytes · SHA-256 verified |
| **1.0.4 experimental preview** | Check release for publication | 1.0.4 | [v1.0.4-preview.1](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.4-preview.1) | AGOT.Desktop_1.0.4_x64_en-US.msi, manual evaluation only |
| **Preview 3 (prior public baseline)** | **2 Nov 2026** | **1.0.2** | [`v1.0.1-preview.3`](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3) | `AGOT.Desktop_1.0.2_x64_en-US.msi` |
| Preview 2 | 1 Nov 2026 | 1.0.1 | [`v1.0.1-preview.2`](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.2) | `AGOT.Desktop_1.0.1_x64_en-US.msi` |
| Preview 1 | 29 Oct 2026 | 1.0.0 | [`v1.0.0-preview.1`](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.0-preview.1) | `AGOT.Desktop_1.0.0_x64_en-US.msi` |

**Naming note:** Preview 3’s tag is `v1.0.1-preview.3`, but the published release and MSI identify the **application and Windows Installer version as 1.0.2**. This historical discrepancy is recorded rather than silently relabeled.

## Desktop 1.0.5 and GIS Hosts / SDK 0.3.0 — public experimental prereleases

**Published on 5 November 2026, verified from GitHub's actual release assets.** The 1.0.5 Windows MSI (1,408,242,136 bytes) and all five GIS-host/independent Python SDK binaries are uploaded, non-draft prereleases. GitHub reports exact file sizes, uploaded states and SHA-256 digests; separate `SHA256SUMS.txt` and `release-evidence.json` files accompany each release.

- [Download Windows AGOT Desktop 1.0.5](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.5-preview.1) · [Detailed release notes](docs/previews/AGOT_DESKTOP_1.0.5_PREVIEW_1.md)
- [Download QGIS, ArcGIS Pro and Python SDK 0.3.0 packages](https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.3.0-preview.1) · [Detailed host notes](docs/previews/GEOAI_HOSTS_0.3.0_PREVIEW_1.md)
- [Verified candidate-to-public asset inventory and digests](docs/previews/PREVIEW_CANDIDATE_ASSETS_1.0.5_0.3.0.json)
- [Publication evidence and installed-host acceptance checklist](docs/previews/RELEASE_1.0.5_0.3.0_PUBLICATION_CHECKLIST.md)
- [2027 Linux/macOS development targets](ROADMAP.md)

**Original compiled source SHA:** `64452231cabee5d1e6b6124923c25d1b2d5ebea9`. The Windows MSI is unsigned at the recorded inspection and neither preview guarantees clean upgrades, licensed Esri/QGIS execution, reliable model inference, certified scientific results or signed Tauri automatic updates. These are published experimental packages, not stable production acceptance.

## Experimental 1.0.4 Windows and GeoAI host 0.1.0 previews

The newer **AGOT Desktop 1.0.4 manual MSI** and the separate **QGIS / ArcGIS Pro GeoAI 0.1.0 host packages** have individual experimental guides: [Desktop MSI](docs/previews/AGOT_DESKTOP_1.0.4_PREVIEW_1.md), [QGIS](docs/previews/QGIS_GEOAI_0.1.0.md), [ArcGIS Python](docs/previews/ARCGIS_PRO_PYTHON_GEOAI_0.1.0.md), [ArcGIS native](docs/previews/ARCGIS_PRO_NATIVE_GEOAI_0.1.0.md), [Host SDK](docs/previews/GEOAI_HOST_SDK_0.1.0.md), [Acceptance matrix](docs/previews/PREVIEW_ACCEPTANCE_20261105.md). Verify publication status on GitHub. These do not include verified stable Tauri update artifacts.

## Preview 3 — AGOT Desktop 1.0.2

[Open full release page](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3).

**Key changes, as recorded in the published release:**

- **Versioned World history:** immutable source/manual-state membership, pinned historical reads, controlled scenario forks, recorded-time corrections and permission checks on historical reads.
- **Durable GeoAI work:** persisted plans, per-step progress, cooperative cancellation, resume after interruption, and verified action receipts. The optional bounded investigation loop supports up to four planning rounds and twelve registered tool actions.
- **Human review:** effectful spatial processing proposals require an explicit approval step; approved outputs become revisioned datasets with upstream lineage and access control.
- **ONNX inference bookkeeping:** retries, cancellation history, lease state and model/source/output digest checks. A compatible, authorized **user-provided model checkpoint** is needed for real segmentation.
- **Local workstation integration:** GIS, imagery, terrain and 3D workflows use packaged backend/GIS components and a PostGIS-backed spatial runtime.
- **Build repairs:** the release description records a PostgreSQL batch-insert fix for World source/version tests and updated GeoAI regression expectations.

**Installer:** `AGOT.Desktop_1.0.2_x64_en-US.msi`, **1,394,453,352 bytes**; GitHub-published SHA-256 `07203740b2e9196cef0d6216f6a6bfff4fa9b11fbdc86cfa273850ba0cbd0a20`.

**Not yet broadly validated:** clean Windows install/upgrade/uninstall and restore; live local LLM interoperability; licensed checkpoint inference accuracy; scientific simulation calibration; large-city/point-cloud/BIM coverage; complete 3D/synchronized multi-view behavior; digitally signed, portable World packages. Some cancellation remains cooperative rather than forceful. Integrity hashes do not equal digital signatures.

## Preview 2 — 1.0.1

[Release](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.2). A more complete ribbon-oriented GIS workstation and expanded MapLibre, editing, PMTiles, catalogs, imagery/STAC pathways, GIS geoprocessing and 3D development foundations. Enhanced permissions, private model credentials and plugin package validation. Some advanced workflows remained experimental.

## Preview 1 — 1.0.0

[Release](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.0-preview.1). Initial public Windows desktop MSI distributing the early integrated GIS, terrain and twin workbench.

## Prior to installation

Read [Installation](docs/INSTALLATION.md), [Quality and limitations](docs/QUALITY_AND_LIMITATIONS.md) and the **actual per-release notes**. Back up projects before changing versions. Do not equate a published package, passing isolated unit tests or a demo with complete platform validation. Future functionality is tracked in [Roadmap](ROADMAP.md).

This repository is a **distribution endpoint**; its GitHub-generated source archives are not AGOT's private application source. Contact [admin@geotwins.org](mailto:admin@geotwins.org) for support.
