# AGOT 1.0.7 / GeoAI Hosts & SDK 0.7.0 — source-grounded UX and release-recovery brief

**Reviewed 10 November 2026.** This is an **engineering specification**, not a shipped feature list or claim of native verification. It supplements [the product roadmap](AGOT_1.0.7_GEOAI_HOSTS_0.7.0_UX_RECOVERY.md). The implementation repository `world-twin-agents` is the private source of truth; this public brief contains no private source code, credentials or customer data.

## Exact baselines — do not mix binaries with newer draft changes

| Channel | Published artifact | Source SHA documented by its release | Acceptance boundary |
|---|---|---|---|
| Desktop | [1.0.6 Preview 2](https://github.com/aerocorp13/AGOT-Releases/releases/tag/v1.0.6-preview.2), Windows x64 MSI, 9 Nov | `9a0aa8b41cb7b7339a72296fdd9f6a48374ca77d` | Experimental unsigned build; installed/upgrade/user-workflow acceptance unverified here |
| GIS Hosts + Python SDK | [0.6.0 Preview 1](https://github.com/aerocorp13/AGOT-Releases/releases/tag/geoai-hosts-v0.6.0-preview.1), five QGIS/ArcGIS/Python artifacts, 9 Nov | `756133f85b21e3e3a1cac3f6c2109683f983f72c` | 114 source/contract tests stated in release; native QGIS/ArcGIS acceptance outstanding |
| Draft development | [world-twin-agents PR #21](https://github.com/aerocorp13/world-twin-agents/pull/21) | Head observed `756133f85b21e3e3a1cac3f6c2109683f983f72c` | **Open, draft and unmerged**. Source changes after the MSI SHA are not automatically in the installed 1.0.6 binary |

The website's downloads and release descriptions must identify each channel independently. A GitHub page displaying new assets does **not** upgrade installed add-ins, verify a plugin or add source changes to an older MSI.

## Why the present UI feels crowded: verified source anchors

The following are observations from PR #21 at the head above, rather than claims about screenshots from an installed binary.

1. **Home stacks too many entry surfaces.** `src/components/studio/WorkspaceDocuments.tsx`, `HomeStart`, contains a left Home navigation rail, a welcome/hero, `CustomerTaskLauncher`, a separate source-to-output mission section, workspace/module navigation, Recent Projects, project save/export controls and a status panel (roughly lines 174–295). Individually reasonable sections add up to competing first-screen priorities. The actual recent-project filtering exists and should be retained.
2. **The Guided task launcher is not an executable workflow.** `src/components/studio/CustomerTaskLauncher.tsx` explicitly says `Navigation only`; its Guided mode describes prerequisites and opens a destination workspace. It does **not** yet take a novice through Ask → registered plan → approved execution → saved artifact.
3. **GeoAI begins with specialist infrastructure rather than the user's question.** `src/modules/agent/GeoAIAssistant.tsx` exposes eight top-level sub-tabs: AI Agent, Analyze, Satellite AI, GIS Tools, AI Models, GIS Hosts, Evidence and Acceptance (roughly lines 370–380). Its first agent page contains `GeoAIIntegrationPanel`, `GeoAIAgentPanel`, map and evidence deck, while a prominent actual question form is inside the separate Analyze page (roughly lines 500–525). This explains the disjointed initial journey; do not solve it by adding a ninth tab.
4. **There are more specialist surfaces outside the assistant.** `src/modules/agent/AgentPage.tsx` renders `GeoAIAssistant` plus collapsible Goal Mode and Development Review. These must remain reachable without crowding the default prompt.
5. **Layout migration is an integration risk.** `AGOTWorkstationShell.tsx` uses `react-resizable-panels` as well as `DockviewWorkspace`, and restores project-specific pane/document state. Consolidate without destroying persistent MapLibre/Three/Cesium WebGL contexts or breaking old saved layouts.
6. **An Ask event is not yet proof of a universal Ask dock.** The assistant defines `GEOAI_ASK_EVENT` and `GEOAI_PIN_EVENT`; version 1.0.7 must verify an always-available dock follows the selected project/layers and restores the same task from Map, Edit, Imagery, Worlds, Twin and other workspaces.

**Owner-observed issues requiring reproductions:** poor GeoAI visual hierarchy; Home information overload; QGIS/ArcGIS planning or execution appearing read-only; model/provider availability and host pairing; missing pinned result visibility. The source inspection supports the first two structural diagnoses but **does not prove or dismiss native runtime bugs**. Log each on Windows with actual installed versions, data, and receipts.

## Approved information architecture

**Default Home / Projects:** New Project, Open Project, Recent Projects and Resume Last Work (only real stored records). Compact Import Data, Ask GeoAI and Open Map secondary actions. A small persistent indication of the active project's name/save state is enough. Remove the oversized mission flow, long source setup instructions, diagnostics/status grid and repeated feature catalog from Home. Move teaching to **Learn / Tutorials**; Settings owns model runtimes, network permission, tokens and SDK/MCP configuration. Project diagnostics live in a contextual issue panel.

**Default Ask GeoAI (everywhere):** one prompt with the placeholder **“What would you like to do with your project?”**; four to six **currently registered** example actions; a compact current project / source layers / CRS / model-or-manual readiness strip; the current conversation and task stage. One optional pinned/right-side dock can move left, resize, close and reopen. An expanded dedicated GeoAI workspace is still available for experts, but it must show the same task and state. No duplicate composer or unrelated infrastructure panels on initial open.

**Task flow:** `Question → Understand data → Propose exact tools → Review/approve effect → Run native tool → Inspect real result → Save / export / reopen`. Show one stage at a time; never hide source changes, cost, data disclosure, CRS warnings or approval decisions behind hover-only UI. For failures, show original native error, the specific proposed correction and the need for **new approval** when effects change. If the provider is offline, explain that fact and offer the same manual registered GIS tools, without simulating model output.

**Professional expansion:** source/version metadata, complete tool parameters, selection and measurements, engine and provider routing, raw execution trace, workflow history, schema/receipt inspection, SDK/MCP management and per-feature geometry controls. These are drawers/secondary views, not beginner landing content. Same operation registry and persisted outputs for both modes.

## Concrete implementation boundaries for PR #21

| Work bundle | Reuse and integration target | Acceptance proof |
|---|---|---|
| **UX-01 Home reduction** | Refactor `HomeStart` in `WorkspaceDocuments.tsx`, `premiumHome.css`; retain `publicProjects`, last selected project and save/export actions | Initial view exposes three primary actions and genuine recent work, not duplicate project widgets; accessible at 1280×800 and 150% scaling |
| **UX-02 One Ask dock** | Integrate existing `GeoAIAssistant`, `GeoAIAgentPanel`, `DockviewWorkspace`, `AGOTWorkstationShell` and project context into one shared task view/state | Prompt callable from any workspace; source/layer identity follows user selection; pin, restore, reopen and project switch preserve task without WebGL teardown |
| **UX-03 One honest plan/result path** | Wire `CustomerTaskLauncher` and question composer through existing registered GIS operations, approval, durable jobs and `ProcessingResultsDeck` | Actual loaded source → typed plan with units → explicit approval → native output → Map/Results → persistent reopen, including empty valid outputs |
| **UX-04 Failure/replan** | Reuse existing restricted GeoAI workflow/host SDK authority, source SHA checks and receipts, not a second chat executor | Real failure and correction, new grant for changed effect, no duplicate execution after restart, user-visible diagnostics |
| **HOST-07 parity** | QGIS Python Processing, licensed ArcGIS Pro ArcPy/.NET add-in and standalone wheel; source-verified capability discovery, panel state, provider settings | Same reference 50-m road buffer and intersection produces a saved, map-visible and reopened result in each **installed** host |
| **DOC-07 documentation and release** | Public markdown, source and asset digests, website release metadata selectors, manual installation/upgrade guidance | Version-specific What's New, Getting Started, Known Issues, model/privacy disclosure, SHA checks and website deep links all match the final tagged assets |

Do **not** reimplement GEOS/GDAL/PostGIS, bypass existing grants, permit arbitrary model-generated Python/ArcPy/SQL/shell, invent layer data or claim a model operation succeeded when it only generated prose.

## Required test scripts and customer scenarios

- **Novice planner:** open project; ask *“Which roads are within 100 metres of my schools?”*; choose authorized real roads/schools; verify units/CRS; review and approve buffer/intersection; show output on existing map; save, close and reopen the project with a receipt.
- **Civil engineer:** import a road alignment, edit vertices, calculate a measured corridor, compare with a verified constraint polygon and export a GeoPackage/PDF only when the registered export exists.
- **Environmental specialist:** assess flood exposure using a named, source-licensed hazard layer. With the hazard layer absent, show an honest missing-input state—not a made-up risk score.
- **QGIS and ArcGIS:** run independently installed plugin tools with one source pin, one approval and a real native output. Verify QGIS dock position/green logo, ArcGIS dockpane/green icons, changed input recovery, and real output reattachment after plugin restart.
- **Adversarial cases:** offline model, refused data sharing, unauthorized layer, invalid CRS, source changed after approval, empty successful output, canceled job, model timeout, native engine exception and host reconnect. No silent success and no repeated side effects.

**Gate matrix:** (a) source/contract tests, (b) disposable PostGIS integration, (c) real QGIS Processing, (d) licensed ArcGIS Pro, (e) Windows 11 installed 1.0.7, (f) GPU/3D continuity where relevant, (g) accessibility with keyboard and screen reader, (h) actual asset release and clean upgrade. Each must retain its own evidence; passing (a) does not imply (c)–(h).

## Release-channel contract and website limitation

The public release pages currently contain the source SHA and actual assets, but the 0.6.0 and 1.0.6 release body summaries are brief. Detailed standalone Markdown lives in this repository's [Desktop 1.0.6 notes](../previews/AGOT_DESKTOP_1.0.6_PREVIEW_2.md) and [Hosts/SDK 0.6.0 notes](../previews/GEOAI_HOSTS_0.6.0_PREVIEW_1.md). Website downloads need **explicit links to those documents**, or a trusted release-body rendering update; committing markdown alone cannot silently modify GitHub's published release description. The website source contains a release-selector feed; its final Cloudflare deployment needs a separate live-site check.

For each future candidate, verify exact private source SHA, artifact hashes, program version, native test and acceptance matrix, changelog links, signed/update policies and explicit prerelease flag. Do not call a draft/zero-asset release “latest,” and do not advertise automatic installed plugin updates solely because the website discovered a new ZIP.

## Reference patterns (inspiration, not AGOT functionality)

- [VS Code: Chat view beside the current workspace](https://code.visualstudio.com/docs/agents/run/chat-view) — one conversation alongside real working content, not a replacement for the editor.
- [QGIS 3.44 Processing Model Designer](https://documentation.qgis.org/3.44/en/docs/user_manual/processing/modeler.html) — inspectable algorithm inputs/outputs, grouped steps, validation and reopened partial results.
- [VS Code: tool approvals](https://code.visualstudio.com/docs/agents/run/approvals) — tool permissions are an explicit operator choice.
- [WCAG 2.2, content on hover or focus](https://www.w3.org/WAI/WCAG22/Understanding/content-on-hover-or-focus.html) — help must work through keyboard/focus and be dismissible, not hover-only.

**Decision:** ship **less initial UI and more completed source-to-output capability**. Keep specialist depth; reveal it when needed. Version 1.0.7 and 0.7.0 remain **candidate targets**, not releases.
