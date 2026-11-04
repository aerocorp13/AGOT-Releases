# QGIS — GeoTwins GeoAI plugin preview 0.1.0

**Package:** geotwins_geoai_qgis_0.1.0.zip (15,426 bytes)  
**SHA-256:** 8946a7de5050449d5abc471af7c8bfb3230c3b9fb40aec0a052563ac5d423ce1  
**Release:** https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.1.0-preview.1  
**Portal:** https://geotwins.org/plugins/#packages

## Function
Development implementation of a QGIS Python plugin (folder geotwins_geoai) with plugin metadata, dock controls, engine, Processing provider, bundled stdlib-only local AGOT host SDK and source SHA verification. It connects an authorized QGIS project to an operator-approved GIS plan proposed by a separate locally running AGOT service. It does not install a model, create a public cloud service or execute arbitrary model-generated Python.

## Install and first test
1. Use a compatible QGIS 3.x build (development tested against the QGIS 3.44 toolchain), local AGOT service and operator-owned/authorized vector layers.
2. Download the ZIP from the **published** GitHub release and check its SHA-256.
3. In QGIS go to Plugins → Manage and Install Plugins → Install from ZIP and select the original archive.
4. Verify the GeoTwins dock and Processing provider actually appear. Configure the AGOT bearer in the dock for the current session, not a saved project.
5. Choose authorized vector layers with known EPSG/CRS and save the source state. Request a structured plan, review exact source SHA, registered tools, parameters and outputs.
6. Explicitly approve and execute against test layers only; compare resulting geometry, map layout and reported feature counts with independent QGIS ground truth. Test invalid SHA, revocation and interrupted workflow.

## Distribution and licensing
**Important:** The ZIP as built contains a development/evaluation-only LICENSE that does not grant downstream redistribution. Its publisher is offering an experimental test build, not relicensing third-party uses. **Do not mirror, repackage or submit the current ZIP to official QGIS plugins without a new, deliberately chosen GPL-compatible licence and publicly available corresponding plugin source.** The release repository's MIT licence covers its own distributed documentation, not this plugin archive. The official QGIS plugin catalogue has separate GPL-compatibility and public source requirements.

## Limits
The QGIS plugin was packaged, but installed host behavior, real data/CRS correctness, model connectivity, controlled failure handling and scientific use were **not** certified. A host-reported outcome is not an independently verified geospatial measurement.

[Host SDK](GEOAI_HOST_SDK_0.1.0.md) · [Acceptance](PREVIEW_ACCEPTANCE_20261105.md) · [Security](../../SECURITY.md)
