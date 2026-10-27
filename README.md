# Geospatial AI Agents in Practice: Sacramento Open Data and Hermes

## Presenter brief

- Speakers: Silas Tom’s and Dara O’Beirne. Speaker labels below use Silas and Dara.
- Speaker assignment: Silas owns the first half (00:00–10:00): Hermes background, workflow fit, harness comparison and GISMap Online. Dara owns the second half (10:00–20:00): the 311 app with 3D columns, permit report, skills, repeatability, performance and closing. Both take Q&A.
- This updates the local speaker notes only; no conference listing or external speaker registration has been changed.
- Accepted session: https://talks.osgeo.org/foss4g-na-2026/talk/GXG78A/
- Published slot: November 3, 2026, 14:00–14:25, Bataglieri. No timezone inferred beyond the program listing.
- Format: 20 minutes of content plus 5 minutes of questions; confirm the conference’s Q&A convention.
- Audience: GIS practitioners who understand spatial workflows but may not know agent harnesses.
- Structure: Silas — Hermes product/background, harness choice and GISMap Online → handoff → Dara — 311 columns app, permits and practical lessons.
- Corrected demo selection: the 311 application with 3D columns, NOT Sacramento 311 Atlas / the point-based 3D Explorer. Exact title and URL remain to be confirmed.
- Thesis: Hermes provides a persistent, extensible way to coordinate GIS work. Results become dependable through bounded tasks, deterministic tools, reusable procedures and human review—not through the harness alone.
- Takeaway: “Let the model interpret the request. Let GIS compute the answer. Make the evidence portable.”
- Scope: revised presentation outline and demo storyboard. This is not a finished slide deck, a new application release, a benchmark, or a completed rehearsal kit.

## Speaker handoff

**At 10:00, Silas to Dara — suggested wording:** “That is Hermes and how it can work with a reusable GIS viewer. Dara will now show the 311 columns application and permit report, then explain the skills, checks and performance choices behind repeatable results.”

**Dara’s opening — suggested wording:** “I’ll start with the 311 columns map, then show the permit reporting workflow. After those, I’ll cover what makes the work repeatable rather than a one-off demo.”

## Slide-by-slide outline

### 1. Hermes for practical GIS work — 00:00–00:30

**Speaker: Silas.**

**On screen:** Talk title, both speakers’ names, and a preview image of the three applications.

**Suggested opening:**

> “We use Hermes as a working assistant around GIS: finding data, coordinating development, checking outputs and helping turn repeated work into reusable procedures. I’ll introduce Hermes and demonstrate GISMap Online. Dara will show the 311 columns app and permit report, then cover repeatability and performance.”

Promise useful outputs and an honest account of the process—not an autonomous GIS analyst or a model leaderboard.

### 2. What is Hermes? — 00:30–02:00

**Speaker: Silas.**

**On screen:** “An open-source agent framework from Nous Research—not a language model and not a GIS engine.”

Explain an **agent harness** as the software that connects a model to tools, context, execution and controls.

Five product capabilities:

- **Tools:** work with files, commands, APIs and browsers within configured permissions.
- **Skills:** load reusable task procedures and supporting resources when needed.
- **Continuity:** persistent memory and session retrieval reduce repeated setup and explanation.
- **Interfaces:** use the terminal or configured messaging integrations such as Telegram.
- **Operations:** schedule work and connect additional tools through MCP or other integrations.

Hermes supports multiple model providers. Provider choice affects quality, cost, privacy and availability; switching providers does not guarantee equivalent results.

**Visual:** One sanitized terminal or messaging example beside the five labels. Do not show private chat history, credentials or personal filesystem paths.

**Key distinction:** Skills preserve procedures; they do not retrain model weights. Persistent memory can be stale and must not replace current source evidence.

### 3. A GIS setup: Mercator — 02:00–03:00

**Speaker: Silas.**

**On screen:** “A general-purpose agent, configured for GIS.”

Mercator is Dara’s GIS-focused Hermes profile, not another model or a separate GIS engine.

```text
Dara: question, constraints and approvals
                    ↓
Hermes / Mercator: context, skills and coordination
           ↙                         ↘
Tested GIS tools                 Coding agents
Python / SQL / APIs              Claude Code / Codex
           ↘                         ↙
        Data artifacts, application and tests
                    ↓
          Human review and approved release
```

**Talk points:**

- GIS skills encode source checks, CRS rules, joins, map behavior and acceptance criteria.
- Python, SQL and GIS libraries perform the calculations.
- Claude Code or Codex can develop and test the implementation; Hermes need not replace them.
- Completed scripts can be reused without asking a model to regenerate them.
- Profiles separate context and configuration. They are not OS security sandboxes.

**Transition:** “I’ll demonstrate the reusable viewer first. Dara will then show the 311 columns app and recurring report.”

### 4. What the agent does—and what it does not — 03:00–04:00

**Speaker: Silas.**

**On screen:** Request → inspect → compute → present → verify.

- **AI assistance:** translate the request into a bounded task; inspect schemas; help develop code; explain recorded results; coordinate checks.
- **Deterministic GIS:** date filtering, joins, geometry processing, spatial aggregation, counts and measurements.
- **Human responsibility:** choose the question, judge the interpretation, review the experience and approve publication.

Introduce the source-to-output pattern:

> Public/approved data → tested processing → compact artifacts → web map/report → evidence and limitations.

A public ArcGIS REST source can feed an open-source processing and presentation stack. Source hosting, software licensing and data reuse rights are separate questions.

Distinguish **built with AI assistance** from **contains runtime AI**. None of the demos requires a claim that a language model answers every visitor’s query.

### 5. Why Hermes—and when not to use it — 04:00–07:00

**Speaker: Silas.**

**On screen:** “Choose for the workflow, not the logo.”

**Why Hermes fits this practice:**

- GIS work crosses research, data acquisition, analysis, development and recurring reporting—not just one repository.
- Persistent context, reusable skills, messaging and scheduling are available in one configurable agent environment.
- Model-provider flexibility and an open-source framework make it possible to adapt the setup.
- Hermes can coordinate provider-native coding tools rather than forcing every task through its own implementation loop.

**When Claude Code is a sensible primary tool:**

- The job is focused repository development, debugging, testing or code review in a Claude-centered workflow.
- Its existing terminal/IDE/desktop/cloud integrations meet the need without another coordination layer.

**When Codex is a sensible primary tool:**

- The job is focused implementation, testing or review in its local/IDE/cloud workflows.
- Scripting and non-interactive execution fit the development process.

**Fairness checks:**

- Claude Code and Codex also support reusable skills and tool integrations. Do not claim these are unique to Hermes.
- Claude Code documents memory, channels, routines and scheduled tasks; do not describe it as terminal-only or unable to automate.
- Codex CLI is open source under Apache-2.0. “Open source versus closed source” is not a valid Hermes-versus-Codex CLI distinction.
- The open-source status of a harness does not determine the licensing or data handling of its models, hosted services or basemaps.
- Hermes adds configuration, maintenance and coordination overhead. For one bounded code change, direct use of the coding tool may be simpler.

**Suggested line:**

> “I choose Hermes for continuity across the GIS workflow. I still use Claude Code and Codex for development. It is a coordination choice, not a claim that one harness wins every task.”

### 6. Demo 1: GISMap Online — 07:00–10:00

**Speaker: Silas.**

**User-supplied URL:** http://gismap.online/

**Public documentation:** https://www.gismap.online/guides/ai-agents/

**Purpose:** Show a reusable browser GIS workspace rather than another single-purpose application. The product describes opening ArcGIS REST services, GeoJSON and local geospatial files for 2D/3D inspection, styling and export.

**Proposed three-minute sequence:**

1. Open one prepared public layer or a small approved local GeoJSON; avoid starting with an empty workspace and searching for data on stage.
2. Inspect an attribute and apply one meaningful style. Explain the field and units, including any no-data codes.
3. Briefly change the camera/view to demonstrate the spatial context without spending the segment navigating.
4. Show the agent connection: a validated map specification can be encoded in a shareable URL. Open a prepared link and explain how Hermes can inspect metadata, construct the specification and verify the result.
5. End on the reusable outcome: a map link or project that can be reopened, not a new deployment for each question.

**Suggested illustrative request:** “Open this approved public layer, style the selected numeric field, preserve the publisher’s no-data codes, and prepare a shareable map. Verify the rendered layer and legend before returning the link.” This is a proposed rehearsal prompt, not a historical transcript or an already executed run.

**Documented agent paths:** Text-only link generation; code-assisted source inspection and specification validation; browser automation through the exposed application API. These are documented capabilities, not interactions independently tested in this outline revision.

**Repeatability lesson:** Capture the source, filter, renderer/classes and view state. A saved style does not freeze a live dataset; preserve the source vintage or approved snapshot separately.

**Performance lesson:** Use source inspection and structured map specifications before unnecessary browser clicking. Browser checks still matter: a valid specification does not prove correct rendering.

**Boundary:** Sharing is a separate user action. Only approved public data and non-sensitive configuration should enter a share link; no tokens, private endpoints or sensitive attributes. No link was published or shared externally in this task.

**FOSS4G framing:** The site calls itself open source, while its interface identifies the ArcGIS Maps SDK. Distinguish the application’s license from the SDK and hosted-service terms; do not describe the whole stack as FOSS without checking licenses. Build provenance for GISMap was not established from this session search, so avoid unsupported model-by-model authorship claims.

### 7. Demo 2: the 311 app with 3D columns — 10:00–13:00

**Speaker: Dara.**

**Selected app:** The 311 visualization with 3D columns, as corrected by Dara. This is not Sacramento 311 Atlas or the point-based Sacramento 311 3D Explorer. Its exact title and URL remain unconfirmed; do not reuse the rejected Explorer URL.

**Purpose:** Lead Dara’s half with the spatial visualization, then connect it to the data and development workflow.

**Proposed three-minute demonstration, subject to the actual app’s controls:**

1. Open a rehearsed view with the columns visible and establish the dataset and reporting period.
2. Explain exactly what a column represents and what height and color encode. Confirm the spatial unit, units, scaling and aggregation before presenting; do not assume raw counts, rates, grid cells or a specific rendering library.
3. Use one verified interaction to explore the pattern, such as selecting a column or changing an available filter. Confirm the actual interaction during rehearsal rather than promising controls not yet inspected.
4. Connect the displayed result to its source and limitations. 311 reporting activity is not a direct measure of population, unmet need or departmental performance.
5. Briefly explain Hermes’ role in the build using verified project evidence, then transition to the recurring permit report.

**Performance connection:** Discuss aggregation, rendering limits and camera/interaction responsiveness only as supported by the selected implementation. Do not carry over the rejected Explorer’s point offsets, source partitions, acquisition counts, Ledger or sampling behavior.

**Readiness:** App identity and URL are pending. No current browser or analytical acceptance claim is made for this demo. Reserve the segment now; finalize the exact click path after identifying the correct application.

### 8. Demo 3: Sacramento permit report — 13:00–15:00

**Speaker: Dara.**

**URL:** https://sacbuildingpermits.vercel.app

**Purpose:** Finish the demos with practical recurring value: a month of permit data turned into a reviewable report.

**Proposed two-minute sequence:**

1. Establish the archived June 2026 reporting period and summary.
2. Show the parcel outlines and clustered map markers, explaining what each represents.
3. Show an unmatched record in the table. The displayed report lists 1,597 permits, 1,568 parcel-matched and 29 unmatched; these are archived report figures, not a fresh analysis.
4. Explain the repeatable pattern: retrieve → validate dates/keys → associate parcels → calculate → render → review.

**Hermes contribution:** Assistance developing and iterating the reporting workflow. Do not claim the refresh schedule is currently active or all prose was generated autonomously without corresponding evidence.

**GIS lesson:** Issued-permit sources are non-spatial tables; parcel associations supply geography. Issued does not mean completed, valuation is not actual spending, and parcel geometry is not a surveyed construction footprint.

**Performance lesson:** Prepare the report once rather than requiring model inference for each reader interaction.

**Transition to practice:** “Three different products, the same discipline: known sources, explicit rules, reusable tools and outputs we can inspect.” The spatial owner brief can summarize any of them: question, owner, period, source, map, findings, exclusions and next decision.

### 9. Which skills should you use? — 15:00–16:00

**Speaker: Dara.**

**On screen:** Source → data QA → analysis → map → verification.

Keep the spoken version to five categories: source validation, data QA, analysis, presentation and testing. The package names below are reference notes, not a list to read aloud in this one-minute segment:

Show a small task-focused bundle from the configured Mercator library:

- **`arcgis-rest-service-validator`:** inspect service/layer metadata, fields, query behavior and completeness before treating a source as usable.
- **`geospatial-data-qa-pipeline`:** validate geometry, CRS, duplicates, nulls and record accounting before analysis or publication.
- **`geopython-analysis-engineering`:** turn Python spatial work into reusable modules, fixtures and reproducible environments.
- **Presentation-specific skills:** `arcgis-maps-sdk-javascript` for ArcGIS scene/view behavior; `web-map-open-source` for Leaflet/MapLibre work. Choose by the actual application, not by a blanket stack preference. Neither skill changes SDK, data or basemap licensing terms.
- **`gis-testing-performance-observability`:** check the user journey, data agreement, failure states and measured performance.

Optional additions for the task: cartographic review, code-agent delegation, and clear technical writing. Do not preload an entire catalog because it exists.

**Important packaging note:** These names describe Dara’s configured library, not a guaranteed default Hermes installation. Several packages have commercial license terms. Do not distribute their text or present them as freely installable conference handouts without permission. Attendees can implement the same procedural categories with appropriately licensed skills.

**Show an illustrative skill contract, not a wall of instructions:**

```text
Task: create a monthly permit report
Inputs: approved source, reporting month, parcel source
Rules: inspect date types; preserve unmatched records
Outputs: report, map-ready data, exclusions and source manifest
Checks: counts reconcile; map and table agree; rerun is safe
Stop: source schema changed or an input is unavailable
```

**Speaker line:** “A good skill contains the checks and stop conditions—not just the happy path.”

### 10. How to get repeatable results — 16:00–17:00

**Speaker: Dara.**

**On screen:** “Repeatability comes from a contract, not a lucky conversation.”

Use the one-minute slide to name five practices; retain the detail below as speaker reference:

1. **Define the task contract.** User, question, geography, period, output and explicit non-goals. State what counts as acceptance.
2. **Freeze the moving parts.** Record data snapshot, source retrieval time, timezone, code revision, dependencies, parameters, skill revisions and actual model identity where available.
3. **Reuse deterministic execution.** Stable scripts and explicit inputs; no hidden notebook state; no new implementation for every refresh. Make reruns safe.
4. **Test the same evidence.** Known-answer fixtures, boundary/null/empty cases, counts, joins, geography, browser interaction and independent review.
5. **Save the artifact and provenance.** Preserve commands, manifest, test results and unresolved limitations. Bind approval to the revision actually tested.

Model output can vary even when the model is pinned. The goal is stable acceptance criteria and reproducible analytical results—not identical prose.

**Illustrative improved request, not a historical transcript:**

> “Using the approved snapshot and existing reporting script, produce the selected month’s report. Preserve unmatched records. Do not change the date or join rules. Reconcile source and output counts, test the map and table, and stop before publication.”

**One brief failure lesson:** A previous tree prototype passed builds and tests while its polygons failed to render. A passing build is not GIS acceptance. Do not let this become a third lengthy demo.

### 11. Performance: improve the workflow, not just the model — 17:00–19:00

**Speaker: Dara.**

**On screen:** Three separate budgets: agent, GIS pipeline, application.

**Agent efficiency:**

- Use APIs, scripts and compact structured results before browser scraping when possible.
- Filter and aggregate near the data; do not send entire feature collections into model context.
- Load relevant skills and hand off bounded tasks rather than duplicating long conversations.
- Parallelize independent work only. Extra agents add coordination cost and can create rework.
- Set time, request, output and retry limits. Stop unsupported or unavailable model lanes rather than silently changing them.
- Use script-only scheduled execution when no reasoning is needed; Hermes documents a no-agent cron mode.

**GIS pipeline performance:**

- Retrieve required fields, rows and geography; honor pagination and reconcile counts.
- Use appropriate spatial indexes and vectorized operations before adding distributed compute.
- Cache approved source snapshots and derived aggregates with explicit freshness rules.
- Separate heavy processing from presentation. The permit report illustrates prepared output; the 311 columns demo should illustrate its verified aggregation and rendering choices, without assuming the architecture before inspection.

**Application performance:**

- Use clustering, generalized display geometry or vector tiles when the workload warrants them.
- Lazy-load details; keep map, table and filter state consistent.
- Inspect actual geometry rendering, cold/warm load behavior, mobile interaction and failures of external basemaps.

**What to measure:**

- Agent: wall-clock time to an accepted result, model/tool cost, retries and human correction time.
- Pipeline: input volume, runtime, peak memory, completeness and data freshness.
- App: payload size, time until usable map data renders, filter latency and error rate.

No quantified Hermes-versus-Claude-Code-versus-Codex benchmark was performed for this outline. Do not claim a percentage improvement. A fair comparison needs equivalent inputs, quality gates, multiple runs and disclosure of model, permissions, environment and warm caches.

### 12. Start with one workflow — 19:00–20:00

**Speaker: Dara.**

**On screen:** One dataset. One repeatable question. One reviewed output.

**Attendee exercise:** Pick a monthly report you already produce. Use a public or approved snapshot, write down the validation rules, and ask the agent to run the existing tools against that contract. Compare the result with a known answer before extending access or scheduling anything.

Keep the MVP to that bounded workflow. A multi-agent platform is not a prerequisite.

Close with:

> “The useful improvement is not an agent that sounds confident. It is a workflow you can run again, inspect and correct.”

Final slide: official Hermes documentation and the three selected demo links after their exact demonstration paths pass rehearsal. Add a handout/repository QR code only after an authorized package is actually published and tested.

### Questions — 20:00–25:00

**Speakers: Silas and Dara.** Silas leads product/harness and GISMap questions; Dara leads 311, permits, skills and performance questions.

Keep the final slide visible. Likely questions: data privacy, local models, skill portability, model cost, framework maintenance and government/on-prem deployment.

## Demo evidence and readiness

**Selected lineup:** GISMap Online (Silas) → 311 app with 3D columns (Dara; exact URL pending) → Sacramento permit report (Dara). Both the Change Instrument and the point-based 311 Atlas/Explorer are excluded.

- **311 columns app:** Dara explicitly rejected the previously selected point-based Explorer. Its historical URL and source facts do not apply. The correct columns app needs identification and an exact demonstration-path check before rehearsal.
- **GISMap Online:** The supplied homepage, examples catalog and agent guide were retrieved. The guide documents map specifications, source inspection, styling, share links and browser automation. No dataset was loaded, map link generated, export exercised or runtime AI connection tested in this revision. Those remain rehearsal checks.
- **Permit report:** The previous outline preparation fetched the archived June report and included a focused browser check of rendered Leaflet tiles and markers/clusters. No new data pipeline run was performed. Freeze the demonstrated page so a homepage update does not change the reporting month unexpectedly.

The outline is revised; a live-demo readiness assessment and recording kit are not yet complete. No application changes, model configuration changes or deployments are part of this revision.

## Five preparation tasks

1. Freeze one short interaction path per app: GISMap source/style/share state for Silas; the correct 311 columns view and verified interaction for Dara; permit month/map/unmatched record for Dara.
2. Verify all three paths in a browser, including actual geometry, relevant counts, source coverage, loading/error behavior and external basemap dependencies. Verify any exports or shared links before promising them on stage.
3. Record short walkthroughs and capture sanitized screenshots as fallbacks. Prepare local playback rather than depending entirely on venue Wi-Fi or live model inference.
4. Assemble a concise takeaway: task contract, validation checklist and appropriately licensed example skill. Keep commercial skill bodies, private transcripts and credentials out of public materials.
5. Rehearse to the timing budget: Silas 10 minutes (Hermes/context 4, harness comparison 3, GISMap demo 3); Dara 10 minutes (311 columns demo 3, permits demo 2, skills/repeatability 2, performance 2, closing 1); joint Q&A 5 minutes. Rehearse the handoff at 10:00. Verify conference expectations and every final link.

Three demos fit only if each demonstrates one bounded workflow. Cut feature touring, not the skills/repeatability discussion that makes the talk useful. Do not perform installations, sign-ins, fresh app builds or large downloads on stage.

## Safety and public-sector discussion notes

- Start with read-only public or explicitly approved data.
- Separate data inspection from authoritative edits, sending messages and publication approval.
- Treat service attributes, websites and retrieved documents as untrusted data, not instructions.
- Keep credentials and restricted data out of prompts, screenshots and logs.
- Local hosting of a harness does not prove local-only processing if a remote model or tool is configured.
- Use real filesystem, database, network and sandbox controls; profile separation alone is not security isolation.
- Review data rights, basemap terms, dependencies and skill provenance independently.
- Do not infer departmental performance, need or severity from 311 counts; do not infer completed construction or economic impact from permit valuations.

## Research references

- Accepted session: https://talks.osgeo.org/foss4g-na-2026/talk/GXG78A/
- Hermes overview: https://hermes-agent.nousresearch.com/docs/
- Hermes skills: https://hermes-agent.nousresearch.com/docs/user-guide/features/skills/
- Hermes profiles: https://hermes-agent.nousresearch.com/docs/user-guide/profiles/
- Hermes scheduled tasks, including no-agent mode: https://hermes-agent.nousresearch.com/docs/user-guide/features/cron
- Claude Code overview, memory and automation links: https://code.claude.com/docs/en/overview
- Claude Code skills: https://code.claude.com/docs/en/skills
- Codex CLI: https://developers.openai.com/codex/cli
- Codex skills: https://developers.openai.com/codex/build-skills
- Codex source and license: https://github.com/openai/codex
- Permit report: https://sacbuildingpermits.vercel.app
- 311 columns application: exact title and URL pending confirmation from Dara; do not substitute the point-based Explorer.
- GISMap Online (user-supplied): http://gismap.online/
- GISMap agent guide: https://www.gismap.online/guides/ai-agents/
- GISMap examples: https://www.gismap.online/examples/

Product capabilities evolve; recheck the official comparison references before final slide publication. Comparative recommendations above express workflow fit, not measured superiority.
