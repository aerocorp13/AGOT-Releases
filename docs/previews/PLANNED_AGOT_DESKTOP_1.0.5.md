<!-- Historical specification preserved for source comparison; native Windows MSI has been built. -->

**STATUS AS OF 5 NOVEMBER 2026: MSI BUILT, PUBLIC BINARY UPLOAD NOT COMPLETE.** The actual 1.0.5 MSI (1,408,242,136 bytes) was produced by Windows native compilation. The `v1.0.5-preview.1` GitHub record is still an unpublished draft with zero binary assets at inspection. See the [actual build's detailed notes](AGOT_DESKTOP_1.0.5_PREVIEW_1.md), [candidate hashes](PREVIEW_CANDIDATE_ASSETS_1.0.5_0.3.0.json) and [publication checklist](RELEASE_1.0.5_0.3.0_PUBLICATION_CHECKLIST.md). Neither this document nor an empty draft is a download link.

# AGOT Desktop 1.0.5 — Preview 1 full-stack integration change notes

**Planned public GitHub prerelease:** v1.0.5-preview.1 (or next available numbered preview at publishing). Source metadata targets AGOT Desktop **1.0.5**, Windows x64; this document records earlier source plans; the native MSI is now built, but publication remains pending.

## Main integrated code changes

1. **Authentic runtime readiness:** authenticated /api/v2/workstation/integration separates PostGIS migration state, actual GIS worker, durable GeoAI worker, model verification and host bridge. A healthy DB alone does not imply a functioning GeoAI model or geoprocessing engine.
2. **Real frontend/backend alignment:** ModelConnections, GeoAI Agent, durable workflow, Geoprocessing and the installed Tauri startup/worker status monitor use real source-truth service responses. Model configuration is not a pass; completed jobs return actual backend result/error/status and can be reopened.
3. **Native model evidence:** local tool-call and tool-result replay evidence expires after one hour or desktop-service instance replacement. Changed model ID or endpoint invalidates cached evidence. A failed or incomplete model cannot be presented as native agent ready.
4. **Source-bound GIS provenance:** approval grants, pinned sources, jobs and immutable receipts are authoritative in backend persistence, not reconstructed from UI toggles. Standalone host receipts remain explicitly host-attested.
5. **Concept 6 workstation integration:** continued enterprise lower-module redesign and shared desktop pane status/operation controls, subject to full installed acceptance across all ribbons and specialist modules.
6. **Separate host release:** QGIS/ArcGIS Pro standalone Python SDK 0.3.0 is independently downloadable. AGOT database-driven multi-world/simulation functions still require the AGOT service, not a fictional standalone host.

## Still required for stable certification

- Real installed Windows MSI clean install, upgrade from previously published 1.0.4, backend/data worker startup, persistence and recovery after restart.
- Real model tool call, GIS data import, source selection, approved GIS execution, nonempty and empty-result truth, map/attribute/results/jobs synchronization and saved project reopen.
- Licensed ArcGIS Pro 3.7 and QGIS 3.44 native execution, exact source fingerprint, signed/unsigned installer provenance and failure recovery.
- All GitHub Actions checks passing and explicit issue closure. Source tests are not substitutes for these.
- 3D city-scale tiles, vertical datum, GPU and numerical engineering accuracy require real-world independent acceptance; they are not certified merely because code compiles.

## Publication

The owner Windows publisher checks the actual MSI ProductVersion 1.0.5 and Esri SDK add-in output, emits source SHA/size/SHA256 notes, stages uploads, verifies their complete asset inventory, pushes Markdown evidence into AGOT-Releases and publishes as **isDraft=false, isPrerelease=true**.

No signed automatic updater manifest is generated without cryptographic signatures, no stable tag is created, and no release is represented as full production acceptance.
