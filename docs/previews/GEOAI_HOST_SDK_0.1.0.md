# GeoTwins GeoAI host SDK 0.1.0 — developer integration contract

**Website:** https://geotwins.org/sdks/ · **Packages:** https://geotwins.org/plugins/#packages

## Components
- **GIS host:** QGIS or licensed ArcGIS Pro retains real source geometry, attributes, map layouts and native geoprocessing.
- **Shared Python SDK:** agot_host_sdk.py, included with the QGIS ZIP and ArcGIS Python toolbox ZIP, handles bounded local AGOT requests, source fingerprinting and approved-plan exchange.
- **AGOT local service:** authenticates the operator and supplies schema-constrained planning, grant/approval and host-attested receipts.
- **Operator:** selects sources, reviews exact source SHA and all requested actions, consents to effects, and checks the outputs.

## Protocol and review
The proposed schema identity is **agot.geoai.host-plan/1**. The development service's plan API begins at **POST /api/v2/geoai/host-sdk/plans**, and planned approval/report flows use its associated per-plan approve/report endpoints. This is **not** an anonymous external public service or general MCP/A2A conformance.

1. Operator selects saved GIS project and rights-cleared feature classes; the host fingerprints geometry/attributes locally.
2. Only bounded source descriptions and the operator's question are provided to the local AGOT planning service; sensitive source feature bytes should remain in the host.
3. Proposed registered GIS actions are reviewed, including operations and source/plan hashes.
4. Operator gives explicit approval for the *exact* plan and data state; expired grants, changed inputs, unsupported CRS and unregistered tools must fail closed.
5. The GIS host executes only approved native actions, records local outputs, and reports a **host_attested_unverified** receipt. This is not scientific validation.

## Security and compatibility
- QGIS host bearer is session-held; ArcGIS Pro Python reads AGOT_HOST_TOKEN from the local process environment. Never save any bearer in a .aprx, log or public website.
- No private GIS attributes, tokens, model weights, proprietary Esri binaries or customer data are bundled with the packages.
- Use a local authenticated AGOT service and operator-owned source data; do not execute arbitrary model-generated Python, C#, SQL or shell.
- The SDK is preview 0.1.0 and requires matching service behavior. It was **not** independently installed and tested against all host versions.
- The desktop MSI and host packages are separate release channels.

[QGIS guide](QGIS_GEOAI_0.1.0.md) · [ArcGIS Python](ARCGIS_PRO_PYTHON_GEOAI_0.1.0.md) · [ArcGIS native](ARCGIS_PRO_NATIVE_GEOAI_0.1.0.md)
