# Capabilities — release evidence matrix

**Updated 5 November 2026.** AGOT 1.0.5 and GIS Host/SDK 0.3.0 are publicly available experimental prereleases, with verified GitHub binary assets and checksums. “Release-documented” and “source-implemented” do **not** certify all workflows on independent clean Windows machines or licensed GIS hosts.

## Latest experimental public preview matrix

| Capability | Published evidence | Remaining acceptance |
| --- | --- | --- |
| Windows AGOT 1.0.5 | MSI `v1.0.5-preview.1`, 1,408,242,136 bytes and SHA-256 | Clean installation/upgrade from 1.0.4, backend recovery, data restore and signed updater |
| Concept 6 desktop workspaces | Windows MSI/source integration line, typecheck and native build evidence | High-DPI, all GIS modules on real installed data and robust keyboard accessibility |
| GeoAI agent/workflow harness | Model capability policy and actual native tool-call readiness gating; reviewed GIS operations and saved receipts | Live model matrix, long-run job recovery, authorized workflow replay and no fabricated outputs |
| Worlds, Twin, Simulation and 3D | Versioned source/World/scene contracts and native runtime pathways in 1.0.5 line | City-scale tiles, CRS/vertical accuracy, real IFC/point clouds, calibrated scenarios and linked temporal worlds |
| QGIS and ArcGIS Pro GeoAI 0.3.0 | QGIS ZIP, ArcGIS Python toolbox ZIP and native .NET 10 .esriAddInX released with SHA-256 | Installed QGIS/ArcGIS Pro tests, licensing and vendor marketplace decisions |
| Standalone Python SDK 0.3.0 | Python wheel and portable source ZIP publicly released | Real host/model interoperability and Python dependency boundary validation |
| Website package refresh | Dynamic public GitHub release metadata, exact version, SHA-256 and asset URL | Website redeployment for the new UI; **not** automatic installed QGIS/ArcGIS upgrades |
| Linux/macOS desktop | Development/readiness scripts and 2027 roadmap only | Native runtime port, Linux/macOS builds, signing and independent installed acceptance |

Historical Preview 3 information follows for provenance.

| Capability | Public Preview 3 evidence | Practical boundary |
| --- | --- | --- |
| Windows x64 MSI | **Published** asset, product version 1.0.2 | Clean install/upgrade/uninstall, signing and restore still need separate acceptance |
| Core 2D workstation and map/layers | **Release-documented** local GIS + map workspace | Depends on valid source format, authorization and available service |
| GIS editing and derived vector processing | **Release-documented** reviewed, versioned operations | Only registered supported tools; not every ArcGIS/QGIS operation |
| Raster/imagery and terrain | **Release-documented** integrated pathways | Service/source-dependent; not universal ECW/remote/DEM compatibility |
| Versioned World history | **Release-documented** pinned reads, membership, fork/correction | Source grants rechecked; portability/offline policy propagation incomplete |
| GeoAI action harness | **Release-documented** plan/step, receipts, reviewed operations, retries | Not unrestricted autonomous actions; real provider and end-to-end native tests still needed |
| Local ONNX inference jobs | **Release-documented** queue/lease/input-output validation | Requires compatible user-supplied checkpoint; no validated production model included |
| 3D and twin viewing | **Partial/experimental in public preview** | Exact engine and asset type depend on build/source; no universal synchronized city-scale 3D |
| Scenario/simulation workflows | **Early/bounded implementations** | No claim of calibrated hazard or coupled simulation accuracy |
| Independent MapLibre / Three / Cesium views and advanced Dockview | **Development branch**, not established as Preview 3 native acceptance | Requires real Windows build and runtime/graphics validation |
| Third-party plugin installation | **Not established as supported** | Internal tool registries are not a public plugin marketplace |
| Auto-updating installed desktop copies | **Not established** | Website release discovery is different from app auto-update |
| Cross-world portal links / generated worlds / fully coupled solvers | **Roadmap** | No current production claim |
| Professionally certified survey/hydrological predictions | **Not claimed** | Calibration and domain review required |

**Evidence categories:** published installer; release-documented feature; tested in isolated development; native Windows tested; production/safety validated. These are not interchangeable.

## What the GeoAI workflow does—and does not—mean

Published Preview 3 describes persistent plans, step logs, bounded agent investigations, consent before GIS side effects and lineage of derived revisions. This can enable workflows such as inspect a vector layer → propose buffer → review → create derived revision → propose dissolve → review. Actual outcomes depend on data format, tools, permissions and backend health.

An AI plan alone does **not** prove local Ollama connectivity, remote API credentials, ONNX segmentation quality, zero-hallucination analysis, simulation calibration or reliable cancellation of long native calls.

## How to check a feature

1. Start with [release notes](../RELEASE_NOTES.md), not screenshots or concept art.
2. Confirm source, CRS, valid date, permissions, engine and required model.
3. Run on permitted test data, inspect resulting revision and logs.
4. Preserve error traces, input IDs and approvals; don't share private datasets publicly.
5. Verify persistence and re-open/upgrade behavior when the task depends on it.

For installation gates and diagnostics see [Quality and limitations](QUALITY_AND_LIMITATIONS.md). For intended scope see [Roadmap](../ROADMAP.md).
