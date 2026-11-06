# GeoTwins GeoAI Hosts and Python SDK 0.4.0 — experimental public preview

**Published:** 6 November 2026 (UTC). **Release:** [geoai-hosts-v0.4.0-preview.1](https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.4.0-preview.1). **Channel:** public prerelease, not stable.

**Exact source revision:** edb47c82c05179c808ea5f07bf631947a83484e3 in the world-twin-agents integration branch, [draft PR #21](https://github.com/aerocorp13/world-twin-agents/pull/21). The release is separate from AGOT Desktop. **No MSI is included, and AGOT v1.0.6 remains in development.**

## What changed from 0.3.0

- **Durable host-independent GeoAI Core:** SQLite jobs, immutable source-bound model plans, operator approval digests, cancellation, crash recovery and real output receipts.
- **Local model adapters:** Ollama plus localhost OpenAI-compatible llama.cpp, vLLM and MLX adapters. Registered provider protocols do not establish all real installed-model capabilities.
- **Real GIS output engine:** Fiona/Shapely/pyproj processing of authorized vector resources with SHA-256 source pins, metric-CRS checks, validated GeoPackage outputs and no-overwrite behavior.
- **Typed GIS tool contracts:** semantic operations and QGIS/ArcGIS native tool symbol mappings, separate from live host availability.
- **Local control plane:** authenticated loopback API, typed Python client, private token, verified local service identity and dynamic port discovery.
- **Independent packaging:** QGIS plugin, ArcGIS Pro Python toolbox, genuine .NET 10/ArcGIS Pro 3.7 add-in, Python SDK source ZIP and wheel. No desktop build required.

## Published assets and hashes

| Asset | Bytes | SHA-256 |
| --- | ---: | --- |
| geotwins_geoai_sdk-0.4.0-py3-none-any.whl | 36,334 | 5f652b44b364f797273cb2409a2f36ea1479fc5ed75b535bb19639c0e7c2494b |
| geotwins_geoai_python_sdk_0.4.0.zip | 37,388 | e6ece54572a1bc55dea25b307cdc47f48e03dda5695e87b61aa183d54d3adedc |
| geotwins_geoai_qgis_0.4.0.zip | 52,815 | 032fcc69be6c19577407638a767ba1defa8019c71d966474928d7dee2109bc04 |
| geotwins_geoai_arcgis_pro_0.4.0.zip | 47,394 | 7601a80e9cf93efa596ec8d58654807fd5990106367f1d4ddcedc2f6ac3722f0 |
| GeoTwins.GeoAI.ArcGISPro.esriAddInX | 47,179 | 34e258414936069fdd9484865c3e5312726c8ce8164e2be1247c66d770824e0a |

The release also contains RELEASE_NOTES.md, SHA256SUMS.txt and release-evidence.json. GitHub digests verify publication bytes; they do not certify Windows code signing, live GIS host compatibility, quality of AI inference or scientific calibration.

## Installation

**QGIS:** Install the QGIS ZIP through Plugins → Manage and Install Plugins → Install from ZIP. Verify compatible QGIS, selected vector layers, CRS and permissions. Local inference requires a separately installed compatible, tool-capable local model.

**ArcGIS Python toolbox:** Extract the ZIP keeping GeoTwinsGeoAI.pyt next to its SDK modules. Add the Python toolbox through ArcGIS Pro Catalog. Native ArcGIS tools execute under licensed Esri's managed Python environment; do not modify that environment merely to install the separate portable SDK.

**ArcGIS native add-in:** Install the authentic compiled .esriAddinX in supported ArcGIS Pro 3.7 with .NET 10. Independently verify actual dockpane startup, selected layers, tool calls and result receipts.

**Standalone Python SDK:** Install the wheel in an isolated compatible Python environment. Portable vector GIS needs host-specific Fiona, GEOS/Shapely and pyproj/GDAL binary dependencies. No proprietary GIS runtime, model weights or credentials are redistributed.

## Evidence and important open gates

The owner reported **35 passing Python 3.12 portable/SDK regression tests** before publication. The build and public asset inventory were checksum-checked. These tests exercise simulated local model transport to **real vector GeoPackage operations**; they do not certify live Ollama/QGIS/ArcGIS behavior.

The previously observed 0.3.0 model-discovery and selected-layer problems were subjects of source repairs, but no full installed-host acceptance is claimed for the new preview. Check local inference inventory, host layer binding, approval and real processing in each installed GIS environment.

**Still open:** native host-to-shared-Core delegation; complete AGOT PostGIS/World orchestration reconciliation; provider parity; raster/EO/3D agent tools; MCP/A2A adapter acceptance; signed platform updates; generalized simulation/scientific validation. Linux and macOS desktop builds target 2027 and have not shipped.

**Web portal:** https://geotwins.org/plugins/ and https://geotwins.org/technology/.
