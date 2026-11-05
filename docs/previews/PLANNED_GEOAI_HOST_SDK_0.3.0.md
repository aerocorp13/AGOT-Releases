<!-- Source specification only. No MSI, add-in or public 1.0.5/0.3.0 release has yet been uploaded by this docs commit. -->

**STATUS: SOURCE IMPLEMENTED, BINARIES NOT YET PUBLISHED.** The Windows owner build and real GIS host acceptance are required before the tags/downloads can go live.

# GeoTwins Africa GIS Hosts + Python SDK 0.3.0 — Preview 1 source specification

**Planned public GitHub prerelease:** geoai-hosts-v0.3.0-preview.1 (or the next available numbered preview at publishing). **Not a stable release.** Binaries are not published by this source document; the owner Windows build/publisher supplies real artifacts first.

## New standalone architecture

GeoTwins GIS hosts now support **two different independently installable modes**, and an optional third AGOT integration:

| Mode | ArcGIS Pro 3.7 (.NET 10 + licensed ArcPy) | QGIS 3.44 (PyQGIS) | AGOT Desktop requirement |
|---|---|---|---|
| Native GIS | inspect real source; reviewed projected-metre Buffer creates new feature class | inspect real source; reviewed native Processing buffer creates derived temporary layer | **None**, and no local LLM |
| Standalone local GeoAI | Python toolbox generates and runs SHA-reviewed local Ollama operation plans, ArcGIS dockpane opens tools | QGIS Standalone AI tab uses a background model planner, explicit reviewed execution and local receipts | **None**, but local tool-capable Ollama runtime required |
| Connected AGOT GeoAI | optional server pairing, agent plan and host attestation | optional pairing, AGOT-managed plan and audit | A **matching running AGOT service**, not necessarily the UI window |

Standalone local model runtime is one standard-library Python module, independent of FastAPI/PostGIS/Tauri. Only an operator-supplied question and a source metadata receipt are sent to the explicitly validated local Ollama loopback service; feature geometry, field values, file paths, bearer tokens and source dataset bytes are not sent by the client.

Allowed model operations: buffer_m, dissolve, convex_hull, multipart_to_singlepart, clip, select_intersects, intersection, union_polygons and difference, bounded by source CRS/geometry and overlay availability. Plans are limited to five operations; metric buffers require a projected metre CRS; inputs are hash-frozen to actual full WKB+attribute content; output is never claimed executed before a separate human confirmation. No model-generated Python, shell, SQL, file path or executable payload runs.

The local Ollama planner requires a **real native function-tool call and a second round-trip that demonstrates receipt consumption**. Invalid schemas, unknown tool names, redirects, non-loopback endpoints, untethered overlays, changed source SHA, missing model support and unapproved operations fail closed. Local receipt files attest native host execution; they do **not** certify numerical GIS accuracy.

**Stand-alone AI is not equivalent to AGOT Worlds.** This preview does not implement independent cross-world simulations, TerraTorch/Prithvi model servers, distributed remote inference or AGOT's PostGIS/worker provenance outside AGOT.

## Actual distribution artifacts produced by owner build

- GeoTwins.GeoAI.ArcGISPro.esriAddInX — compiled genuine Esri SDK add-in, .NET 10, Windows/Pro 3.7 only
- geotwins_geoai_arcgis_pro_0.3.0.zip — Python toolbox, local AI runtime and shared host client
- geotwins_geoai_qgis_0.3.0.zip — QGIS install-from-ZIP plugin, local AI runtime and native Processing adapter
- geotwins_geoai_python_sdk_0.3.0.zip — portable Python SDK source and notice
- geotwins_geoai_sdk-0.3.0-py3-none-any.whl — deterministic standalone SDK wheel for Python >=3.11
- SHA256SUMS.txt and release-evidence.json — exact binary hashes and originating development SHA

Neither ArcGIS/QGIS executable binaries, model weights, paid model API credentials nor Ollama itself are bundled. The .NET 10 runtime is installed as a supported ArcGIS Pro prerequisite; a .NET10 Esri add-in is **not advertised as backward-compatible with Pro 3.6**.

## Build and actual installed tests

Run the one-command build/publisher documented in RELEASE_PIPELINE_1.0.5_0.3.0.md. Before any field acceptance, verify:

1. Python package/source syntax, deterministic wheel hashes and explicit SDK version identity.
2. Esri add-in produced with real VS2026/MSBuild SDK targets, correct Config.daml and compiled DLL; do not rename ZIP.
3. Install the QGIS ZIP, open its Standalone AI dock and test a **real selected projected-metre vector**, including a native model call, human SHA review, no AGOT running, actual output and local receipt.
4. Install ArcGIS Pro 3.7 add-in and local .pyt companion, use the same real source-bound workflow with AGOT completely closed, verify exact output and new feature class in ArcGIS Contents.
5. Restart the hosts; reopen local receipts. Test changed-source rejection, failure paths and no source overwrites.
6. For optional connected mode, open matching AGOT Desktop, pair, run a separately approved source-bound plan and verify AGOT database receipts.
7. Check Windows DLL packaging, any missing Python dependencies, model memory pressure, GPU concurrency and UI responsiveness with actual installed hosts.

Until actual licensed-host test evidence is attached, only the **source implementation** and **package-build** state are claimed.

## Licensing decision still required

The current QGIS plugin source contains an owner-evaluation/non-redistribution notice. Publishing an evaluation ZIP **by its copyright holder** does not automatically grant everyone the right to redistribute it. Official QGIS Plugin Directory submission requires an explicit GPLv2-or-later-compatible license and public source repository. No automatic relicensing is authorized by this script; do not claim official QGIS approval.

## Reference

- Esri ArcGIS Pro 3.7 API SDK (.NET 10): https://doc.esri.com/en/arcgis-pro/latest/sdk/api-reference/conceptdocs/docs/Home.html
- Esri .NET 10 migration: https://doc.esri.com/en/arcgis-pro/latest/sdk/api-reference/conceptdocs/docs/ProGuide-NET-10-Upgrade.html
- QGIS plugin publication licensing: https://plugins.qgis.org/docs/publish
- GeoTwins Africa: https://geotwins.org
