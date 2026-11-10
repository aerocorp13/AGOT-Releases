# AGOT Desktop 1.0.6 — Preview 2 release notes

**Published:** 9 November 2026, 17:33 UTC  
**Channel:** experimental Windows x64 public prerelease, **not stable or field-certified**  
**Tag:** [v1.0.6-preview.2](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.6-preview.2)  
**Exact recorded application source:** [9a0aa8b41cb7b7339a72296fdd9f6a48374ca77d](https://github.com/aerocorp13/world-twin-agents/commit/9a0aa8b41cb7b7339a72296fdd9f6a48374ca77d)  
**Development integration:** [draft PR #21](https://github.com/aerocorp13/world-twin-agents/pull/21), which continues past this binary's source commit.

## Download and verify

| Published asset | Bytes | SHA-256 |
| --- | ---: | --- |
| \`AGOT.Desktop_1.0.6_x64_en-US.msi\` | 1,416,188,896 | \`59ae2b13f2bddfb7cff5abea1fa090814b572eeeb87fd38bf20211a6182f4df3\` |

The release also includes \`SHA256SUMS.txt\` and \`release-evidence.json\`. These are actual GitHub-uploaded asset records, not promises of signed installers. The release declaration says **Authenticode: NotSigned**. The installer was uploaded from an existing recorded native build; this documentation update does not rebuild it.

Check your downloaded MSI on Windows:

\`\`\`powershell
Get-FileHash -Algorithm SHA256 .\AGOT.Desktop_1.0.6_x64_en-US.msi
\`\`\`

Back up existing projects and local data before upgrading. GitHub's generated “Source code” archives for this *distribution repository* are **not** the private AGOT application source.

## What changed from the 1.0.5 preview

These are source-described areas of 1.0.6 engineering, **not a claim that every screen or operation has passed installed-user acceptance**:

- **A more integrated geospatial workstation:** Concept 6 ribbon and project workspace, source-aware Map, Edit, Analysis, Catalog, Imagery, Twin, Worlds, Simulation, Geoprocessing and GeoAI workspaces with project/save and output presentation work.
- **More substantial 3D pathways:** MapLibre, Three.js and Cesium views share source-governance and scene context. The source engineering notes describe 3D Tiles/GLB ingestion, locally selected PMTiles, terrain/vertical-datum checks, and diagnostic states for unavailable or unauthorised source data. Performance and multi-engine rendering still require a real GPU acceptance matrix.
- **Simulation and digital-twin work:** numerical, recorded-source studies and versioned World/Scenario concepts, including exploratory hydrology, urban dynamics and evidence replay. **Do not treat exploratory numerical results as calibrated flood, traffic, heat or engineering forecasts.**
- **GIS and GeoAI workflow integration:** typed source/CRS-aware processing, reviewed actions, persistent output receipts, and links between project layers, Worlds, Simulation and Twin workflows. A visible capability is not proof of successful end-to-end native execution.
- **Build and reliability corrections:** better DEM tile identity and checksum diagnostics, GLB classification, source-linked scene replay, TypeScript/JSX repairs, Rust hydraulic build corrections, immutable simulation input handling and additional automated contract tests.

A later draft PR #21 may contain changes that are **not present in this MSI**. Specifically, the published 1.0.6 MSI is bound to \`9a0aa8b\`; later branch HEAD \`756133f\` includes additional ArcGIS icon and host message fixes and must not be retroactively claimed as part of this installed desktop binary.

## Known limitations / evaluation cautions

1. **Experimental UI:** Home/project entry and the GeoAI route currently expose too much explanatory and specialist configuration; a unified plain-English, cross-workspace assistant and low-clutter Home are **planned**, not delivered as 1.0.6 user-accepted outcomes.
2. **Agent execution:** source-side plans, receipts, failure handling and World-to-Twin code do not establish a reliable operator journey. Verify real input, approval, native output, on-map result, reopen and restart yourself.
3. **Separate host channel:** QGIS, ArcGIS Pro add-in/toolbox and Python SDK have their own [0.6.0 preview](GEOAI_HOSTS_0.6.0_PREVIEW_1.md). They are not bundled in, synchronized by, or automatically updated by this MSI.
4. **Unverified native gates:** clean Windows install/upgrade, full licensed host pairing, persistent GIS output across hosts, real-model inference quality, GPU three-engine rendering, signing and signed automatic updating remain separately unverified.
5. **No invented sources:** absent or unauthorized data should fail clearly, rather than filling the map with fictional buildings, layers, terrain or simulation results.

## Installation, issue reporting, and next version

Use the linked GitHub release for actual binaries; report version, OS, intended task, source CRS (without confidential data), expected result, observed error and whether output appears in Map/Results and after reopening. Never share access tokens or protected datasets.

**Next:** [AGOT Desktop 1.0.7 + GeoAI Hosts/SDK 0.7.0 prioritized UX and reliability roadmap](../roadmaps/AGOT_1.0.7_GEOAI_HOSTS_0.7.0_UX_RECOVERY.md). Those are **proposed next version scopes**, not released builds or delivery-date commitments.

_This note reconciles the public GitHub release with source evidence reviewed 10 November 2026. It does not amend the original release's binary provenance, tests or acceptance status._