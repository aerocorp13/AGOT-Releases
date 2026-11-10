# GeoTwins Africa — AGOT Desktop 1.0.7–1.0.8 and GeoAI Hosts/SDK 0.7.0–0.8.0

**Developer-facing public roadmap · 10 November 2026 · proposed, NOT released.** This summary is intended for collaborators and customers assessing the next milestones. The authoritative detailed implementation plans and live evidence ledger reside in the private `world-twin-agents` integration branch (PR #21); their existence does **not** grant public access or establish a source license. This publication does not contain real customer datasets or code.

## Current verified publication vs engineering candidates

| Product | Current public experimental baseline | Next engineering targets |
|---|---|---|
| AGOT Desktop | Windows 1.0.6 Preview 2 ([release](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.6-preview.2)); Preview 3 documentation candidate, MSI not verified in this brief | 1.0.7 completion and reliability; 1.0.8 professional expansion |
| QGIS, ArcGIS Pro, Python SDK | 0.6.0 Preview 1 ([release](https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.6.0-preview.1)) | 0.7.0 true native plan→execute→result; 0.8.0 interoperable workflows and plugins |
| MCP and optional Harness | Source integration under development, separate native acceptance needed | 0.7.0 restricted transport and trusted grants; 0.8.0 MCP/A2A interoperability, bounded Creator review |

The 1.0.6 Preview 3 candidate improves public profile isolation and removes extraneous bundled pgAdmin dependencies before privacy scanning. **Its public MSI remains distinct from this roadmap**, and it must pass its own native Windows build/evidence process. A public GitHub release asset is not the same as an installed and accepted QGIS/ArcGIS plugin.

## Why 1.0.7 matters — finished professional tasks, not additional dashboards

AGOT's purpose is a professional geospatial workstation usable by engineers, urban planners, surveyors, environmental teams and non-GIS specialists, with powerful manual GIS controls for experts.

**1.0.7 should provide:**
1. **Working project and data continuity:** start/open/import project, inspect source and CRS/units, work in Map/Edit/Analysis/Imagery, save/reopen outputs without losing privileges, layers or window state.
2. **One quiet Home and one dockable Ask GeoAI:** a plain-language prompt beside the real project map, clear supported task shortcuts, no duplicated chat or diagnostics overload. Guided and Professional use exactly the same GIS operations.
3. **Real geoprocessing completion:** source→typed buffer/intersection/clip/measure→actual native/registered operation→verified output GPKG/feature count/digest→visible map and Results→export and reopen. Do not represent a planned command as an executed result.
4. **Reliable GeoAI:** real available local or optional provider, inspectable plan/parameters, human authorization, bounded failure diagnosis and fresh approval for changed effects, persistent result with no duplicate tool executions after a crash.
5. **Integrated Worlds / Simulation / Twin / 3D:** use actual versioned dataset and World, explicit scenario, supported numerical study, source-linked scene and independent real 3D renderer test. Uncalibrated scientific results must be labeled experimental.
6. **Install/serviceability:** clean user-isolated PostgreSQL/PostGIS, safe MSI upgrade, privacy protections, backup/recovery, readable UI at common DPI/keyboard settings, honest supported capabilities and comprehensive release evidence.

**The release gate** covers source+TypeScript/Rust, disposable database processing, real QGIS and licensed ArcGIS workflows, installed Windows MSI and 1.0.6→1.0.7 upgrade, output/raster/3D evidence, accessibility and publication digests. Passing source tests alone is insufficient.

## Why 1.0.8 should be materially bigger

1. **Professional GIS model-building:** reproducible multi-step processing recipes, batch runs, topology/advanced editing, outputs with full lineage, original inputs unchanged.
2. **Large and diverse geospatial data:** streaming indexed features, COG/STAC catalogs and georeferenced imagery, optional point clouds (PDAL LAS/LAZ/COPC), road networks (OSMnx), explicit offline datasets; measure performance instead of advertising assumed speed.
3. **Engineering 3D/BIM:** trustworthy IFC/CityJSON and terrain alignment, semantic object identities, quantities/clearances/clashes with stated tolerances, canonical scenes in MapLibre/Three/Cesium, documented GPU budgets.
4. **Validated simulation and comparison:** reproducible studies, supported environmental/engineering models, external benchmark for suitable drainage workloads, clear distinction between exploratory and calibrated/validated results.
5. **Local / private / hybrid deployments:** voluntary cloud services, permission-scoped collaboration, safe on-prem endpoints, admin backup/restore, explicit cloud data transfer consent and no reliance on expensive model hardware.
6. **Documentation, update and interoperability:** professional maps and evidence exports, SDK/plugin lifecycle and supported APIs; explore Linux/macOS only when respective native dependencies and installer acceptance exist.

## Native GeoAI Hosts, Python SDK and plugin work

| Target | 0.7.0 must pass | 0.8.0 expands |
|---|---|---|
| **QGIS** | Real Processing provider discovery, plan/approve/execute, persisted GeoPackage, dockable branded panel, restart and host result return | Visual multi-step models, batches, signed/permission-aware plugin ecosystem and robust upgrades |
| **ArcGIS Pro** | Genuine Esri tool execution and GP error messages, `.esriAddInX` DockPane, actual file geodatabase outputs, source checks and pinned result | Advanced recipe interoperability, multi-step workflows and versioned SDK contracts |
| **Portable Python SDK** | Independent pip-installable typed SDK and examples, standalone GIS operation without AGOT, canonical receipt and error types | Stable externally consumable SDK, schema-version negotiation and additional language clients if demanded |
| **MCP** | Standard official tool/resource discovery and typed output, separate one-use approval for native effects, deny arbitrary shell/Python/SQL | Adopt latest compatible protocol semantics and optionally A2A 1.0 for agent-to-agent task delegation, never bypassing AGOT authority |
| **Harness / local AI** | Local small model planning with provider health, optional cloud/on-prem only with consent, durable session and failure recovery | Reviewed Creator/Cordis extension lifecycle, private model routing, specialist planning and sandboxed opt-in plugins |

**No mandatory 24 GB GPU.** Target a working local profile on ordinary 8 GB RTX 4060-class machines with modest model sizes and explicit fallback. Full simulation and 3D rendering may have distinct resource/performance limits.

## A real example, shared across products

A planner imports a georeferenced road layer and schools. They ask *“Which roads are within 100 metres of schools?”* AGOT checks actual sources/units, proposes buffer and intersection, asks for review/approval, executes through its registered GIS engine or explicitly paired native host, saves a genuine GeoPackage output, shows it on the map and Results, and reopens it after restart. QGIS and ArcGIS versions must work independently without the main desktop running; optional connection only adds a common approved mission and artifacts. If source, CRS or model is missing, the product explains the missing prerequisite.

A second reproducible mission links an accepted dataset to a versioned World, forks a scenario, runs a supported numerical study with qualified scientific language, creates a source-backed Twin scene and verifies rendering on actual hardware.

## Developer release rule and evidence labels

Each work package must show **implementation → executed source/unit test → integrated real output → installed native check (where relevant) → exact public artifact**. Keep the logs, hashes, source revision and existing known issues. An AI response, a mock test, a new ribbon tab, a downloaded file or a green website badge is **not** equivalent to native operation or scientifically valid output.

Before release, demonstrate source identity, user and data permission safety, independently reopened artifacts and installation, failure/restart/permission-revoke behavior, version-compatible upgrades, supported model/provider selection, release notes and SHA256 inventories. SDK/host releases are separately versioned from Desktop. An updater must be genuinely signed; unsigned evaluation installers must not be advertised as signed automatic updates.

## Proven upstream projects to adopt rather than rebuild

- Official [QGIS Processing plugin framework](https://doc.qgis.org/3.44/en/docs/pyqgis_developer_cookbook/processing.html) for QGIS-native operations.
- Official [ArcGIS Pro 3.7 Geoprocessing SDK](https://doc.esri.com/en/arcgis-pro/latest/sdk/api-reference/conceptdocs/docs/ProConcepts-Geoprocessing.html) for licensed Pro-native tasks.
- [GDAL/OGR](https://gdal.org/en/stable/programs/ogr2ogr.html) for source transformation/reprojection; [IfcOpenShell](https://docs.ifcopenshell.org/ifcopenshell-python/geometry_processing.html) for BIM geometry.
- [MCP 2026-07-28 specification release](https://blog.modelcontextprotocol.io/posts/2026-07-28/), [A2A specification](https://github.com/a2aproject/A2A/blob/main/docs/specification.md) and [Pydantic AI toolsets](https://pydantic.dev/docs/ai/tools-toolsets/toolsets/) as integration candidates, not presumed deployed capabilities.
- [Tauri 2 Windows distribution](https://v2.tauri.app/distribute/windows-installer/) and [signed updater](https://v2.tauri.app/plugin/updater/) for future authenticated installed updates.

## Related existing public docs

- [1.0.7 UX recovery roadmap](AGOT_1.0.7_GEOAI_HOSTS_0.7.0_UX_RECOVERY.md)
- [1.0.7 source UX audit and acceptance boundaries](AGOT_1.0.7_0.7.0_SOURCE_UI_AUDIT_20261110.md)
- [Current Desktop 1.0.6 Preview 3 candidate changelog](../previews/AGOT_DESKTOP_1.0.6_PREVIEW_3.md)

**This document is a development plan, not a promise of delivery date, certified engineering/survey outputs or completed Windows/host builds.**
