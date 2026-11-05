# Changelog

Public Windows preview timeline, most recent first. This log is historical, not a list of unsupported future claims. All dates are UTC.

## 2026-11-05 — Published Desktop 1.0.5 and GIS Hosts / SDK 0.3.0 experimental previews

- **Windows Desktop 1.0.5 publicly released:** [`v1.0.5-preview.1`](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.5-preview.1), real x64 MSI (1,408,242,136 bytes) and GitHub SHA-256/file provenance. Original native build source `64452231cabee5d1e6b6124923c25d1b2d5ebea9`.
- **Independent GIS Hosts and Python SDK 0.3.0 publicly released:** [`geoai-hosts-v0.3.0-preview.1`](https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.3.0-preview.1), actual ArcGIS Pro 3.7 .NET 10 add-in, ArcGIS toolbox ZIP, QGIS plugin ZIP, Python SDK source ZIP and Python wheel.
- **Software progress:** Concept 6 desktop workstation and specialist modules, source-aware Worlds, typed GeoAI/model readiness, native GIS jobs and reviewed Ollama planning, alongside evolving city-scale 3D/simulation pipelines. A completed native build is not proof that every real workflow is field accepted.
- **Release upload correction:** public previews were promoted only after independent SHA-256 and size checks for each remote asset, with matching `SHA256SUMS.txt` and `release-evidence.json`. [Detailed notes](RELEASE_NOTES.md) and [asset evidence](docs/previews/PREVIEW_CANDIDATE_ASSETS_1.0.5_0.3.0.json).
- **2027 direction:** Linux AppImage/DEB and macOS ARM64/Intel app/DMG planned; source gate and native-runtime portability work begin before any public OS-specific bundles. [Roadmap](ROADMAP.md).
- **Remaining gates:** Windows install/upgrade and data recovery, licensed QGIS/ArcGIS host execution, validated local models and numerical outputs, signed updater artifacts and platform-specific field acceptance. No stable signing or marketplace approval claimed.

## 2026-11-02 — Desktop 1.0.2 / Preview 3
- Published [Preview 3](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3) with a Windows x64 MSI.
- Added release-documented versioned World membership, historical reads, scenario forks and corrections with source-permission checking.
- Added durable, auditable GeoAI plans, bounded investigation flow, human approval for effectful spatial steps and revisioned outputs.
- Exposed local ONNX work scheduling, retry/cancellation/lease audit and hash-verified source/model/output evidence.
- Documented world-source PostgreSQL batch-insert stabilization and related regression repairs.
- **Known gate:** no blanket guarantee of clean-machine deployment, live inference quality, model availability, signed World export or calibrated simulations.

## 2026-11-01 — Desktop 1.0.1 / Preview 2
- Published [Preview 2](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.2).
- Expanded ribbon workstation, professional map/editing workflows, imagery and source handling, PMTiles/STAC pathways, permissions and selected GIS operations.
- Continued terrain-aware 3D, Worlds and GeoAI integration; advanced functions remained experimental.

## 2026-10-29 — Desktop 1.0.0 / Preview 1
- Published [Preview 1](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.0-preview.1), the first AGOT Desktop Windows installer.

## Subsequent development, not yet a published release
Separate private development work has explored enhanced Dockview-style workspace layout and MapLibre/Three.js/Cesium multi-engine rendering. These items must pass native Windows acceptance and an explicit published release before they can be promoted to “available in Preview.” See [Roadmap](ROADMAP.md) and [Capabilities](docs/CAPABILITY_MATRIX.md).

**Terminology:** “Preview 3” is the channel/iteration, **1.0.2** is the published application version, and `v1.0.1-preview.3` is the historical Git tag.
