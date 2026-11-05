# AGOT Desktop Windows 1.0.5 — Preview 1

**Release channel:** Experimental **public GitHub prerelease**; not a stable release.
**Publishing:** The automated pipeline publishes only after all named assets are uploaded and checked. The release must end with \`isDraft=false\` and \`isPrerelease=true\`.

- **Source repo:** https://github.com/aerocorp13/world-twin-agents
- **Source commit:** [\`64452231cabee5d1e6b6124923c25d1b2d5ebea9\`](https://github.com/aerocorp13/world-twin-agents/commit/64452231cabee5d1e6b6124923c25d1b2d5ebea9)
- **Release tag:** \`v1.0.5-preview.1\`
- **Target:** Windows 11 x64, native Tauri/MSI, packaged local FastAPI/PostGIS
- **Model weights:** Not bundled or downloaded.

## Actual release files and SHA-256

| Asset | Size | SHA-256 |
| --- | ---: | --- |
| \`AGOT.Desktop_1.0.5_x64_en-US.msi\` | 1,408,242,136 bytes | \`4c84b5f682cd709996ae6fb8edde07890e9118271816755f1e8ee57b5de251de\` |

Verify on Windows with \`Get-FileHash -Algorithm SHA256 <asset>\`.
The hashes prove bytes only; they do not prove Authenticode signing or licensed-host acceptance.

## Changes since the previous source baseline

- Full-stack readiness diagnostics now distinguish real PostgreSQL/migration, GIS queue, GeoAI agent worker, model tool-call readiness and host pairing states.
- GeoAI frontend reads the authenticated backend's real readiness rather than treating a saved model profile as functional.
- Stored model verification is invalidated when a desktop backend instance restarts or the verification window expires.
- Durable GeoAI and Geoprocessing share the same actual GIS job ID/status, recorded output, error and provenance path.
- Source code includes the continued Concept 6 enterprise workstation redesign and lower-module UI integration; completeness must still be confirmed in installed frontend/back-end acceptance.
- GIS hosts 0.3.0 are independently packaged and published as a **separate** GitHub prerelease; they are not embedded model/Esri runtimes.

## Detailed source change evidence

Source comparison: \`origin/main\` (merge-base) → \`64452231cabee5d1e6b6124923c25d1b2d5ebea9\`.
Changed source paths: **675**. Source commits in comparison: **100**.

### Related changed areas

- **GeoAI model/agent/backend:** 34 changed paths
- **GIS host/SDK packaging:** 42 changed paths
- **Desktop and full-stack UI:** 137 changed paths
- **Release, CI and architecture:** 227 changed paths
- **Other GIS/World modules:** 235 changed paths

### Source commits

- [\`64452231cabe\`](https://github.com/aerocorp13/world-twin-agents/commit/64452231cabee5d1e6b6124923c25d1b2d5ebea9) fix(windows-release): keep database-dependent GeoAI endpoint test out of early source preflight
- [\`e73718b07738\`](https://github.com/aerocorp13/world-twin-agents/commit/e73718b07738bc65c8f9b91b8fb088fc2d87d0ac) fix(build-preflight): execute GeoAI policy catalog regression before expensive PyInstaller freeze
- [\`7aa8b57f32fd\`](https://github.com/aerocorp13/world-twin-agents/commit/7aa8b57f32fde26a9e5174886ee9fb30118945f1) fix(geoai): separate local workflow policy permission from verified native model readiness
- [\`acce352b2f29\`](https://github.com/aerocorp13/world-twin-agents/commit/acce352b2f297a091077b5320cdc8356dccb73de) fix(release-python): consistently resolve pinned Python 3.12 venv and locked pytest dependencies
- [\`a960c483da68\`](https://github.com/aerocorp13/world-twin-agents/commit/a960c483da686a44e261bef1433f4b26ddaf81fa) test(host-sdk): accept and verify all four deterministic 0.3.0 standalone distributions
- [\`638cc19c8a8f\`](https://github.com/aerocorp13/world-twin-agents/commit/638cc19c8a8f96c34119de89e8a4a217d9a04611) fix(release-ci): repair all seven npm test failures from desktop fixture and source UI contracts
- [\`37b67f7d5817\`](https://github.com/aerocorp13/world-twin-agents/commit/37b67f7d5817cb3155eb13db8f013fcc9c194c57) fix(concept6): replace unsupported Fluent DocumentCode20Regular icon
- [\`846d0729d524\`](https://github.com/aerocorp13/world-twin-agents/commit/846d0729d5241a4a8908118252eb5985b404be71) fix(preview-release): correct stale 1.0.4 window title gate for desktop 1.0.5
- [\`fafc1ce15134\`](https://github.com/aerocorp13/world-twin-agents/commit/fafc1ce151342fb97843254a0da8a6ce1e27332d) fix(preview-publisher): allow only unstaged regenerated Esri .NET bin/obj outputs without discarding user files
- [\`9d9624c76a92\`](https://github.com/aerocorp13/world-twin-agents/commit/9d9624c76a921edabb0c49495a6060c1502522af) fix(releases): replace outdated planned-preview docs when public binaries are published
- [\`550e0ff1eda9\`](https://github.com/aerocorp13/world-twin-agents/commit/550e0ff1eda949779a996f9ad45d1847118e360b) feat(geoai-hosts): independent local Ollama agent SDK, native GIS hosts and complete prerelease pipeline
- [\`7a60ea361c82\`](https://github.com/aerocorp13/world-twin-agents/commit/7a60ea361c82cc442c171867cf2d6839f5b29bd7) test(docs): lock Home/Utility, GeoAI and icon bundle acceptance with truthful v1.0.5 evidence
- [\`c9c7b77a0822\`](https://github.com/aerocorp13/world-twin-agents/commit/c9c7b77a0822eb82c60d5d2eee88e31a726b9814) perf(icons): statically import Fluent glyphs for tree-shaken desktop bundle
- [\`8831f7afbbee\`](https://github.com/aerocorp13/world-twin-agents/commit/8831f7afbbee7bdab4ea0f740711577a3e25264e) feat(icons): unify durable GeoAI agent, World evidence and cartography on Fluent registry
- [\`918829a681d3\`](https://github.com/aerocorp13/world-twin-agents/commit/918829a681d37861e832bb482c2fa5d9b1a16683) feat(workstation): complete source-backed Home results and Utility jobs workbenches
- [\`25d74339583d\`](https://github.com/aerocorp13/world-twin-agents/commit/25d74339583dbbc262a0c9c8c2f68b053da60e4a) docs(workstation): record v1.0.5 per-module integration, test commands and native blockers
- [\`d7f6ec6ce005\`](https://github.com/aerocorp13/world-twin-agents/commit/d7f6ec6ce005233c73e6255bc923d13d29dd4aa1) style(workstation): centralize semantic chrome tokens and restore project-specific tree state
- [\`376d08c89924\`](https://github.com/aerocorp13/world-twin-agents/commit/376d08c89924da60103bfdb672694d942628d467) feat(geoai): show verified agent map beside workflow with real evidence/results deck
- [\`9bf51610e92b\`](https://github.com/aerocorp13/world-twin-agents/commit/9bf51610e92be5f270c585c0121698ff1dde0a55) test(desktop): add Concept 6 v1.0.5 source, 416-case matrix and local MSI gate
- [\`72e63c8189dc\`](https://github.com/aerocorp13/world-twin-agents/commit/72e63c8189dc08782a7eac9c83540701a1af23ff) test(workstation): assert 20-route migration, source-backed panes and Fluent registry integrity
- [\`0c61cce80475\`](https://github.com/aerocorp13/world-twin-agents/commit/0c61cce804755d5052c460007e87e89364922f12) fix(workstation): functional hydrology timestep selection and clean migrated icon imports
- [\`eae7e72e76f6\`](https://github.com/aerocorp13/world-twin-agents/commit/eae7e72e76f6e11ef66b7c923cb5a40ca689a2e7) style(workstation): consolidate GeoAI, Edit, Share, Engineering and Add-In interiors
- [\`7065d7cde7ea\`](https://github.com/aerocorp13/world-twin-agents/commit/7065d7cde7eae2b3ab7303fa9a68eab11e23faff) feat(workstations): integrate Concept 6 GeoAI, Edit, Share, Engineering and native host pairing
- [\`af4b251b551c\`](https://github.com/aerocorp13/world-twin-agents/commit/af4b251b551cdf92d938682e501379bbfdbbb072) feat(3d): migrate recorded multi-engine scene browser, source inspector and evidence deck
- [\`e32ca27a85af\`](https://github.com/aerocorp13/world-twin-agents/commit/e32ca27a85affdedd9647c4479d6d6ad586489c5) feat(workstation): controlled persistent project navigation across all major workspaces
- [\`64d82f31fcf1\`](https://github.com/aerocorp13/world-twin-agents/commit/64d82f31fcf1e790bd0cb493706b7e310fb10c26) feat(simulation): migrate all simulation disciplines and durable hydrology job workbench to Concept 6
- [\`6ca36e0232b9\`](https://github.com/aerocorp13/world-twin-agents/commit/6ca36e0232b9561522479fa9d7d03ae47eb21d68) build(desktop): align AGOT 1.0.5 installer identity and fix catalog virtual-grid stability
- [\`841b1f81e247\`](https://github.com/aerocorp13/world-twin-agents/commit/841b1f81e24773a3601d0be8765d5983f29b5e29) feat(fullstack): reconnect actual GIS worker results, session-fenced model probes and desktop worker health
- [\`95a60a9f9666\`](https://github.com/aerocorp13/world-twin-agents/commit/95a60a9f96660dfaa46199d17c362cb1c6a214ea) feat(gis-hosts): real standalone ArcPy/QGIS native processing without AGOT Desktop
- [\`9e631b9c26d3\`](https://github.com/aerocorp13/world-twin-agents/commit/9e631b9c26d36217e396b6e1af7286b3833e9fdf) feat(fullstack): unify AGOT installed-service readiness, verified model gating and GeoAI runtime evidence
- [\`350d31e1a161\`](https://github.com/aerocorp13/world-twin-agents/commit/350d31e1a161493c221275738f3b0ce522061b31) feat(workstations): source-bound simulation readiness and consistent module pane/runtime states
- [\`3c1a06c3a4b3\`](https://github.com/aerocorp13/world-twin-agents/commit/3c1a06c3a4b3ab5951e5f35901e1d921bfe40b82) feat(icons): Fluent semantic icons across core lower modules and owned GIS operation glyphs
- [\`3412a93f255e\`](https://github.com/aerocorp13/world-twin-agents/commit/3412a93f255ee0ecd742043e4a52f67fa1d55153) feat(catalog): source-backed virtual dataset browser and compact Concept 6 inspector
- [\`49ecdb25b477\`](https://github.com/aerocorp13/world-twin-agents/commit/49ecdb25b47730aaa4cd4b5d930eeb90eb75195f) feat(workstation): source-backed Concept 6 Twin, Home and routed desktop interiors
- [\`9ba5eccf7b08\`](https://github.com/aerocorp13/world-twin-agents/commit/9ba5eccf7b088d02a1b8056456d6e6b21034066c) style(workstation): consolidate Concept 6 lower-pane rules and add integration contracts
- [\`6f28aadb9e5a\`](https://github.com/aerocorp13/world-twin-agents/commit/6f28aadb9e5a4184eda92b4f5ea4baa67bac577e) feat(workstation): Concept 6 shared panes and connected specialist module surfaces
- [\`17ce3bea4fc7\`](https://github.com/aerocorp13/world-twin-agents/commit/17ce3bea4fc73bb9f65f9832ba53d1174672fa39) fix(geoai-host): discover real AGOT Desktop loopback API and expose native pairing UX
- [\`d5ef5cb2f6e4\`](https://github.com/aerocorp13/world-twin-agents/commit/d5ef5cb2f6e4af41006268e6d275dae21fdc88b1) fix(host-v2): use named hashtable splatting for child GIS package build
- [\`9783bfe8ce2f\`](https://github.com/aerocorp13/world-twin-agents/commit/9783bfe8ce2f96a73678d30ebca6e373897eb085) fix(host-v2): robust one-command Windows rebuild and exact ArcGIS package version gate
- [\`fdd6a86771ab\`](https://github.com/aerocorp13/world-twin-agents/commit/fdd6a86771ab23888404af4558018f5ceec26b80) build(host-v2): include matching AGOT Desktop backend in one-command native host rebuild
- [\`62a6ad947c2a\`](https://github.com/aerocorp13/world-twin-agents/commit/62a6ad947c2ae956a12cc1a39524357186f39c5e) test(host-sdk): distinguish valid empty derived outputs from invalid empty input sources
- [\`50db3e3bb5f4\`](https://github.com/aerocorp13/world-twin-agents/commit/50db3e3bb5f4fd7c7df9376e4b15cca52054af91) feat(geoai-hosts): integrate V2 native ArcGIS/QGIS workstations, scoped pairing and audited host execution
- [\`a997e9acfa60\`](https://github.com/aerocorp13/world-twin-agents/commit/a997e9acfa601868620c6c6f79bd851a3ea17cda) agot v1.0.4
- [\`c23b79874c5c\`](https://github.com/aerocorp13/world-twin-agents/commit/c23b79874c5c0ef1cd360991ad2280ac4e79d1b2) sdks and plugins
- [\`d1c3359325ff\`](https://github.com/aerocorp13/world-twin-agents/commit/d1c3359325ff00843b5c0c0eb1f58e59d0a4e508) agot worksell update
- [\`8086a1d2c802\`](https://github.com/aerocorp13/world-twin-agents/commit/8086a1d2c802d25dbe847285946798024f29982f) docs(updater): correct local npx Tauri signer generate command argument forwarding
- [\`1523059b5a76\`](https://github.com/aerocorp13/world-twin-agents/commit/1523059b5a7612526fca071a9c7bbadc0af92c70) test(updater): assert cold-start upgrade is canceled after GIS input and native UI shields editing while MSI applies
- [\`8a028eb40400\`](https://github.com/aerocorp13/world-twin-agents/commit/8a028eb40400c121e8405f2b1674ced7a93c1549) style(updater): accessible exclusive Windows MSI progress shield protects active GIS state during installation
- [\`c1bf6832eff8\`](https://github.com/aerocorp13/world-twin-agents/commit/c1bf6832eff8f264b7168953e4388492abea8f66) safety(updater): block active GIS editing during signed MSI download/install and provide accessible full-screen progress
- [\`980fa9b95b55\`](https://github.com/aerocorp13/world-twin-agents/commit/980fa9b95b553c0557f8d4eab65852a5bfe1bd51) fix(updater): match official Tauri Windows x86_64 target in stable static latest.json and release validation
- [\`5d4bf2aab89c\`](https://github.com/aerocorp13/world-twin-agents/commit/5d4bf2aab89cb9f79d9a993c230b93935ccda3a4) fix(updater): match official Tauri Windows x86_64 target in stable static latest.json and release validation
- [\`a327f248f262\`](https://github.com/aerocorp13/world-twin-agents/commit/a327f248f262171cd518b53e081df3a0661961ed) fix(updater): match official Tauri Windows x86_64 target in stable static latest.json and release validation
- [\`bee1ecf859a3\`](https://github.com/aerocorp13/world-twin-agents/commit/bee1ecf859a31f3738c282b8131855525b9e96bd) fix(updater): match official Tauri Windows x86_64 target in stable static latest.json and release validation
- [\`64781acf0e78\`](https://github.com/aerocorp13/world-twin-agents/commit/64781acf0e781a69e8b7884b402910bc5315c871) fix(updater): match official Tauri Windows x86_64 target in stable static latest.json and release validation
- [\`a73afc0edaf8\`](https://github.com/aerocorp13/world-twin-agents/commit/a73afc0edaf87a728c399642a7dac55da0d8155f) safety(updater): defer automatic cold-start upgrade after any user map/project interaction
- [\`60e94ac08f0e\`](https://github.com/aerocorp13/world-twin-agents/commit/60e94ac08f0e666569513bf553db0d248a562687) safety(updater): defer automatic cold-start upgrade after any user map/project interaction
- [\`2a6d3c629930\`](https://github.com/aerocorp13/world-twin-agents/commit/2a6d3c62993076f5461679a409465d8eb3c5757d) safety(updater): defer automatic cold-start upgrade after any user map/project interaction
- [\`0c70979678ca\`](https://github.com/aerocorp13/world-twin-agents/commit/0c70979678ca744fec3d75977bc462553e457198) audit(v1.0.4): record signed updater, native host/plugin release gates WITHOUT marking unexecuted acceptance PASS
- [\`ae8b0976691d\`](https://github.com/aerocorp13/world-twin-agents/commit/ae8b0976691d9ad6010f439630a9d0f2b1c5408d) audit(v1.0.4): record signed updater, native host/plugin release gates WITHOUT marking unexecuted acceptance PASS
- [\`9458445bbe10\`](https://github.com/aerocorp13/world-twin-agents/commit/9458445bbe10b498d619d015131180b9218111b2) docs(v1.0.4): update canonical MDS, HA1/HB1/HC1 audit, R0-R6 roadmap and R6 signed updater acceptance
- … 40 older commits omitted from notes; inspect compare link.

## Evidence, limitations, and known release gates

- Source packages, hashes and release metadata are generated from actual files, not from earlier release downloads or assumed artifacts.
- **Native ArcGIS Pro 3.7 licensed execution, QGIS 3.44 field execution, real local-model inference and Windows MSI clean install/upgrade have not been certified by the release-notes generator.**
- Preview builds may be unsigned. This release does not represent a verified signed Tauri automatic update.
- Real data requires source permissions, valid CRS, model support and human authorization. Do not use experimental output as independent engineering, cadastral or survey certification.
- Known CI failures in other suites remain blockers for stable release until reproduced and resolved with actual logs.

## Installation and verification

Read the bundled README and acceptance matrix in [the source repository](https://github.com/aerocorp13/world-twin-agents). Verify each downloaded SHA-256 against \`SHA256SUMS.txt\`. For host previews, the QGIS ZIP installs via Plugins → Install from ZIP, ArcGIS Pro uses the native Esri add-in and sibling toolbox, and the Python wheel installs independently with pip. For Desktop, run the MSI and verify the active service/worker integration before relying on GeoAI.

---
_Generated from the exact source SHA and staged built artifacts. No fabricated test result or certification is implied._
