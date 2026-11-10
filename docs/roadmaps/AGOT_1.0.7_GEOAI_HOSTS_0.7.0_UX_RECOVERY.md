# AGOT 1.0.7 + GeoAI Hosts / SDK 0.7.0 — usability-first recovery roadmap

**Proposed:** 10 November 2026 · **not a published release or version bump**  
**Inputs:** public Desktop 1.0.6 Preview 2 (source `9a0aa8b`), public hosts 0.6.0 Preview 1 (source `756133f`), draft private integration [PR #21](https://github.com/aerocorp13/world-twin-agents/pull/21), owner-observed Home and GeoAI usability defects, and the existing source capability/acceptance ledger. The private PR is not public documentation or an open-source license grant.

## Product decision

**Stop adding primary navigation and specialist configuration before common tasks work.** AGOT should be approachable by planners, engineers, surveyors, environmental officers, local-government teams, architects and experienced GIS analysts. GeoAI should be a *cross-workspace assistant grounded in the current project*, not a separate laboratory full of infrastructure panels. Preserve the expert tools; progressively reveal complexity on demand.

**Success definition:** A first-time non-GIS user can describe a task in ordinary language, select or import the necessary authorized inputs, inspect the proposed operations, explicitly approve any effect, receive a real visible GIS output, save it, reopen it, and understand any failure. The same operation and receipt must be accessible in Professional mode.

## Product navigation: destination design

### Home / Projects (Desktop 1.0.7)

- Primary focus: **New project**, **Open project**, **Recent projects** (real, no fixture data) and **Resume last work**; one quiet project search/filter.
- Secondary, compact actions: **Ask GeoAI**, **Open map**, **Import data**. Offer 3–5 task templates without long explanations on the landing page.
- Remove instructional walls, duplicate module grids, technical capability tables, speculative analytics cards, marketing copy and persistent system diagnostics from Home. Tutorials become a discoverable **Learn / Tutorials** destination; operational errors remain in the relevant status or task panel.
- Show concise one-line context only when useful: project name, last saved, actual location/CRS where available. Never manufacture last-used projects or city metrics.
- Contextual `i` help can appear on hover **and keyboard focus/touch activation**; essential instructions and blocking warnings must never be hover-only. Provide closeable first-run tips and an accessible Help command.

### GeoAI workspace (Desktop 1.0.7)

- A persistent, dockable **Ask GeoAI** pane (right by default, optional left), callable from **every** major workspace and with a keyboard shortcut. Its first focus is a single plain-English question box: **“What would you like to do with your project?”**
- Beneath the composer, 4–6 **real supported example tasks**: “Map my project area”, “Buffer these roads by 50 m”, “Measure this site”, “Compare two layers”, “Assess flood exposure using my data”, “Export this map”. Unsupported simulations and engine actions must appear as unavailable with a reason, not as decorative chips.
- Context strip: **Current project / selected layers / CRS / provider readiness**. Missing project or source triggers one clear “Choose your data” action; no silent guesses.
- One **task timeline**: **Ask → Inspect sources → Propose plan → Review/Approve → Run → Result**. Show which step is active, which engine/tool is truly available, progress/cancellation, and an actionable failure with retry/replan. Do not let agent prose impersonate a success receipt.
- Plan preview: tool names in plain language, selected source, buffer distance/units, expected output, model/provider and warnings. Keep parameter editing and source lineage in **Advanced / Professional**, not permanently on screen.
- Result card: actual feature count, output layer name and path, CRS, source and run IDs, map preview/zoom, **Add to map**, **Open results**, **Save/export**, **View technical receipt**. Empty valid outputs must be distinguished from failed jobs.
- Keep model integrations, raw MCP/SDK settings, debug traces, local-provider setup, specialist harness history and developer-only controls in **Settings → AI & Integrations**, **Activity / Run history**, or Advanced drawers. Do not duplicate chat composers across agent panels.
- Use one source-verified operation registry and one action/receipt path for Guided and Professional views. No second autonomous executor, unreviewed shell/Python/SQL, fabricated data or silently approved effects.

### Example first-time user journey

`Open project → Ask “Which roads are within 100 metres of schools?” → choose my roads and school points → verify projected units → preview buffer/intersection plan → approve → native operation executes → new layer appears on Map and Results → save → reopen with receipt.`

If there are no school locations or no authorized source, the assistant explains the specific missing input instead of inventing schools. A planner can perform the same operation manually through Geoprocessing; an expert can modify joins, geometry predicates, CRS and output settings.

## Version 1.0.7 — focused desktop delivery sequence

| Priority | Deliverable | Definition of done |
| --- | --- | --- |
| **P0.1** | Quiet, task-first Home/Project page | Real recent projects + three primary actions; Learn/help moved out; no redundant cards; dark/light, 125–150% DPI and keyboard QA |
| **P0.2** | Single dockable Ask GeoAI everywhere | Composer follows project/map context; resize, pin/unpin, switch tabs, close/reopen and restore without remounting live WebGL; no duplicate chat |
| **P0.3** | Plain-English to reviewed GIS output | Real selected layers, typed plan, explicit source and approval, persisted GIS artifact and visible map/results/reopen |
| **P0.4** | Failure-aware agent interaction | Genuine provider/algorithm failure → diagnosis → revised plan → fresh human grant → verified output or honest blocked state; cancellation and no-effect replay |
| **P0.5** | Output and project continuity | Canonical source IDs/CRS, derived layer selection, map attachment, save/reopen, export, persistent job history and actual output count/checksum |
| **P1.1** | Professional controls without beginner overload | Expert parameter editor, provider/source settings, provenance drawer and batch tool access behind progressive disclosure |
| **P1.2** | Worlds → Simulation → Twin → 3D one usable journey | Real authorized dataset versions, saved scenario, numeric study, source-bound scene; reopen and independently measure GPU renderer behavior |
| **P1.3** | Tutorials and support | Separate searchable Learn area, concise context-aware guides, offline help, troubleshooting linked from actual errors |
| **P1.4** | Release + quality telemetry | No sensitive content upload; evidence-bound build/source identification, crash diagnostics and actual acceptance records |

Use existing `WorkspaceDocuments`, `premiumHome.css`, `CustomerTaskLauncher`, `AgentPage`, `GeoAIAssistant`, durable task/goal panels, `DockviewWorkspace`, project context and registered GIS jobs. **Consolidate** rather than layering new panels on existing panels. The current first-stage task launcher is navigation-oriented; it does not by itself execute an end-to-end workflow.

## Version 0.7.0 — SDK / plugins delivery sequence

| Priority | QGIS, ArcGIS Pro and SDK result | Definition of done |
| --- | --- | --- |
| **P0.1** | Native Ask → plan → execute → receipt parity | In **both installed hosts**, same typed task and source rules yield actual buffer/intersection/clip output, visible layer, count, checksum and reopened artifact |
| **P0.2** | Contextual dock UX | QGIS right-pinnable panel with brand SVG; ArcGIS Pro dockpane with recognizable green glyphs and preserved dock state; one chat/plan/result flow |
| **P0.3** | Provider and model reliability | Installed local Ollama and optional OpenAI-compatible/vLLM/cloud provider selection; actual model tool-call or valid typed proposal, bounded errors, explicit remote consent; no synthetic successes |
| **P0.4** | Correct approvals and recovery | Source drift fail-close, exact-plan approval, revised approval after failure, crash/restart and reconnect without double GIS effects |
| **P0.5** | Compatibility and packaging | Version/source manifests across all five artifacts, semantic release feed, installer/update guidance, QGIS version compatibility checks, licensed Esri .NET/ArcPy checks |
| **P1.1** | Restricted MCP and portable SDK | Verified installed MCP tool discovery and read-only catalog, scoped native execution through existing permissions, documented API contracts, examples and tests |
| **P1.2** | Standalone documentation | Install, setup, privacy/model requirements, common operations, troubleshooting, upgrade path and example real-data receipt |

A published website download is **not** an automatically installed or updated host plugin. Do not call any of these tasks complete without real GIS host acceptance.

## UI design/acceptance rules

- Target clear 1280×800, 1440×900, 1920×1080 and 2560×1440 layouts, light/dark, 100/125/150% scaling, keyboard/focus access, screen-reader labels, zoom and reduced motion. **Observe** actual visuals on a Windows workstation; source-only CSS tests cannot certify visual design.
- Default Home contains **no** opaque API IDs, 20-module lists, giant capability cards, diagnostics dump, “setup guides” or verbose marketing. Expose them through Settings, Learn or the relevant task.
- Default GeoAI contains **one** question box, task examples, a compact context header and the current task/results. Hide no critical permission, approval or error in a tooltip.
- Every actionable CTA either runs an existing registered operation or tells the user what prerequisite is missing. No fake “AI working” animation, static output counts or invented project data.
- Measure: time to first real layer; time to successful first reviewed geoprocessing output; novice completion rate and errors; number of visible controls on first open; successful save/reopen; cancellations and source-denial handling.

## Must-pass customer acceptance journeys

1. **Planner:** import actual project boundary, map it, buffer roads, intersect a known flood-risk layer, export PDF/GeoPackage; verify geometry, CRS, counts, source rights and saved output.
2. **Engineer:** edit road alignment/vertices, calculate proximity, save and reopen corrected layers; derive and view project output.
3. **Surveyor:** select a correctly georeferenced site and measure its area/length with explicit units; export with source identity.
4. **Environmental analyst:** choose documented raster/flood evidence, produce a *qualified* exposure output, disclose missing data and scientific limitations.
5. **Novice:** use one Ask pane for a one-sentence question, understand the proposed plan, approve, see results on Map and export without learning ArcPy/QGIS terminology.
6. **Expert:** perform the identical task through manual GIS tools and compare identical algorithm parameters and persisted output hashes.
7. **Failure/security:** with missing provider, denied dataset, changed source SHA, invalid CRS, empty valid result, canceled task and host reconnect, the UI reports the truth and never replays effects.
8. **Installed delivery:** use actual Windows 11, installed QGIS and licensed ArcGIS Pro; run build and clean upgrade, verify artifact hashes, crash recovery, renderer state and plugin version detection. Test local RTX 4060 only where GPU is part of the capability claim.

## Release decision and dependency boundaries

The source architecture handoff still records unverified capability IDs across the workstation, native GIS and World mission. Continue PR #21, preserve the existing canonical authority/implementation ledger, and implement substantial connected source→output slices; **do not** equate a passing source test with native field approval.

Suggested gates in order:

1. Freeze a candidate source SHA; inspect exact 1.0.6 and 0.6.0 published gaps before changing versions.
2. Finish and validate P0.1–P0.5 with targeted tests (one coherent integration pass), disposable PostGIS, real data, and actual application UI proof.
3. Run native QGIS + ArcGIS field tests, SDK/MCP interoperability, model-provider tests and source-bound receipts.
4. Run clean MSI install/upgrade/restart, WebGL/3D, accessibility and visual matrix. Scientific results need independent reference validation where claimed.
5. Only after those gates and owner authorization, choose whether 1.0.7 / 0.7.0 merit a separately published **experimental** release. Version numbers here are working targets, not already built artifacts.

## External UX references (design inspiration, not claimed AGOT features)

- [Esri: ArcGIS AI assistants](https://architecture.arcgis.com/en/industry-and-tech-patterns/ai-lens/ai-assistants.html) — scoped, permission-grounded task assistants.
- [QGIS Model Designer](https://github.com/qgis/QGIS-Documentation/blob/master/docs/user_manual/processing/modeler.rst) — accessible chain of real algorithms with editable parameters.
- [Microsoft MCP app UX guidelines](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/declarative-agent-ui-widgets-guidelines) — focused chat, explicit task state and human control.

**Roadmap ownership:** GeoTwins Africa. Report observed bugs with reproducible steps; do not publish private client datasets, tokens, company-private code or assumed feature-completion claims in this public repository.
