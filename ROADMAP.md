# AGOT — product and engineering roadmap

**Direction:** An interoperable, multi-world geospatial operating workstation for **climate-resilient infrastructure and urban planning**, starting with data-scarce African cities and regions. Users manage an authoritative **Operational World**, create governed **Scenario Worlds**, compare changes and generate evidence that can be reviewed before it changes spatial state.

This roadmap is a **prioritized engineering plan**, not a delivery commitment. No feature below is promised for a specific date, funded pilot or release unless explicitly recorded as published.

## Current public experimental baseline — 5 November 2026

- **AGOT Desktop Windows 1.0.5:** [v1.0.5-preview.1](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.5-preview.1), an actual 1,408,242,136-byte Windows x64 MSI with uploaded SHA-256 and source provenance. Concept 6 professional GIS workstation, source-backed Worlds and specialist modules, GIS jobs, experimental Twin/Simulation/GeoAI and developing large-scale 3D. This is **published**, not production-certified; clean Windows install and upgrade are separate gates.
- **GeoAI Hosts and standalone Python SDK 0.3.0:** [geoai-hosts-v0.3.0-preview.1](https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.3.0-preview.1), five real binaries: ArcGIS Pro .NET 10 add-in, ArcGIS Python toolbox ZIP, QGIS plugin ZIP, independent Python SDK source ZIP and wheel, plus hashes/evidence. Standalone native host GIS and reviewed local Ollama workflows are distinct from optional connected AGOT mode. Installed Esri/QGIS and model acceptance remain separate.
- **Older Preview 3 (1.0.2):** historical release. These newer public previews supersede it as the latest download choices, but do not imply every source capability is tested in production.

See [release notes](RELEASE_NOTES.md) and [capability matrix](docs/CAPABILITY_MATRIX.md) for specific boundaries.

## Release gates before broad production claims

| Priority | Milestone | Evidence required |
| --- | --- | --- |
| **P0** | **Windows install/upgrade and data safety** | Clean Windows 11 x64 MSI installation; in-place upgrade from earlier preview; uninstall/reinstall; repeatable project backup/restore; WebView2 provisioning; signing/terms audit |
| **P0** | **Reliable operational GIS** | Real user-controlled vector/raster datasets, CRS/geometry correctness, project persistence, permission-denial tests, measured job success and failure modes |
| **P0** | **GeoAI is an operator, not just a chatbot** | Ground every recommendation in real dataset/tool provenance; visible approval before edits; working local/remote provider adapters; resume, cancel, audit and rollback/compensation where appropriate |
| **P0** | **Reproducible World versions** | Canonical asset IDs, bitemporal/historical reads, branching with permissions, no silent mutation of baseline, consistent outputs and source traceability |
| **P1** | **Native workstation polish** | Accessibility, responsive docking, saved layouts, high-DPI and multi-monitor tests, true local screenshots in light and dark, offline/error recovery |
| **P1** | **Spatial 3D interoperability** | Verified terrain/vertical-datum handling and bounded map/Three/Cesium rendering; explicit 3D Tiles, GLB, CityJSON and IFC coverage where tested |
| **P1** | **Scenario comparison and exports** | Operational vs scenario comparison, source-backed indicators, versioned evidence, reproducible report/map exports |
| **P2** | **Extensibility and deployment** | Public tools/plugin contracts, optional adapters, predictable upgrades, licensing/third-party disclosure, deployment and user feedback loop |

## Linux and macOS — planned 2027 experimental candidates

These are **coming soon, not downloadable and not committed to a specific day**. The current AGOT 1.0.5 desktop runtime and installer still contain Windows `.exe` service/PostGIS/GDAL paths, Windows-specific bundling and Windows PATH semantics. A Tauri cross-platform UI compile does not prove that AGOT starts as a real Linux/macOS GIS workstation.

| Operating system | 2027 target | Required platform proof |
| --- | --- | --- |
| **Linux x86_64** | AppImage and DEB development candidates; RPM/ARM under evaluation | Native service/embedded PostGIS packaging, libwebkit2gtk-4.1 and GIS libraries, actual Ubuntu/Debian clean install, project recovery, GPU and geoprocessing |
| **macOS ARM64 and Intel** | App bundle/DMG development candidates | Portable bundled GIS/PostgreSQL binaries, macOS permissions, Apple code signing/notarization, real Apple Silicon and Intel runtime/GPU/upgrade tests |
| **Automatic host extension updates** | Separate future feature | Trusted QGIS/ArcGIS distribution policy, signing and rollback; website dynamic release listings are **not** installed plugin updates |
| **Signed desktop automatic updates** | Separate acceptance gate | Cryptographically signed Tauri updater artifacts and validated update manifest per platform, not only GitHub SHA-256 |

The [cross-platform development scripts and 2027 acceptance matrix](https://github.com/aerocorp13/world-twin-agents/blob/ui/premium-glass-workstation-20261030/docs/platforms/CROSS_PLATFORM_2027_ROADMAP.md) are now in the software repository. They run native OS source checks and refuse to make bundles while platform-specific service/GIS runtime blockers remain. Public Linux/macOS installers will be linked only after recorded native acceptance and publication.

## First vertical: scenario digital twins for African planning

**Operational World:** map existing roads, buildings, land use, growth corridors, infrastructure assets, water systems, imagery and observation dates with explicit source quality and uncertainty.

**Scenario Worlds:** fork alternative development assumptions such as Green Growth, Higher Warming / 2030 and Fragility. Treat labels as **user-defined scenarios**, not official climate predictions. Changes to land use, footprints, infrastructure and environmental forcing must be backed by inputs and recorded methods.

**Compare and explain:** prioritize urban extent/growth, infrastructure exposure, water stress, heat/flood risk and adaptation interventions. Support maps, metrics and ranked options only when underlying source data, models and calibration are sufficient. Show unknowns rather than synthesizing false precision.

**Reproducible decision record:** preserve input versions, spatial operations, solver/model identities, parameters, approvals and output hashes. Keep the baseline immutable across hypothetical experiments.

## GeoAI engineering direction

1. **Tool registry + typed contracts:** dataset discovery, metadata inspection, geoprocessing, retrieval, World comparison and model inference as permissions-aware tools.
2. **Evidence → plan → approval → job → artifact → World:** record sources first, pause effectful steps for human review, retain outputs and lineage.
3. **Provider-independent harness:** local models and opt-in external services behind capability checks, budgets, retries, cancellation and auditable actions. Never state that a model is working unless it has passed live compatibility tests.
4. **Specialist GeoAI:** segmentation, change detection, hotspots, risk ranking, geospatial explanation and comparative scenario assessment—all subject to source and model validation.
5. **Resource-aware inference:** bounded GPU scheduling and transparent model/device requirements; no claim of bundled production ONNX segmentation checkpoints.

## Rendering and developer platform

Target one coherent user experience using MapLibre for 2D GIS, Three.js for local 3D scenes, and Cesium for globe and geodetic views **as implementations pass their respective gates**. Active private development has more sophisticated multi-engine and docking source than the publicly installed releases; source presence and passing unit tests alone do not establish native MSI behavior.

Potential interoperable services: GDAL/PROJ/PostGIS, STAC/COG/PMTiles, compatible OGC APIs, user-approved model endpoints and specialist geoprocessing engines. Each adapter needs explicit availability and licensing notices.

## Evidence and transparency rules

- **Published** only when there is a public tagged installer and corresponding feature/release description.
- **Demonstrated** only with an actual reproducible run and environment identified.
- **Experimental** when dependent on sample fixtures, external engines, unvalidated models or bounded implementations.
- **Planned** until shipping evidence exists.
- Do not use mock/synthetic data as if they were real African observations.
- No assertions of professional engineering/survey accuracy, hydrological calibration, regulatory acceptance or production pilots without independent evidence.

## Feedback and pilots

Desktop preview is free to evaluate; pilot access and future commercialization are separate decisions. We welcome reproducible GIS use cases from planners, utilities, cities, infrastructure organizations and researchers. Contact [admin@geotwins.org](mailto:admin@geotwins.org), including data permissions and the specific decision workflow you need.

Next public release is intentionally **unannounced** until the gates above are met. See [Product vision](docs/PRODUCT_VISION.md) and [quality limits](docs/QUALITY_AND_LIMITATIONS.md).
