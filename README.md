# AGOT Desktop
### African Geospatial Operational Twin · by [GeoTwins Africa](https://geotwins.org)

**A source-aware GIS and multi-world digital-twin workstation for mapping, geospatial analysis and evidence-led infrastructure planning.**

AGOT brings professional geospatial workflows, versioned operational worlds, human-reviewed GeoAI tools, 2D/3D visualization and emerging scenario simulation into one Windows desktop workspace. Our initial focus is **climate-resilient infrastructure and urban planning in data-scarce African contexts**; the architecture is not limited to Africa.

> **Public preview — not a stable production release.** Published capabilities are unevenly mature. Real data, licensing and professional decisions remain the user's responsibility. The latest public installer is **AGOT Desktop 1.0.2 / Preview 3**, published 2 November 2026 (UTC).

[**Download latest public release**](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3) · [**Download Preview 3 directly**](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3) · [**GeoTwins website**](https://geotwins.org) · [**Report a problem**](https://github.com/aerocorp13/AGOT-Releases/issues)

## Current downloadable build

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

## Five-minute evaluation

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

_Release and documentation snapshot: 3 November 2026. For the authoritative assets and version-specific limitations, always consult the individual GitHub release._
