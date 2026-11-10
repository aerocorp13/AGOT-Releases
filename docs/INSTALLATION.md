# Install and evaluate the current AGOT public previews

**Updated 10 November 2026.** Current distribution channels are **experimental**, not stable or certified for production. This guide covers **AGOT Desktop 1.0.6 Preview 2** and the **independently versioned GeoAI QGIS / ArcGIS Pro / Python SDK 0.6.0 Preview 1**. They are separate downloads. Neither a GitHub release nor an updated GeoTwins website automatically upgrades an installed desktop, QGIS plugin or ArcGIS Pro add-in.

## 1. Choose the correct published release

| Product | Public release | Files to use |
| --- | --- | --- |
| AGOT Desktop Windows x64 | [v1.0.6-preview.2](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.6-preview.2) | `AGOT.Desktop_1.0.6_x64_en-US.msi`, `SHA256SUMS.txt`, `release-evidence.json` |
| GeoAI GIS hosts and Python SDK | [geoai-hosts-v0.6.0-preview.1](https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.6.0-preview.1) | QGIS ZIP, ArcGIS Pro .NET `.esriAddInX`, ArcGIS Pro Python companion ZIP, Python SDK wheel and source ZIP |

The Desktop installer was recorded from source `9a0aa8b41cb7b7339a72296fdd9f6a48374ca77d`; the later Host SDK packages were recorded from `756133f85b21e3e3a1cac3f6c2109683f983f72c`. **They are not the same build**, and private development after either source commit is not part of that artifact.

A separate `v1.0.6-preview.1` entry may appear in repository release APIs as a **draft with no downloadable assets**; do not mistake it for the current published installer.

## 2. Verify downloaded bytes and trust independently

The public 1.0.6 Preview 2 MSI has recorded size **1,416,188,896 bytes** and SHA-256:

`59ae2b13f2bddfb7cff5abea1fa090814b572eeeb87fd38bf20211a6182f4df3`

Open **PowerShell 7** in the folder containing the downloaded installer:

```powershell
Get-FileHash -LiteralPath ".\AGOT.Desktop_1.0.6_x64_en-US.msi" -Algorithm SHA256
Get-AuthenticodeSignature -FilePath ".\AGOT.Desktop_1.0.6_x64_en-US.msi" |
  Format-List Status, SignerCertificate, StatusMessage
```

Confirm the complete hash matches the value above; compare the release's `SHA256SUMS.txt` and `release-evidence.json` where provided. **At recorded publication the MSI was NotSigned**; matching a hash is not a code signature, and the installer has not received independent clean-machine acceptance here. Never disregard an unexpected signer, installer source or changed checksum.

For host assets, consult the [five individually recorded 0.6.0 hashes](previews/GEOAI_HOSTS_0.6.0_PREVIEW_1.md). You can hash a downloaded ZIP, wheel or `.esriAddInX` by replacing the filename above.

## 3. AGOT Desktop: install, first run and upgrade

1. Back up project data and existing workspaces **before** experimenting. The historical default path documented by earlier previews is `%APPDATA%\af.agot.desktop\runtime-v1`; configured overrides may differ. Confirm your actual workspace path before copying or cleaning anything.
2. Close the previous AGOT Desktop and background host processes; use the published Windows x64 MSI, not a GitHub auto-generated source ZIP.
3. Windows 11 x64 and Microsoft Edge **WebView2 Runtime** are the primary target environment. Backend/PostGIS service readiness, disk space and optional basemap internet access depend on the chosen features. LLM weights, API keys and licensed vendor GIS installations are **not** bundled.
4. Launch and check the exact installed version, local service readiness and project access. Open a *non-sensitive* test GeoJSON/GeoPackage with known CRS, add a real layer and verify the map/attributes. Test native processing only after ensuring sources and engine permissions are valid.
5. Before upgrading a previous preview, record original version, project IDs, output locations and copies of user data. After installation, reopen the same project and validate layer counts, source IDs, map layout and any saved GIS receipts. Do not assume migration or upgrades are certified.
6. Treat Worlds, Simulation, Twin, 3D, GPU processing and GeoAI as **capability-specific experimental paths**; a visible tab or local provider status is not evidence of a correct saved scientific result.

No signed stable auto-update channel is asserted by these preview uploads.

## 4. QGIS 0.6.0: manual plugin installation

Download `geotwins_geoai_qgis_0.6.0.zip` from the tagged **host** release, verify its hash, and inspect the contained license/metadata. Open a compatible installed QGIS version, then use **Plugins → Manage and Install Plugins → Install from ZIP** and select the official ZIP. Depending on QGIS version, menu wording can differ. Restart QGIS, confirm the loaded plugin reports the intended version, and verify the dock/panel and native Processing provider presence.

For a real source-to-output check, load a licensed projected roads dataset, choose the exact source, propose a 50-metre buffer, inspect the plan and CRS, approve the GIS effect explicitly, run it and reopen the resulting layer. Verify geometry, feature count, output path and processing receipt. If using a model, configure a compatible local model service separately and check a genuine tool-call response; otherwise use only supported manual operations. This release is **not** a certified official QGIS Plugin Directory installation or automatic upgrade. Native QGIS installed-host testing remains open.

## 5. ArcGIS Pro 0.6.0: native add-in and Python toolbox

On a licensed, compatible Windows ArcGIS Pro installation, download and hash **`GeoTwins.GeoAI.ArcGISPro.esriAddInX`** for the native .NET add-in. The separate `geotwins_geoai_arcgis_pro_0.6.0.zip` is the Python companion/toolbox package; it is **not** a renamed `.esriAddInX`. Close ArcGIS Pro before changing add-in versions; install according to ArcGIS Pro's add-in trust/extension prompts, reopen and check version/toolbar resources. Native API, SDK/.NET compatibility and installation trust must be checked against the actual installed ArcGIS Pro version.

Use authorized feature classes and run one reviewed ArcPy-based operation with exact input and output names. Verify native geoprocessing result, layer addition, approval, receipt and reopen in the GeoAI dock. An explanation in chat or geoprocessing history **without an actual saved output and its original pinned result** is not success. Do not treat old cached ribbon icons as proof that the current package loaded.

## 6. Python SDK wheel 0.6.0

Download `geotwins_geoai_sdk-0.6.0-py3-none-any.whl` to an isolated Python virtual environment. Confirm its checksum against the host release guide, then install the exact local wheel:

```powershell
py -3.12 -m venv .venv-geotwins-eval
.\.venv-geotwins-eval\Scripts\python.exe -m pip install ".\geotwins_geoai_sdk-0.6.0-py3-none-any.whl"
```

The `geotwins_geoai_python_sdk_0.6.0.zip` is a source archive for inspection and development, not a substitute for the installable wheel. The SDK does not supply ArcGIS Pro, QGIS, a GPU runtime, models, cloud credentials or the AGOT Desktop MSI. Model-provider/MCP integration should be tested only with registered, authorized GIS capabilities and explicit external-data consent.

## 7. Troubleshooting and honest support reports

Record the product/version/tag, downloaded asset SHA-256, OS and exact QGIS/ArcGIS version, local model provider, selected authorized source and CRS, proposed operation, operator grant, native error and whether a **real saved result** exists after reopening. Do not include secrets, access tokens or protected project data in public issues.

- [Desktop 1.0.6 detailed changes / known issues](previews/AGOT_DESKTOP_1.0.6_PREVIEW_2.md)
- [Host/SDK 0.6.0 changes / hashes / limitations](previews/GEOAI_HOSTS_0.6.0_PREVIEW_1.md)
- [Release evidence and limitations matrix](CAPABILITY_MATRIX.md)
- [1.0.7 / 0.7.0 UX and native reliability roadmap](roadmaps/AGOT_1.0.7_GEOAI_HOSTS_0.7.0_UX_RECOVERY.md)
- [10 November source UI audit](roadmaps/AGOT_1.0.7_0.7.0_SOURCE_UI_AUDIT_20261110.md)
- [Historical Preview 3](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3) (product version 1.0.2, legacy tag naming)

Contact [admin@geotwins.org](mailto:admin@geotwins.org) or use [GitHub Issues](https://github.com/aerocorp13/AGOT-Releases/issues). For security disclosure use [SECURITY.md](../SECURITY.md).
