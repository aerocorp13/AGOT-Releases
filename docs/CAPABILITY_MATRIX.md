# Capabilities — release evidence matrix

**As of 3 November 2026.** “Documented in Preview 3” means described in its published notes; it does **not** certify all workflows on an independent clean Windows machine.

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
