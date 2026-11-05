# Experimental AGOT distribution channels — 5 November 2026

**Source-built, not yet public:** Desktop 1.0.5 and GIS Hosts / SDK 0.3.0 were compiled, but their new GitHub release records were **drafts with zero uploaded assets** at the 5 November inspection. Do not advertise them as downloadable until every binary and checksum is verified and both drafts become public prereleases.

| New candidate | GitHub tag | Status at inspection | Required deliverables |
| --- | --- | --- | --- |
| AGOT Desktop 1.0.5 | `v1.0.5-preview.1` | Draft; zero assets | 1.0.5 MSI, evidence JSON, SHA256SUMS |
| GIS Hosts / SDK 0.3.0 | `geoai-hosts-v0.3.0-preview.1` | Draft; zero assets | native .esriAddInX, ArcGIS toolbox ZIP, QGIS ZIP, SDK source ZIP, SDK wheel, evidence JSON, SHA256SUMS |

[Desktop 1.0.5 notes](AGOT_DESKTOP_1.0.5_PREVIEW_1.md) · [Hosts/SDK 0.3.0 notes](GEOAI_HOSTS_0.3.0_PREVIEW_1.md) · [Release checklist](RELEASE_1.0.5_0.3.0_PUBLICATION_CHECKLIST.md).

The older 1.0.4 / 0.1.0 prereleases below remain publicly available. No preview is a signed stable automatic-update feed.

## Separate release channels
| Channel | GitHub tag | Assets | Promotion rule |
| --- | --- | --- | --- |
| Windows desktop evaluation | v1.0.4-preview.1 | Windows MSI and SHA256SUMS.txt | Manual prerelease only; not latest |
| QGIS + ArcGIS host extensions | geoai-hosts-v0.1.0-preview.1 | Three host packages and SHA256SUMS.txt | Manual prerelease only; not latest |
| Stable Tauri Windows updater | Future stable signed release | Approved MSI + real signature + latest.json | Not provided by either preview |

**Desktop MSI source checkout at upload:** a997e9acfa601868620c6c6f79bd851a3ea17cda — NOT independently proven exact MSI provenance. MSI Authenticode reported NotSigned. Clean-machine install, upgrade, PostGIS acceptance and updater integration remain unverified.

**GIS hosts:** QGIS plugin, ArcGIS Pro Python toolbox and a real native .NET/DAML .esriAddInX were packaged with SHA receipts. Host manifest recorded 58bd1b3aafc7b9685559f59c1209344f0c3a399b but build was from a working tree; exact clean-source reproducibility is not proven. Host installed acceptance, scientific correctness, QGIS license reconciliation and Esri distribution are outstanding.

A public GitHub Release exposes voluntary experiment downloads, not a supported general-release entitlement, automatic updater, accepted plugin marketplace listing or signed scientific result.

## Website
GeoTwins Africa's public download routes dynamically discover approved published assets. https://geotwins.org/agot/ handles eligible desktop MSI releases; https://geotwins.org/plugins/#packages requires a complete published GIS host prerelease with exact three filenames and verified GitHub digests. Drafts never count as public assets.

## Guide index
- [AGOT Desktop installation and known limits](AGOT_DESKTOP_1.0.4_PREVIEW_1.md)
- [QGIS preview and licence warning](QGIS_GEOAI_0.1.0.md)
- [ArcGIS Pro Python toolbox](ARCGIS_PRO_PYTHON_GEOAI_0.1.0.md)
- [ArcGIS Pro native add-in](ARCGIS_PRO_NATIVE_GEOAI_0.1.0.md)
- [Shared host SDK](GEOAI_HOST_SDK_0.1.0.md)
- [Next-day test matrix](PREVIEW_ACCEPTANCE_20261105.md)
