# Geospatial AI Agents in Practice: Sacramento Open Data and Hermes

## Presenter brief

- **Speakers:** Silas Toms and Dara O’Beirne. Speaker labels below use Silas and Dara.
- **Session:** FOSS4G North America 2026. The published program lists November 3, 2026, 14:00–14:25, Bataglieri. Use the conference program’s displayed time convention.
- **Accepted session:** https://talks.osgeo.org/foss4g-na-2026/talk/GXG78A/
- **Format:** 20 minutes of presentation and demonstrations, followed by 5 minutes of questions.
- **Audience:** GIS practitioners, civic technologists and public-sector teams who understand spatial workflows but may be unfamiliar with agent software.
- **Current deck:** 22 slides. Slides 1–18 form the presentation, including the questions slide. Slides 19–22 are hidden backup slides.
- **Speaker assignment:** Silas presents slides 1–8, from 00:00 to 10:00. Dara presents slides 9–17, from 10:00 to 20:00. Both use slide 18 for questions.
- **Order:** Hermes, task execution, memory, Mercator, responsibilities, tool comparison and GISMap Online. Then Service Terrain, the September permit report, Obsidian as a second brain, reusable project knowledge, procedures, repeatability, cost, performance and the closing exercise.
- **Second-brain placement:** “Obsidian as a second brain” and “Project knowledge in a GIS workflow” now follow the permit report directly, as slides 11 and 12.
- **Central point:** Hermes coordinates work across models, tools and project information. GIS scripts perform the calculations. People define the question, judge the result and approve its release.
- **Takeaway:** Keep the source, processing rules and review evidence with the output so another person can inspect or repeat the work.
- **Terminology:** Call Mercator **the GIS agent profile**. Distinguish Hermes Agent, the software runtime, from the separately named Hermes model family. Explain specialist terms when they first appear.

This outline follows the reordered PowerPoint. The timing below replaces the earlier outline’s allocation and accounts for the added Hermes and second-brain material. Detailed reference points support rehearsal and questions. They are not a script to read in full during the talk.

## Timing and speaker plan

| Slide | Title | Speaker | Elapsed time | Budget |
| --- | --- | --- | --- | --- |
| 1 | Geospatial AI Agents in Practice | Silas | 00:00–00:30 | 0:30 |
| 2 | Hermes | Silas | 00:30–01:20 | 0:50 |
| 3 | How Hermes carries out a task | Silas | 01:20–02:00 | 0:40 |
| 4 | Memory, skills and project knowledge | Silas | 02:00–02:40 | 0:40 |
| 5 | Mercator | Silas | 02:40–03:30 | 0:50 |
| 6 | The division of work | Silas | 03:30–04:10 | 0:40 |
| 7 | Choosing a working environment | Silas | 04:10–07:00 | 2:50 |
| 8 | GISMap Online | Silas | 07:00–10:00 | 3:00 |
| 9 | Sacramento 311 | Dara | 10:00–12:15 | 2:15 |
| 10 | Sacramento permit report | Dara | 12:15–14:15 | 2:00 |
| 11 | Obsidian as a second brain | Dara | 14:15–15:00 | 0:45 |
| 12 | Project knowledge in a GIS workflow | Dara | 15:00–15:45 | 0:45 |
| 13 | Reusable GIS procedures | Dara | 15:45–16:30 | 0:45 |
| 14 | What a repeatable run records | Dara | 16:30–17:15 | 0:45 |
| 15 | Agent time and cost | Dara | 17:15–18:00 | 0:45 |
| 16 | Processing and map performance | Dara | 18:00–19:00 | 1:00 |
| 17 | A first workflow | Dara | 19:00–20:00 | 1:00 |
| 18 | Questions | Both | 20:00–25:00 | 5:00 |
| 19 | Monthly permit report | Backup | As needed | Outside main talk |
| 20 | Mercator skill references | Backup | As needed | Outside main talk |
| 21 | Public-sector use | Backup | As needed | Outside main talk |
| 22 | Hermes setup and access | Backup | As needed | Outside main talk |

## Speaker handoff

**At 10:00, Silas to Dara, suggested wording:**

> “That is the Hermes setup and one way to use it with a reusable GIS viewer. Dara will now show Service Terrain and the permit report, then explain how project notes, procedures and checks help us repeat the work.”

**Dara’s opening, suggested wording:**

> “I’ll start with the 311 map and the September permit report. Then I’ll show where we keep the project knowledge and how we use it when the same work comes around again.”

## Slide-by-slide outline

### 1. Geospatial AI Agents in Practice — 00:00–00:30

**Speaker: Silas.**

**On screen:** “Geospatial AI Agents in Practice,” the subtitle “Sacramento Open Data and Hermes,” Silas Toms and Dara O’Beirne, and the Sacramento Tower Bridge photograph.

**Purpose:** Establish the practical scope and the two speakers’ roles.

**Suggested opening:**

> “We use Hermes around GIS work: finding data, coordinating development, checking outputs and turning repeated work into procedures we can use again. I’ll introduce the setup and GISMap Online. Dara will show two Sacramento examples and explain how we keep the work documented and reviewable.”

Set expectations for concrete applications, source checks and human judgment. The examples show workflows and development assistance. They do not establish that every application runs a language model for its visitors.

**Visual:** Retain the current cover photo and corrected names. No extra introductory diagram is needed.

### 2. Hermes — 00:30–01:20

**Speaker: Silas.**

**On screen:** “Hermes Agent, the open-source runtime” and “Connects a chosen language model to tools and reusable procedures.” The supplied Hermes profile image appears beside four capabilities.

**Purpose:** Explain the software’s role before introducing the GIS profile.

**Talk points:**

- A language model interprets the request and proposes actions. Hermes supplies the surrounding software that can execute permitted tool requests and keep working context.
- Tools can work with files, commands, APIs and browsers, subject to the configuration and host’s access controls.
- Skills are written procedures with checks and stop conditions.
- Saved details support continuity between sessions, but they need correction when a project or source changes.
- Recurring work can use scheduling. A routine script is sufficient when the task needs no model reasoning.

Briefly distinguish **Hermes Agent** from the **Hermes model family**. This presentation concerns the agent runtime and its GIS workflow. Do not describe the profile image as proof of a specific model configuration.

**Key qualification:** Model-provider choice affects cost, availability and data handling. Running the agent software locally does not by itself keep every request local.

**Transition:** “The useful part is the sequence of actions and checks around a request.”

### 3. How Hermes carries out a task — 01:20–02:00

**Speaker: Silas.**

**On screen:** Four stages: establish the task, use a tool, inspect the result, finish and report.

**Purpose:** Give the audience a concrete explanation of an agent’s working loop.

Use a short GIS example through all four stages:

1. **Establish the task:** Identify the reporting month, approved source and expected report. Resolve missing information before proceeding.
2. **Use a tool:** Inspect an ArcGIS service, read an approved file or run an existing extraction script.
3. **Inspect the result:** Check returned records and errors. Compare the map with the data rather than accepting a successful command as proof.
4. **Finish and report:** Reconcile the output with the request, preserve limitations and leave a result for human review.

Explain that the next action depends on the previous result. An error may require a revised step or a stop, rather than repeated attempts without a limit.

**Boundary:** Time, cost and retry limits belong to the task. A missing source or failed acceptance check can be a valid reason to stop.

### 4. Memory, skills and project knowledge — 02:00–02:40

**Speaker: Silas.**

**On screen:** Current conversation, saved memory, skills and Obsidian vault.

**Purpose:** Separate four kinds of information that can otherwise sound like one feature.

| Information | What it holds | GIS example |
| --- | --- | --- |
| Current conversation | The current request and recent tool results | The selected reporting month and an error returned by a query |
| Saved memory | Compact facts and conventions reused in later sessions | A project location or a preferred output convention |
| Skills | Procedures for doing a task | How to validate a service and reconcile extracted records |
| Obsidian vault | Longer notes, references and recorded decisions | Source definitions, join decisions and lessons from prior reports |

The built-in memory is bounded and associated with a profile. Skills load relevant procedural information when needed. An Obsidian vault is a separate collection of files. Reading or searching it requires appropriate configuration and permission.

**Suggested line:**

> “The conversation holds today’s task. Memory holds a few durable details. Skills hold procedures. The notebook holds the longer project record.”

Do not imply that saving notes retrains the model, that all notes are automatically available, or that retrieved information is necessarily correct. Dara will return to Obsidian after the permit example.

### 5. Mercator — 02:40–03:30

**Speaker: Silas.**

**On screen:** “Mercator” with the subtitle **“The GIS agent profile.”** Four rows describe request limits, GIS procedures, existing tools, and review records.

**Purpose:** Explain how the general agent environment becomes useful for a defined GIS workflow.

**Talk points:**

- The profile keeps settings, project information and reusable procedures together.
- A request names approved inputs, the reporting period, expected outputs and actions requiring approval.
- GIS procedures specify coordinate systems, identifiers, date fields, missing values and join rules.
- Python, SQL and GIS libraries perform calculations. Claude Code or Codex can help develop and test the implementation.
- A person checks the actual map, reconciles the counts and reviews the report before release.

Completed scripts can run again without regenerating their implementation for every reporting cycle.

**Boundary:** A profile organizes configuration and state. Filesystem, database and network controls determine what the running software can access. Profile separation does not replace those controls.

**Transition:** “That still leaves a clear division between what the model assists with, what the GIS tools calculate and what people decide.”

### 6. The division of work — 03:30–04:10

**Speaker: Silas.**

**On screen:** Three columns headed “Model and agent,” “GIS tools” and “People.”

**Purpose:** Make responsibility explicit.

- **Model and agent:** Interpret the question, inspect fields, assist code development, explain errors and summarize recorded results. Stop when a missing input or assumption needs review.
- **GIS tools:** Apply date filters and join rules, process geometry, calculate measurements and produce files and counts that another person can inspect.
- **People:** Choose the question and suitable sources, decide whether the map answers the question, assess limitations and approve authoritative changes or public release.

Explain the working pattern in ordinary language: approved data enters tested processing, which produces compact map or report files and a record of the checks.

**Important distinction:** AI assistance during development does not require a model call for every visitor to the finished map. A prepared report can remain a conventional web page.

**FOSS4G connection:** A source hosted through ArcGIS REST can feed an open-source processing stack. Source hosting, software licenses, data rights and basemap terms remain separate questions.

### 7. Choosing a working environment — 04:10–07:00

**Speaker: Silas.**

**On screen:** The editable comparison table for Hermes, Claude Code and Codex.

**Purpose:** Explain the workflow choice without presenting a product ranking.

**Hermes:** Fits work that continues across source research, processing, application development and recurring reports. Project details, procedures and messaging can support that continuity. It also introduces setup and maintenance responsibilities.

**Claude Code:** Fits repository development, debugging, testing and review in an existing Claude development environment. Its available integrations, skills and automation may already meet the need.

**Codex:** Fits implementation, testing and review, including scripted development and repeated code tasks. Direct use of the coding workflow may be sufficient for a focused change.

**Suggested explanation:**

> “I use Hermes when I want continuity across the wider GIS workflow. I still use Claude Code and Codex for development. The choice depends on the job and the setup we already maintain.”

**Reference detail for questions:**

- Reusable skills and tool integrations are not exclusive to Hermes.
- Claude Code also documents memory and automation. Avoid describing it as terminal-only or unable to support recurring work.
- Codex CLI is open source under Apache-2.0. Do not use a simple open-versus-closed distinction to compare Hermes with Codex CLI.
- A framework’s license does not establish the terms of its model providers, SDKs, data or basemaps.
- Provider flexibility does not guarantee equivalent output quality when changing models.
- For one bounded code change, an additional coordination layer may add more maintenance than value.

**Evidence limit:** No equivalent-input, repeated-run speed or accuracy benchmark accompanies this presentation. Do not claim that one environment is faster, cheaper or more accurate by a measured percentage.

**Timing:** Keep the table discussion focused. Start GISMap Online at 07:00.

### 8. GISMap Online — 07:00–10:00

**Speaker: Silas.**

**On screen:** The supplied portrait screenshot of the GISMap Online welcome screen, with text about source selection, field styling and saved views.

**Application:** https://www.gismap.online/

**Agent guide:** https://www.gismap.online/guides/ai-agents/

**Purpose:** Demonstrate a reusable browser mapping workspace and a map that someone else can reopen.

**Three-minute demonstration plan:**

1. Open one prepared public layer or a small approved GeoJSON. Establish its publisher and date.
2. Inspect a useful field. State its units and how missing values appear.
3. Apply one meaningful style and inspect the rendered layer and legend.
4. Open a prepared saved view or map link. Explain which filters, classes and camera settings it preserves.
5. End on the reusable result rather than touring every control.

**Illustrative request for rehearsal:**

> “Open this approved layer, style the selected field and check the legend before returning a map link. Preserve the source’s missing-value codes and record the source date.”

This is a proposed task, not a quoted transcript of an executed run.

**Repeatability lesson:** Saving a map view does not freeze a changing source. Record the source vintage or preserve an approved snapshot separately.

**Performance lesson:** Inspect structured source metadata and prepare the map specification before relying on repeated browser actions. Still inspect the rendered geometry.

**Current evidence:** The deck contains the supplied welcome-screen image. It is not an image of a completed analysis. The application could not render its map in the review environment because WebGL was unavailable, so a complete interactive path remains a rehearsal task.

**Release boundary:** Keep credentials, private endpoints and sensitive attributes out of shared links. Explain the application, SDK and service terms separately.

**Handoff:** Use the agreed wording and give Dara control at 10:00.

### 9. Sacramento 311 — 10:00–12:15

**Speaker: Dara.**

**On screen:** The supplied **Service Terrain** screenshot, headed “Public 311 Snapshot · Sacramento, CA,” with colored hexagonal columns. Adjacent text covers column meaning, comparisons and record checks.

**Selected application:** Service Terrain. The exact live URL has not been supplied. Use this identified columns visualization rather than a different point-based 311 application.

**Purpose:** Start Dara’s section with a spatial example and explain how interpretation depends on data definitions.

**Two-minute-fifteen-second demonstration plan:**

1. Open the prepared view and establish the source and reporting period.
2. Explain the spatial unit and the precise meaning of height and color using the application’s legend or information panel.
3. Demonstrate one rehearsed interaction, such as inspecting a column or an available filter, only if the application actually supports it.
4. Relate the displayed values to the source records and explain exclusions or repeated reports.
5. End on what the visualization helps a reviewer inspect, then move to the permit report.

**Interpretation:** A 311 record represents a submitted service request. Reporting access, habits, repeat reports and the chosen period can all affect patterns. Counts alone do not establish unmet need, severity, population or departmental performance.

**What remains to verify:** The screenshot identifies Service Terrain and shows hexagonal columns. It does not establish the reporting period, height or color definitions, aggregation rules, or implementation library. Confirm those before making analytical claims.

**Performance discussion:** Explain aggregation, payload or renderer choices only when supported by the actual project. Do not transfer technical details or counts from another 311 application.

**Fallback:** Use the supplied screenshot to discuss the structure and required checks if the live view is unavailable.

### 10. Sacramento permit report — 12:15–14:15

**Speaker: Dara.**

**On screen:** Both supplied September report images: the summary and the parcel map with its legend and attribution. Large editable figures show 1,445 permits, 1,411 parcel matches, 34 unmatched and $116.35 million in declared valuation.

**Application:** https://sacbuildingpermits.vercel.app

**Period:** September 2026 issued permits. This supersedes the June example in the original outline.

**Report figures from the supplied snapshot:**

| Measure | Value |
| --- | --- |
| Issued permits | 1,445 |
| Parcel-matched records | 1,411 |
| Unmatched records | 34 |
| Declared valuation | $116,352,642.84, shown as $116.35m on the slide |
| Largest permit | $20,092,704.25, shown as $20.09m |
| Largest permit identifier and address | COM-2509363, 1133 Corporate Way |
| Report refresh | October 26, 2026 |
| Latest returned status date stated in the report | September 27, 2026 |

**Two-minute demonstration plan:**

1. Establish September and the displayed refresh date. These are figures from the supplied report snapshot, not a new extraction performed for the presentation.
2. Point out that 1,411 matched records plus 34 unmatched records reconcile to the 1,445 total.
3. Show parcel outlines, clusters and the legend. Explain that City permit records and county parcel geography have different roles.
4. Retain unmatched records in the accounting. Show an example only if a rehearsed table or record view supports it.
5. Briefly describe the recurring sequence: retrieve approved records, check dates and keys, associate parcels, calculate the summary, render the report and review it.

**Interpretation limits:** Issued permits do not establish completed construction. Declared valuation does not measure actual expenditure. Parcel outlines do not establish the construction footprint. The snapshot states that later dates beyond September 27 are not represented, and current status/date fields can change historical totals.

**Hermes contribution:** Describe assistance developing and iterating the workflow. An active automatic refresh schedule or autonomous authorship of all report prose requires separate evidence.

**Transition:**

> “The report also depends on decisions we need next month: which date field to use, how the parcel join works and what to do with unmatched records. That is where the project notebook comes in.”

### 11. Obsidian as a second brain — 14:15–15:00

**Speaker: Dara.**

**On screen:** An Obsidian source-note screenshot from the supplied portfolio deck. It shows an article’s source URL, author, dates, tags, related topics and captured summary. The slide describes a linked project notebook.

**Purpose:** Show where longer project knowledge lives between conversations and reporting cycles.

Explain “second brain” as a practical name for an organized external notebook. In this workflow, it retains research, decisions, source definitions and procedures that would be difficult to reconstruct from chat history alone.

**Talk points:**

- An Obsidian vault is a folder of local Markdown notes. Other text editors can read the files.
- Source links and dates help a reader distinguish original evidence from a written summary.
- Links and tags connect a source note to project decisions and reusable procedures. Backlinks reveal other notes that refer to the current note.
- The captured note provides traceability. It does not make the underlying article’s claims automatically correct.

**Suggested line:**

> “The value is keeping the explanation with the source, so we can return to the decision and check why we made it.”

**Boundary:** The vault is separate from Hermes’ compact saved memory. Access, search and writes require configuration. A local file can still be included in a request to a remote model if that is how the system is configured.

### 12. Project knowledge in a GIS workflow — 15:00–15:45

**Speaker: Dara.**

**On screen:** Capture the evidence, retrieve for the task, check the output and keep the lesson. The Obsidian logo identifies the notebook component.

**Purpose:** Connect the second-brain explanation directly to the permit example.

1. **Capture the evidence:** Keep source URLs, field definitions and dated project notes. Link summaries back to their sources.
2. **Retrieve for the task:** Read the reporting-date definition, parcel join rules and known exclusions. Compare those notes with current source metadata.
3. **Check the output:** Run existing scripts, reconcile matched and unmatched records and inspect the actual report and map.
4. **Keep the lesson:** After review, update the note or procedure. Record the change and identify the result that a person approved.

**Concrete example:** A note can explain why the report uses one status-date field and how it handles a missing parcel association. The script implements the calculation. The report exposes the result. The reviewer checks the relationship among all three.

**Evidence limit:** This is an illustrative working pattern. It does not claim that every capture, retrieval, correction and approval currently happens automatically.

**Transition:** “Once those decisions are stable, the steps and checks can become a reusable procedure.”

### 13. Reusable GIS procedures — 15:45–16:30

**Speaker: Dara.**

**On screen:** A task-focused skill contract covering inputs, data rules, outputs, checks and stop conditions.

**Purpose:** Explain what makes a skill useful beyond a general prompt.

Use the monthly permit report as the example:

- **Inputs:** Approved permit snapshot, reporting month and parcel source.
- **Data rules:** Inspect date types and timezones. Preserve identifiers and unmatched rows.
- **Outputs:** Report, map-ready data, source record, exclusions and unresolved issues.
- **Checks:** Source and output counts reconcile. The map agrees with the table.
- **Stop conditions:** A required source is unavailable, its schema changes or a check fails.

**Suggested line:**

> “The procedure records what must be checked, including when the task should stop.”

Existing scripts still perform the calculations. The skill describes how to use and verify them. Load procedures relevant to the task rather than the entire catalog.

**Reference detail:** Source validation, data QA, analysis, mapping and testing are the useful categories. Keep package names on backup slide 20. Availability and license terms vary, so the configured packages are not a promise of default Hermes installation or freely redistributable handouts.

### 14. What a repeatable run records — 16:30–17:15

**Speaker: Dara.**

**On screen:** The task, inputs, execution and evidence.

**Purpose:** Make a report auditable and safe to rerun.

**Talk points:**

- **Task:** Record the question, geography, period, expected output and acceptance checks.
- **Inputs:** Record the source snapshot, retrieval time, timezone, code revision, dependencies and procedure revisions. Include the actual model identity when available.
- **Execution:** Use existing scripts with explicit parameters and stable date and join rules. Check that a rerun does not duplicate records or silently alter the method.
- **Evidence:** Preserve reconciled counts, known-answer tests, geometry and interaction checks, remaining limitations and the reviewed revision.

Model wording may vary. The source, calculation rules and acceptance conditions should remain explicit.

**Brief failure example:** A prior tree prototype passed its build and tests while polygons failed to render. Use the example to explain why the browser check must examine the data and geometry, not just whether the page loads.

**Reference task wording:** “Use the approved snapshot and existing script. Keep the date and join logic. Preserve unmatched records, test the map and table, and stop before publication.”

### 15. Agent time and cost — 17:15–18:00

**Speaker: Dara.**

**On screen:** Time to an accepted result, structured work, model inputs, limits and recurring jobs.

**Purpose:** Measure the whole task, including corrections.

Count elapsed time, retries, tool requests and model cost. Include the time a person spends making the result usable.

**Practices:**

- Use APIs and existing scripts for routine data operations.
- Filter and aggregate close to the data. Give the model relevant fields and compact summaries instead of entire feature collections.
- Load the procedures that apply to the current task.
- Set request, retry and output limits. Stop an unavailable or unsupported path rather than silently changing the method.
- Schedule ordinary scripts when recurring work needs no reasoning.

Additional agents can add coordination and rework. Parallel work is useful only when the tasks are independent and the benefit exceeds that overhead.

**Evidence limit:** No comparative cost or speed benchmark is presented. A fair comparison would hold sources, task, quality checks, permissions and environment constant across multiple runs.

### 16. Processing and map performance — 18:00–19:00

**Speaker: Dara.**

**On screen:** GIS processing and browser experience, with the reminder that a passing build can still leave the map empty.

**Purpose:** Separate processing efficiency from the experience of opening and using the map.

**GIS processing:** Retrieve required fields, rows and geography. Honor pagination and reconcile counts. Use suitable spatial indexes and vectorized operations before adding a more complex computing stack. Keep prepared aggregates and cached snapshots tied to their age and freshness rules.

**Browser experience:** Measure time until usable map data appears. Check geometry, filters and agreement with any table. Use clustering, generalized display geometry or vector tiles when warranted by the workload. Test cold and warm loads, mobile interaction and external-basemap failures.

**Useful measures:**

| Layer | Measures |
| --- | --- |
| Agent | Accepted-result time, model and tool cost, retries, human correction time |
| Processing | Input volume, runtime, peak memory, completeness, freshness |
| Application | Payload size, usable-map time, filter latency, errors |

Keep implementation claims specific to evidence from each application. The Service Terrain screenshot alone does not establish a renderer, data pipeline or performance result.

### 17. A first workflow — 19:00–20:00

**Speaker: Dara.**

**On screen:** A monthly report you already produce, with four steps: define it, reuse tools, check it and extend it.

**Purpose:** Give attendees a manageable next step.

Ask the audience to choose a recurring report with a known result and an approved source.

1. Define one question, a reporting period and a reviewable output.
2. Use an approved snapshot and an existing processing script.
3. Reconcile counts and compare the result with a known answer.
4. Extend access or introduce scheduling only after the bounded workflow passes review.

**Illustrative exercise:** Produce one month’s permit report, retain unmatched records and stop before publication. Keep a short note of the source, rules, checks and unresolved issues.

The first implementation does not need a multi-agent platform or a new application for every question.

**Suggested close:**

> “Choose a report you already understand. Keep the sources and rules with it, make the checks repeatable, and leave a result that another person can inspect and correct.”

Move to the questions slide at 20:00.

### 18. Questions — 20:00–25:00

**Speakers: Silas and Dara.**

**On screen:** Corrected speaker names, discussion topics and links to Hermes documentation, GISMap Online and the September permit report application.

**Silas leads:** Hermes, tool choice, model-provider configuration and GISMap Online.

**Dara leads:** Service Terrain, permits, Obsidian, procedures, repeatability and performance.

Likely questions include data handling, local deployment, maintenance cost, portability of skills, project-note organization and government use.

Use the hidden backup slides only when they answer a specific question. The Service Terrain URL remains to be supplied. Add a repository or handout QR code only after its destination has actually been published and tested.

## Hidden backup slides

### 19. Monthly permit report

**Use when:** An attendee asks what the actual task instructions or acceptance conditions look like.

**On screen:** A concise, illustrative task contract.

- **Task:** Produce the selected month’s report using the existing script.
- **Inputs:** Approved permit snapshot, parcel source and reporting month.
- **Rules:** Preserve date and join logic, identifiers and unmatched rows.
- **Outputs:** Report, map data, source record, exclusions and unresolved issues.
- **Checks:** Counts reconcile, map and table agree, reruns do not duplicate records.
- **Stop:** A required source is missing, the schema changes or a check fails.

Explain how the person reviewing the result decides whether to publish it. This is example wording, not a historical agent transcript. A completed output and approval should refer to the same reviewed revision.

### 20. Mercator skill references

**Use when:** An attendee asks which procedure categories or configured packages support the work.

| Purpose | Configured package | Checks to include |
| --- | --- | --- |
| Source checks | `arcgis-rest-service-validator` | Fields, query behavior and record completeness |
| Data QA | `geospatial-data-qa-pipeline` | CRS, geometry, duplicates and missing values |
| Python analysis | `geopython-analysis-engineering` | Reusable modules, fixtures and environments |
| Maps | `arcgis-maps-sdk-javascript`; `web-map-open-source` | Rendering, legends and map interaction |
| Testing | `gis-testing-performance-observability` | User journeys, data agreement and measured performance |

These names describe the configured GIS agent profile’s library. Some packages have commercial terms. Do not distribute their bodies without permission. Attendees can implement the same categories with appropriately licensed procedures.

Choose map procedures for the actual application stack. A skill’s license does not change the terms of an SDK, basemap or dataset.

### 21. Public-sector use

**Use when:** The discussion turns to organizational data, access or publication.

**Talking points:**

- Begin with public or explicitly approved sources. Keep restricted data and credentials out of prompts, screenshots and logs.
- Separate inspection from authoritative edits and release. Tie approval to the version actually reviewed.
- Use filesystem, database, network and sandbox controls. Profile separation alone is not security isolation.
- Treat service attributes, web pages and retrieved documents as source material, not authority to change the task.
- Review software, data, basemap and skill terms separately.
- Explain 311 reporting limitations and the difference between permit valuation, expenditure and completed work.
- Trace where data actually goes. A local host can still call a remote model or tool.

Keep the discussion tied to the source and action in question rather than claiming a general guarantee of privacy, safety or correctness.

### 22. Hermes setup and access

**Use when:** An attendee asks how the described setup runs across devices.

**On screen:** Phone and terminal access to a Mac Mini host, with rows for access, host and workspaces.

**Talking points:**

- Telegram on a phone or a terminal on a laptop provides a way to send tasks and inspect results.
- A Mac Mini runs Hermes and stores the project files.
- Tailscale provides private network access between devices in the described setup.
- Mercator keeps its configuration, memory and skills. Approved Obsidian notes supply longer project context.
- The host and the model provider have distinct roles. Local hosting does not establish local-only processing.

These setup details come from the supplied portfolio presentation. They are not an inspection of the current hardware or configuration. Avoid unsupported claims about model sizes, local memory capacity or guaranteed offline capability.

## Demo evidence and readiness

**Lineup:** GISMap Online with Silas, then Service Terrain and the September permit report with Dara. The second-brain explanation follows the permit report, rather than interrupting the three application examples.

| Item | Evidence included in the deck | Remaining rehearsal work |
| --- | --- | --- |
| Hermes | Supplied profile image and an explanation of tools, procedures, memory and scheduling | Verify any live terminal or messaging interaction before using it on stage |
| GISMap Online | Supplied welcome-screen screenshot and documented source/style/saved-view workflow | Rehearse the source, rendered geometry, legend and saved-view path in a browser with working WebGL |
| Service Terrain | Supplied image identifies the Sacramento public 311 columns visualization | Supply the exact URL and confirm the reporting period, legend, aggregation and one interaction |
| Permit report | Supplied September summary and map images, with totals and refresh date | Open the exact September state, verify a short map/table path and preserve the demonstrated snapshot |
| Obsidian | A source note and logo extracted from the supplied portfolio presentation | If using the live vault, choose an approved project-only path and avoid unrelated personal notes |
| Task and skill examples | Editable descriptions of procedures, inputs, checks and stop conditions | Prepare an appropriately licensed handout example if one will be distributed |

The supplied screenshots make the slides usable without live rendering. They do not establish that all application controls, schedules, data refreshes or model connections have been tested. No application deployment or new source-data pipeline run is part of this outline update.

## Five preparation tasks

1. **Freeze the demonstration path.** Use one prepared GISMap layer and style, one Service Terrain view and interaction, and one September permit summary/map/record path. Confirm the Service Terrain URL and definitions.
2. **Verify the displayed evidence.** Check geometry, units, counts, date coverage, exclusions, loading behavior and map/table agreement. Keep the September report’s September 27 cutoff and October 26 refresh context available.
3. **Prepare fallbacks.** Keep the current screenshots and short local recordings available. Avoid depending on conference Wi-Fi, live model inference, sign-ins, new installations or fresh builds.
4. **Prepare the takeaway.** Provide a short task contract, source/check record and licensed example procedure. Include the project-notebook pattern without publishing unrelated vault contents or commercial skill bodies.
5. **Rehearse the revised clock.** Silas ends GISMap at 10:00. Dara covers Service Terrain and permits by 14:15, the second-brain material by 15:45, and closes at 20:00. Leave the five-minute questions segment intact.

If the talk runs long, shorten navigation and feature touring. Use screenshots for the same evidence rather than dropping the checks and limitations that explain the workflow.

## Source and image notes

- The original detailed outline provides the session structure, demo framing, skill categories and practical checks.
- The current reordered PowerPoint supplies the exact 22-slide sequence and on-screen content.
- `From_LLMs_to_GIS_Hermes_Portfolio.pptx` supplies supporting Hermes, memory, Obsidian and setup material. Relevant original file positions include slides 19–22 and 25–28. File positions are used because its visible numbering is inconsistent with its 36-slide count.
- Hermes profile artwork: supplied `IMG_5742.jpeg`. Retain the supplied image without labeling it as an independently verified official logo.
- GISMap Online screenshot: supplied `IMG_5741.jpeg`.
- September permit summary: supplied `IMG_5740.jpeg`.
- Permit map and legend: supplied `IMG_5739.jpeg`. Retain the Leaflet and OpenStreetMap contributor attribution.
- Service Terrain screenshot: supplied `IMG_5738.jpeg`.
- Obsidian source-note screenshot and logo: extracted from the supplied portfolio deck’s Obsidian slide. The source note is evidence of the notebook structure, not independent verification of the article it summarizes.
- Cover photograph: Stephen Leonardi, “Aerial View of Sacramento’s Tower Bridge at Sunset,” Pexels. https://www.pexels.com/photo/aerial-view-of-sacramento-s-tower-bridge-at-sunset-34276098/ . License: https://www.pexels.com/license/ .

## Research references

- Accepted session and current program listing: https://talks.osgeo.org/foss4g-na-2026/talk/GXG78A/
- Hermes documentation: https://hermes-agent.nousresearch.com/docs/
- Hermes memory: https://hermes-agent.nousresearch.com/docs/user-guide/features/memory/
- Hermes skills: https://hermes-agent.nousresearch.com/docs/user-guide/features/skills/
- Hermes profiles: https://hermes-agent.nousresearch.com/docs/user-guide/profiles/
- Hermes scheduled tasks: https://hermes-agent.nousresearch.com/docs/user-guide/features/cron
- Obsidian data storage: https://obsidian.md/help/data-storage
- Obsidian backlinks: https://obsidian.md/help/plugins/backlinks
- Claude Code overview: https://code.claude.com/docs/en/overview
- Claude Code skills: https://code.claude.com/docs/en/skills
- Codex CLI: https://developers.openai.com/codex/cli
- Codex source and license: https://github.com/openai/codex
- GISMap Online: https://www.gismap.online/
- GISMap agent guide: https://www.gismap.online/guides/ai-agents/
- GISMap examples: https://www.gismap.online/examples/
- Permit report application: https://sacbuildingpermits.vercel.app
- Service Terrain: identified by the supplied screenshot. Exact application URL pending.

Session listing checked October 28, 2026. The outline uses the supplied September permit snapshot and the reviewed deck. Comparative statements concern workflow fit, not measured product superiority.
