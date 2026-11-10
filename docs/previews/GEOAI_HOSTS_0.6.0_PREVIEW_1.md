# GeoTwins GeoAI QGIS, ArcGIS Pro and Python SDK 0.6.0 — Preview 1

**Published:** 9 November 2026, 17:33 UTC  
**Tag:** [geoai-hosts-v0.6.0-preview.1](https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.6.0-preview.1)  
**Status:** experimental evaluation packages. **Installed QGIS/ArcGIS Pro native acceptance pending.**  
**Recorded package source:** [756133f85b21e3e3a1cac3f6c2109683f983f72c](https://github.com/aerocorp13/world-twin-agents/commit/756133f85b21e3e3a1cac3f6c2109683f983f72c)

## What's included

Five named, publicly uploaded artifacts are recorded on GitHub:

| Asset | Purpose | Uploaded SHA-256 |
| --- | --- | --- |
| \`geotwins_geoai_qgis_0.6.0.zip\` | QGIS GeoAI dock/plugin | \`4b6acc3d582480e38c43205dda0c308e16e01b22b794408fce7044db4e199960\` |
| \`GeoTwins.GeoAI.ArcGISPro.esriAddInX\` | Native ArcGIS Pro .NET add-in | \`7e4d3fe68b44eebedf74b29bd9303b3dad94260f16b9f1f5e28ea2332db6c9b8\` |
| \`geotwins_geoai_arcgis_pro_0.6.0.zip\` | ArcGIS Pro Python companion/toolbox | \`b877e5b1d3a2d4bffe75a6d0061c24d4d3eb58f7020b6602c2951e756f37e0fb\` |
| \`geotwins_geoai_sdk-0.6.0-py3-none-any.whl\` | Python SDK wheel | \`242e9219e47b1c938b5dcd3ee9b605fe82eb4db760f04dec7d5d6c2dff1ad9ab\` |
| \`geotwins_geoai_python_sdk_0.6.0.zip\` | SDK source distribution | \`ecaece61e816a32d08b3eddd3e789a19a5e7004e8d8f855f4d7c58aeb73a7312\` |

All five GitHub assets have an uploaded digest. **An uploaded hash establishes asset identity, not model output quality or successful native execution.** This release does **not** contain an AGOT Desktop MSI or licensed Esri/QGIS installations.

## Changes since 0.5.0 — candidate functionality

The private source handoff for this exact package commit describes the following changes, which must be verified in actual installed hosts:

- **Native host planning and execution:** current-source QGIS Processing and ArcPy action registries, explicit primary/overlay selection, CRS and source fingerprints, previewed typed operation sequences, and new approval before source-changing GIS effects.
- **More useful operator controls:** in supported host builds, plan editing/replanning and a clearly distinguished operator-authored fallback when no working model is available. A model answer that only explains a workflow is **not** an executed plan.
- **Persistence and evidence:** refreshed active layer inventory; local execution reports with actual outputs/counts/checksums; attempts to surface host results in the original Ask/Results pane; a durable report/reconnect path that must not replay effects.
- **Model options and governance:** local Ollama/open-compatible model choices and optional explicitly consented cloud-provider adapters in source; actual availability depends on installed provider, exact model, credentials and compatibility. The SDK/MCP transport remains restricted to discovered registered capabilities and reviewed execution.
- **Host UI recovery:** source changes address green ArcGIS ribbon glyphs, chat Markdown formatting, map-ready source refresh and genuine ArcPy diagnostic messages. Installed add-in version and resource caching must still be checked on the user's workstation.

**No arbitrary LLM-generated Python, shell, SQL or direct unreviewed GIS mutations are authorized.** The public preview is not permission to bypass source owners' rights or to send data to a cloud model without consent.

## Evidence versus missing acceptance

The 0.6.0 public release reports **114 automated source/contract tests passed**. That is the publisher's recorded test claim; the present documentation update did **not** independently rerun the tests.

| Evidence category | Current state |
| --- | --- |
| Public ZIP, wheel, .esriAddInX assets and recorded GitHub hashes | **Published** |
| Source/contract test declaration | **114 reported passing in release body** |
| Installed QGIS 3.x/4.x selection → real model plan → human approval → Processing output → map + reopen | **Not native-verified here** |
| Licensed ArcGIS Pro 3.7 selection → model plan → ArcPy output → pinned results + reopen | **Not native-verified here** |
| No-model operator-authored execution, failure diagnosis, revised approval, reconnect with no double effect | **Field acceptance outstanding** |
| AGOT pairing and World → Simulation → Twin → 3D end-to-end | **Not certified** |
| Signing, commercial cloud provider credentials/model availability and real-data scientific validity | **Not certified** |

## Responsible installation and testing

Download from the official tagged release, verify SHA-256 and check compatibility before upgrading. QGIS plugin installation is performed from the local ZIP in the relevant QGIS plugin manager. ArcGIS Pro requires the appropriate installed SDK/host version and the native \`.esriAddInX\`; close the application and ensure older add-in resources are not being reused. Use an isolated environment for the wheel. These packages are evaluation builds, not verified marketplace packages or automatic in-app updates.

A meaningful first test is: open a real, authorized projected roads layer; choose the exact layer; ask *“Create a 50-metre buffer around these roads, intersect it with my approved project boundary, save the resulting layer and show it on the map.”* Inspect the proposed native plan and source selection, approve explicitly, then verify the created output geometry, features, CRS, saved dataset and visible Results/receipt after reopening. Repeat with an intentionally invalid source and confirm fail-closed, diagnosable behavior. Do not use sensitive project data when the selected model provider could transmit the question externally.

For compatibility and staged acceptance, see the [next 0.7.0 engineering roadmap](../roadmaps/AGOT_1.0.7_GEOAI_HOSTS_0.7.0_UX_RECOVERY.md) and [public quality limits](../QUALITY_AND_LIMITATIONS.md).

_The implementation details above summarize source-documented candidate capabilities at the package SHA. They are not assertions that every provider, licensed host, or workflow has passed installed tests._