# ArcGIS Pro — GeoTwins GeoAI Python toolbox preview 0.1.0

**Package:** geotwins_geoai_arcgis_pro_0.1.0.zip (12,376 bytes)  
**SHA-256:** bfee6d37e2b18a2849bbe42378ebd76f8d40a14fc54e9131007c609d61fa5007  
**Release:** https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.1.0-preview.1

## Contents
GeoTwinsGeoAI.pyt, agot_host_sdk.py and package README. This is a genuine ArcGIS Pro Python toolbox, **not** the native .NET Esri add-in. It proposes a bounded JSON GIS plan, then separately executes the human-approved plan with ArcPy and host-local data; the LLM does not supply runnable ArcPy code.

## Evaluation installation
1. Have properly licensed ArcGIS Pro (development targeted version 3.7), a configured local AGOT backend and local model, an authorized saved .aprx, test feature classes and a writable output workspace.
2. Download the archive from the published GitHub prerelease and verify the complete SHA-256 shown above.
3. Extract to a folder you control. Keep GeoTwinsGeoAI.pyt alongside agot_host_sdk.py.
4. Provide the local bearer using the **process environment variable AGOT_HOST_TOKEN** before ArcGIS Pro launches. Never enter it into geoprocessing tool parameters, saved project history or public logs.
5. In ArcGIS Pro use Catalog → Toolboxes → Add Toolbox, selecting GeoTwinsGeoAI.pyt.
6. Invoke the propose/review tool, examine plan operations, exact source/plan SHA and scopes. Use the separate approved-execute tool with explicit consent and the exact SHA.
7. Check feature geometry and CRS, map/layout exports, source drift rejection, GP tool history and saved .aprx restoration.

## Limits
The ZIP does not contain Esri licensing, proprietary ArcGIS binaries, an AGOT service or model weights. Packaging and Python syntax alone do not confirm actual native execution, source rights, numerical GIS correctness or interoperability. A host-reported receipt is not independent AGOT recomputation.

[Shared SDK](GEOAI_HOST_SDK_0.1.0.md) · [Native ArcGIS add-in](ARCGIS_PRO_NATIVE_GEOAI_0.1.0.md) · [Acceptance](PREVIEW_ACCEPTANCE_20261105.md)
