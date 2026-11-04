# AGOT and GeoAI GIS-host preview acceptance matrix

**Status as of 5 November 2026:** Build artifacts and GitHub uploads exist with verified SHA-256. Actual installed functionality and clean upgrades are pending. Experimental publication is not professional, security or scientific certification.

## Exact candidate hashes
| Product | File | SHA-256 |
| --- | --- | --- |
| Windows Desktop 1.0.4 | AGOT.Desktop_1.0.4_x64_en-US.msi | 1d02e66348cbde2d4c4157d096987c3659f9d87709789f3f7429ba8702899770 |
| QGIS plugin | geotwins_geoai_qgis_0.1.0.zip | 8946a7de5050449d5abc471af7c8bfb3230c3b9fb40aec0a052563ac5d423ce1 |
| ArcGIS Python | geotwins_geoai_arcgis_pro_0.1.0.zip | bfee6d37e2b18a2849bbe42378ebd76f8d40a14fc54e9131007c609d61fa5007 |
| ArcGIS native | GeoTwins.GeoAI.ArcGISPro.esriAddInX | bdab5b1d7d0e87d49fa316998cab4c2d40188847eedcb17f171ba2d573591880 |

## Test session — all unchecked pending real evidence
- [ ] Download anonymously from public GitHub and verify complete SHA-256 for each file.
- [ ] Verify actual Windows MSI version, code signature result (unsigned if so), startup and permission/error handling.
- [ ] Clean Windows 11 x64 desktop installation and WebView2/AGOT service/PostGIS readiness.
- [ ] Preview 3 to 1.0.4 upgrade, backup/restore and reopen local projects; uninstall/rollback scenario.
- [ ] Actual GIS import, edit, geoprocess, export and saved source/revision rights on real authorized data.
- [ ] Local model/provider, approved GeoAI plan, execution receipt, cancellation and stale source rejection.
- [ ] QGIS 3.44 plugin install, real dock and Processing provider, native geometry, CRS and output checks.
- [ ] Licensed ArcGIS Pro 3.7 Python toolbox loaded, plan/approval, output layout and no bearer token in GP history.
- [ ] Licensed ArcGIS Pro 3.7 native .NET add-in installed, UI ribbon/dockpane and authenticated handoff verified.
- [ ] 3D terrain, valid vertical datum, real GPU/memory load and source revocation independently benchmarked before performance claims.
- [ ] QGIS restrictive embedded licence reviewed; choose GPL-compatible terms and publicly available corresponding source before seeking official QGIS plugin repository admission.
- [ ] Esri distribution terms, all third-party notices and permitted data licenses reviewed.
- [ ] Ensure GIS-host prerelease cannot supersede desktop stable updater feed; no latest.json/.msi.sig attached.

## Record evidence
Capture exact machine/OS build, package hash, data CRS, sanitized logs, product steps and pass/fail. Store reports in development evidence, not as a false claim of released production acceptance. File support issues at https://github.com/aerocorp13/AGOT-Releases/issues or mail admin@geotwins.org without confidential credentials.
