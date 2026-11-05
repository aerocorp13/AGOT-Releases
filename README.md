# AGOT Desktop
### African Geospatial Operational Twin · by [GeoTwins Africa](https://geotwins.org)

**A source-aware GIS and multi-world digital-twin workstation for mapping, geospatial analysis and evidence-led infrastructure planning.**

AGOT brings professional geospatial workflows, versioned operational worlds, human-reviewed GeoAI tools, 2D/3D visualization and emerging scenario simulation into one Windows desktop workspace. Our initial focus is **climate-resilient infrastructure and urban planning in data-scarce African contexts**; the architecture is not limited to Africa.

> **Public preview — not a stable production release.** Published capabilities are unevenly mature. Real data, licensing and professional decisions remain the user's responsibility. Preview 3 (1.0.2) was published 2 November 2026. A newer experimental 1.0.4 MSI and QGIS/ArcGIS GeoAI host packages are documented separately; check GitHub Releases for their actual current public status.

[**Browse all published releases**](https://github.com/aerocorp13/AGOT-Releases/releases) · [**Download Preview 3 directly**](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3) · [**GeoTwins website**](https://geotwins.org) · [**Report a problem**](https://github.com/aerocorp13/AGOT-Releases/issues)

## Historical published baseline — Preview 3

| Item | Verified publication |
| --- | --- |
| Channel | Free public preview (pre-release) |
| Product / installer version | **1.0.2 — Preview 3** |
| GitHub release tag | `v1.0.1-preview.3` (historical tag differs from product version) |
| Release published | **2 November 2026, 21:24 UTC** (3 November in Uganda) |
| Target platform | Windows x64; Windows 11 is the primary target |
| Installer asset | `AGOT.Desktop_1.0.2_x64_en-US.msi` |
| Installer size | 1,394,453,352 bytes (approximately 1.30 GiB) |
| Published asset SHA-256 | `07203740b2e9196cef0d6216f6a6bfff4fa9b11fbdc86cfa273850ba0cbd0a20` |

The hash above is the **GitHub release asset digest**, not evidence of a code-signing certificate. Check the asset on the linked release before installation. A successful MSI upload does **not** certify clean-machine installation, installed upgrades, data restoration, code signing or all native workflows.

## What is in Preview 3?

- **Spatial workstation:** project-oriented map and geospatial editing workspaces, layer/catalog tools, imagery, terrain/3D pathways, and geoprocessing backed by local components.
- **Versioned Worlds:** retained source and manual-state membership, pinned historical reads, scenario forks, recorded-time corrections and source-permission rechecks.
- **GeoAI with oversight:** persisted multi-step plans, action progress, interruption/resume and cancellation boundaries, human approval before effectful GIS operations, and hash-verified execution receipts.
- **Reproducible vector workflows:** approved spatial operations can produce revisioned derived datasets; later approved steps can use their results while retaining source lineage and permissions.
- **Local inference job tracking:** ONNX job retries, worker leases, cancellation records and verified model/source/output hashes; **checkpoint models are not included**.
- **Desktop packaging:** a Windows x64 MSI integrating the application and packaged geospatial runtime dependencies.

**Important:** Availability is not the same as end-to-end validation. Exact workflow support depends on configuration, compatible data and the installed engines. Details are in [Capabilities and evidence](docs/CAPABILITY_MATRIX.md) and [Known limits](docs/QUALITY_AND_LIMITATIONS.md).

## Upcoming independently installable GeoAI SDK 0.3.0 and AGOT 1.0.5

**Windows native build complete; public upload pending at the 5 November 2026 check.** The 1.0.5 Windows MSI and five GIS Hosts / SDK 0.3.0 binaries were compiled from [source `64452231`](https://github.com/aerocorp13/world-twin-agents/commit/64452231cabee5d1e6b6124923c25d1b2d5ebea9). Both GitHub release records currently exist as **drafts with zero uploaded assets**, not live downloadable prereleases. Check [GitHub Releases](https://github.com/aerocorp13/AGOT-Releases/releases) for actual publication status.

- [AGOT Desktop 1.0.5 Preview 1 build and release notes](docs/previews/AGOT_DESKTOP_1.0.5_PREVIEW_1.md)
- [ArcGIS Pro, QGIS and standalone Python SDK 0.3.0 notes](docs/previews/GEOAI_HOSTS_0.3.0_PREVIEW_1.md)
- [Candidate binary checksums and sizes](docs/previews/PREVIEW_CANDIDATE_ASSETS_1.0.5_0.3.0.json)
- [Prerelease publication checklist and limitations](docs/previews/RELEASE_1.0.5_0.3.0_PUBLICATION_CHECKLIST.md)
- [Owner resumable Windows publish instructions](docs/previews/OWNER_PREVIEW_BUILD_AND_PUBLISH_1.0.5_0.3.0.md)

The older public 1.0.4 and 0.1.0 experimental releases are unaffected. The new packages do not imply signed stable automatic updating, clean Windows upgrade acceptance, real model validation or licensed GIS host certification.

## Experimental 1.0.4 and GeoAI host previews

- **[Desktop 1.0.4 experimental MSI](docs/previews/AGOT_DESKTOP_1.0.4_PREVIEW_1.md)** · [Release page](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.4-preview.1): unsigned at inspection, manual evaluation only; not a verified Tauri automatic update.
- **[QGIS GeoAI plugin](docs/previews/QGIS_GEOAI_0.1.0.md)** · **[ArcGIS Pro Python toolbox](docs/previews/ARCGIS_PRO_PYTHON_GEOAI_0.1.0.md)** · **[native Esri add-in](docs/previews/ARCGIS_PRO_NATIVE_GEOAI_0.1.0.md)** · [GIS host release](https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.1.0-preview.1).
- **[Shared host SDK](docs/previews/GEOAI_HOST_SDK_0.1.0.md)** · **[Release channels](docs/previews/CHANNELS_AND_RELEASE_NOTES.md)** · **[Next-day acceptance checklist](docs/previews/PREVIEW_ACCEPTANCE_20261105.md)** · [Plugins portal](https://geotwins.org/plugins/).

All current packages are **experimental**. Native installed-host, clean upgrade and backend acceptance have not been demonstrated by the release uploads. The QGIS ZIP includes a **restrictive evaluation-only license**, which does not authorize downstream redistribution or official marketplace submission. The experimental desktop and host packages are separately tagged and must not replace a stable signed updater feed. Check each release page to establish whether it has been published.

## Five-minute evaluation of historical Preview 3

1. Open the [Preview 3 release](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3) and download the named MSI from **Assets**.
2. Verify the downloaded file against the SHA-256 above; follow [installation and upgrade guidance](docs/INSTALLATION.md).
3. Launch AGOT, connect or open a compatible local project, and use authorized data you can share or test.
4. Start with a simple GIS map or layer workflow. Advanced Worlds, GeoAI, simulation and 3D work require supported sources and service configuration.
5. Report problems with the exact version, Windows build, feature, steps and sanitized error text.

## What is next?

Our direction is an **interoperable multi-world digital-twin operating system**: maintain an authoritative Operational World; fork scenario worlds; compare land use, infrastructure, urban growth, water stress and climate exposure; and use tool-grounded GeoAI to propose reproducible, reviewable GIS actions.

This is a **roadmap, not a promise of current capability**. See [Product vision](docs/PRODUCT_VISION.md), [Roadmap](ROADMAP.md) and [Architecture](docs/ARCHITECTURE.md).

## Documentation

| Guide | Purpose |
| --- | --- |
| [Release history](RELEASE_NOTES.md) · [Changelog](CHANGELOG.md) | Preview 1 → 2 → 3 and compatibility notes |
| [Installation and verification](docs/INSTALLATION.md) | Requirements, SHA-256, backups, upgrade precautions |
| [Capability matrix](docs/CAPABILITY_MATRIX.md) | Published, conditional, development and future capabilities |
| [Architecture](docs/ARCHITECTURE.md) | Desktop, GIS services, spatial data, GeoAI and World boundaries |
| [Product vision](docs/PRODUCT_VISION.md) | Africa planning wedge and multi-world design principles |
| [Roadmap](ROADMAP.md) | Quality gates and feature priorities, without invented ETAs |
| [Quality and limitations](docs/QUALITY_AND_LIMITATIONS.md) | Release acceptance still required; scientific and model caveats |
| [FAQ](docs/FAQ.md) | Sources, setup, licensing and support |
| [Demo and screenshots policy](docs/DEMO_AND_SCREENSHOTS.md) | How real captures and demos will be published |
| [Contributing](CONTRIBUTING.md) · [Security](SECURITY.md) | Feedback, private reports and support |

## Repository, license and support

This **public repository distributes installers and documentation**, not AGOT's application source. GitHub's generated “Source code” ZIPs here contain only this small distribution repository. The MIT license in this repository covers its public documentation and metadata; **it does not place the separately distributed AGOT executable or private source under MIT**. Verify the installer’s applicable terms and third-party notices before redistribution or production deployment. No public source license should be inferred from the release assets.

Website: [geotwins.org](https://geotwins.org) · Support: [admin@geotwins.org](mailto:admin@geotwins.org) · Responsible security disclosure: [SECURITY.md](SECURITY.md).

_Build-candidate documentation checked 5 November 2026; refer to GitHub release assets for the current publication state. For the authoritative assets and version-specific limitations, always consult the individual GitHub release._
