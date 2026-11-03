# Why AGOT exists

**AGOT — African Geospatial Operational Twin** is designed to close the distance between **geospatial data**, **scenario decisions** and **actions that can be audited**.

Many infrastructure and planning teams have fragmented maps, incomplete building/road inventories, intermittent observations and limited access to specialist modeling infrastructure. A GIS viewer alone does not explain how a proposed development changes risks and opportunities—and an AI answer without source lineage cannot safely stand in for planning analysis.

## The first wedge

**Scenario Digital Twins for Climate-Resilient Infrastructure & Urban Planning in Africa.**

A team should be able to preserve one **Operational World** grounded in observed data, fork governed alternatives and compare spatial consequences before making planning decisions. The concept is extensible to other regions and disciplines.

### Example future workflow (target, not an end-to-end Preview 3 promise)

1. Import authorized administrative boundaries, roads, buildings, elevation/imagery and planning land-use layers.
2. Record provenance, CRS, valid time and known coverage gaps.
3. Commit an Operational World baseline.
4. Fork a “Green Growth” world with a transport or drainage intervention and a “Higher Warming” world with different hazard assumptions.
5. Run suitable, scientifically validated indicators or models (e.g. exposure, runoff, accessibility) on each world.
6. Let GeoAI **inspect and propose** repeatable registered operations; obtain explicit review before effectful changes.
7. Compare source-backed maps, metrics, uncertainties and derived artifacts; export an evidence-backed decision record.

**Current state:** Preview 3 publishes relevant foundations (World history/forks, governed GIS processing, GeoAI jobs and receipts). Fully coupled climate/hydrology, calibrated predictions, verified multi-engine 3D and complete report generation are ongoing milestones.

## Design principles

- **Data first:** separate measured data, derived datasets, synthetic fixtures and scenarios.
- **Operational truth stays intact:** scenario branches never silently overwrite the baseline.
- **Time is explicit:** distinguish effective/valid time from when a record was learned or corrected.
- **Grounded AI:** tools must access authorized sources and provide traceable outputs, not fabricated maps or confident unsupported numbers.
- **Human authority:** review before lasting changes; document overrides and decisions.
- **Interoperability:** use documented spatial and model interfaces wherever possible.
- **Resource awareness:** permit useful local workflows on practical developer workstations; disclose model, GPU, storage and networking requirements.
- **Portable evidence:** hashes, source IDs, parameters and approvals accompany artifacts. Hashes alone are not digital signatures.
- **Honest uncertainty:** absence of data is surfaced, not guessed.

## Product families

GeoTwins Africa's broader portfolio also includes GIS Assistant, Hybrid Map Viewer, Street AI Mapper and Physical Planning Assistant. AGOT is the flagship integration direction. Other projects and restricted pilots should **not** be treated as installed AGOT features.

[Roadmap](../ROADMAP.md) · [Capabilities](CAPABILITY_MATRIX.md) · [Public release](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.1-preview.3).
