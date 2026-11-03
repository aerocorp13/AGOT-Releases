# Quality, verification and preview limitations

**AGOT is a public preview, not a certified professional GIS, civil-engineering or scientific prediction service.** The presence of a feature in code, release notes or a synthetic test does not by itself establish that every configuration will work.

## Evidence already public

- Three public Windows preview MSI assets have been published since 29 October 2026.
- Preview 3 (Desktop 1.0.2) has an immutable GitHub-published MSI asset digest.
- The Preview 3 release describes batch-insert and regression fixes, World versioning, approved GeoAI jobs, inference records and local geospatial workspaces.

The source repository is private; published release descriptions and installer metadata are the public evidence available here. The following independent tests or acceptances have **not** been confirmed in this repository.

## Critical remaining gates

| Gate | Required validation |
| --- | --- |
| Installed runtime | Fresh Windows 11 x64 setup, launch, backend startup, WebView2, permissions, shutdown |
| Upgrades | Preview 1/2 → Preview 3, failure rollback, uninstall/reinstall and workspace backup/restore |
| Code signing / license | Authenticode publisher identity, installer terms, third-party notices and redistribution obligations |
| Basic GIS | Real data with known CRS/datum, import/reopen/edit, derived revision, geometry/topology regression and error states |
| Worlds | Authorized source read/revoke, fork, historical correction, immutable baseline and predictable persistence |
| GeoAI | Actual local/remote provider connectivity; effect approvals; trace replay; job failure/cancellation without partial silent writes |
| ONNX | Compatible licensed checkpoint and true inference accuracy, memory pressure, lease cancellation and retry |
| 3D/terrain | Real DEM vertical reference, view engine behavior, scene persistence, GPU and high-DPI tests |
| Scientific models | Parameter sourcing, calibrations, sensitivity, uncertainty and domain validation for climate/hazard analyses |
| Stress and deployment | City-scale features, large rasters, disk/IO, CPU/GPU budgets, authorized plugins, offline behavior |

## Specific limitations in Preview 3 notes

- Windows installed acceptance, backup/recovery and uninstall are distinct from successful source/package builds.
- Local-model connections and real ONNX checkpoint quality are not established by mocks.
- Cancellation of long native inference calls can be cooperative between tiles.
- Simulation/hazard studies are not consistently under the same durable agent protocol and are not scientifically calibrated.
- 3D providers, full linked multi-view synchronization, point-cloud/BIM support and city-scale performance have bounded coverage.
- Complete signed World transfer and offline source permissions are not finished.
- Hash-verified receipts document integrity relationships, **not signatures**.

## Reporting test results

Use precise language:
- **Build succeeds:** a specified binary was produced in a stated environment.
- **Unit tests pass:** named isolated tests executed successfully with measured counts.
- **End-to-end pass:** a particular workflow completed on named data/environment.
- **Installed-native pass:** a real installed Windows client performed the workflow.
- **Professionally validated:** an independent qualified review, scientific calibration or regulatory acceptance was completed.

Do **not** infer one level from another. Mock and synthetic data are valid for engineering regression but must never be described as operational African planning observations.

[Install](INSTALLATION.md) · [Capabilities](CAPABILITY_MATRIX.md) · [Roadmap](../ROADMAP.md).
