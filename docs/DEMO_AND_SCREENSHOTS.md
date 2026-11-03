# Genuine screenshots and demo evidence policy

AGOT screenshots should show **the actual running application**, with the release/version and data provenance made clear. Concept images, rendered product art and static UI sketches must **never** be presented as proof of implemented functionality.

## Required showcase captures (future work)

| Shot | What a real capture must demonstrate |
| --- | --- |
| Home / project launcher | Actual installed Windows build and available project/start actions |
| Map + Catalog | Real layers, attribution, source format, map state and source metadata |
| Editing + geoprocessing | Selected feature, registered tool/parameters, human review and derived revision |
| Worlds | Source-backed baseline, version list, fork/correction and authorization behavior |
| GeoAI | Real registered tool, plan/progress, approval control and input/output receipt |
| Twin / terrain / 3D | Actual renderer, authorized source and clearly stated DEM/vertical reference assumptions |
| Simulation | A real solver/indicator output with disclosed calibration and uncertainties; otherwise label prototype |
| Installation | Actual Windows installer, version information and launch/result evidence |

## Rules for publication

1. Name installed product version, release tag and OS build. Do not substitute later private branch screenshots for Preview 3.
2. State data provenance and whether the source is real, anonymized, synthetic or a fixture.
3. Redact credentials, private local file paths, user names, customer datasets and precise sensitive locations.
4. Do not overlay invented model confidence, maps, projections, map labels, traffic or scientific risk readings.
5. Confirm permission to use third-party imagery, map tiles, datasets and company logos.
6. Capture real images in both dark/light and at useful display scales only after the installed app's visual signoff.

No screenshots are added to this repo until they meet these rules. We prefer **fewer genuine screenshots** over attractive but misleading concept renderings.

A useful first demo is a ~90-second installed Preview 3 sequence: open an authorized layer → inspect source → show a versioned World read → propose a registered GIS step → review before execution → inspect lineage/receipt. Label any part that cannot currently be completed in the public installer.

[README](../README.md) · [Quality and limitations](QUALITY_AND_LIMITATIONS.md).
