# Changelog

Public Windows preview timeline, most recent first. This log is historical, not a list of unsupported future claims. All dates are UTC.

## 2026-11-05 — AGOT Desktop 1.0.5 and GIS Hosts/SDK 0.3.0 compiled candidates

- **Built, upload still pending at this snapshot:** native Windows x64 Desktop 1.0.5 MSI (1,408,242,136 bytes) from source `64452231cabee5d1e6b6124923c25d1b2d5ebea9`. The `v1.0.5-preview.1` GitHub record was a draft with zero assets at inspection. [Detailed candidate notes](docs/previews/AGOT_DESKTOP_1.0.5_PREVIEW_1.md).
- **GIS Hosts and SDK v0.3.0 compiled:** ArcGIS Pro 3.7 .NET 10 add-in, ArcGIS Python toolbox, QGIS plugin ZIP, standalone Python SDK source ZIP and wheel. The `geoai-hosts-v0.3.0-preview.1` record was also a draft with zero assets. [Host notes](docs/previews/GEOAI_HOSTS_0.3.0_PREVIEW_1.md).
- **Source/build advances:** workstation Concept 6 module integration, authenticated GIS and GeoAI state, model verification and source-scoped jobs, optional standalone GIS host workflows and reviewed local Ollama planning. Not all functions are certified by an installed-host run.
- **Publication fix:** the 1.31 GiB MSI upload failed using Python's file-object HTTP request. A numeric-release-ID Windows PowerShell `Invoke-RestMethod -InFile` helper was added, preserving original binary SHA-256 manifests, resumable draft state and public-only-after-verification behavior.
- **Remaining gates:** upload and verify all assets, confirm both public prereleases, run clean Windows upgrade and actual licensed GIS/model acceptance. [Checksums and required gates](docs/previews/RELEASE_1.0.5_0.3.0_PUBLICATION_CHECKLIST.md).

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
