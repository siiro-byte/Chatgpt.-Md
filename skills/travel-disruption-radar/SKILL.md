# Travel Disruption Radar — Skill
Version: 1.0 (2026-11-14)
Purpose: Catch high-impact emerging travel disruptions missed by routine editorial research. This is a detection and verification skill, not automatic publication.

## Trigger
Run before every Travel Alerts.ke daily briefing and on each dedicated monitoring cycle. Scan the preceding 24 hours plus developing incidents and meaningful status changes. Use EAT for editorial timestamps.

## Mandatory discovery sweep
1. Search explicitly for: airspace closed/reopened, ground stop, airport shutdown, FAA national ground delay, ATC outage, mass flight cancellations, NOTAM restrictions, diversions, airline suspension, border closure, evacuation, major transport strike, severe-weather travel shutdown, travel health entry restrictions.
2. Check all five African regions independently, then Middle East, Europe, North America, Asia-Pacific and major intercontinental routes. Do not let African coverage suppress global critical events.
3. Cross-check official aviation regulators/ANSPs, airport operators, airline notices, official NOTAM/AIP sources, transport/immigration authorities, and credible breaking-news desks (Reuters/AP and relevant local media). Social/Reddit/trends are discovery leads, never confirmation.
4. Search both current breaking stories and official incident status; compare announcement time, actual incident time and effective time. Watch reopenings and cancellations of restrictions.
5. Check recent research and published content; only escalate previously covered stories if there is a material verified change.

## Priority
P0: verified national/regional airspace closure, nationwide ground stop, multiple major airports shut, large-scale passenger safety emergency or mass disruption across international routes.
P1: major airport closure, significant airline network cancellations, new border ban or significant traveller safety emergency.
P2: localized but consequential disruptions or important emerging leads.
Trends and social volume affect discovery order, NOT evidence status or publication priority. Do not invent thresholds, passenger totals, affected airports or closures.

## Verification and escalation
For each lead capture: headline, country/airport/route, event and publication timestamps (timezone), status (active/resolved/upcoming), precise affected travellers, operational impact, traveller action, official URL, independent corroboration URL, confidence (CONFIRMED/PARTLY CONFIRMED/CONFLICTING/UNVERIFIED/STALE), prior coverage and what materially changed.
A technical NOTAM alone does not prove a passenger disruption. Distinguish airspace closure, airport closure, ground stop, ground delay and individual cancellations. If verification fails, retain as monitoring-only.
Escalate verified P0/P1 to the editor at the next monitoring run; do not wait for the next daily briefing. Do not post publicly without explicit authorization. If no new verified impact, report no material change, not a manufactured alert.

## Output
One concise alert per development: editorial headline; what changed; exact location; event and update dates; status; traveller consequence and practical action; confidence; links; new versus previous coverage. Flag P0 prominently.
Before finalizing, do a separate final scan of worldwide aviation disruption headlines to catch stories that regional searches missed.

## Integration
Use with CHATGPT.md, TRAVELALERTS_RESEARCH.md and the maintained SOURCES.md registry. This skill supplements, never overrides, existing freshness, verification, traveller-impact, duplicate-control and publication rules. GitHub storage alone does not activate scheduled execution; use a separately configured monitor.

## Operational assurance and missed-alert prevention (v1.1)
- Mandatory sweep checklist for every run: East, West, North, Central and Southern Africa; Middle East; Europe; North America; Asia-Pacific; worldwide aviation disruption search. Record searched/not searched for each. A region with no confirmed alerts is NOT the same as a region not searched.
- Search for both headline vocabulary and operator terminology: FAA ground stop, ground delay program, ATC system outage, flight cancellations, airspace restriction, airport closure, airline operational advisory, border suspension, reopening and restoration.
- Prioritise new material changes in the last hour, but include a rolling 24-hour lookback to catch late reporting and missed checks. Track first detection, latest update and whether the incident was already notified.
- Source outage, inaccessible official notice, missing result, or search-tool failure must be recorded as COVERAGE GAP, never interpreted as no disruption. If a critical region/source cannot be checked, raise an operational failure notice identifying the missing coverage, without claiming an incident.
- On P0, use the earliest available corroborated official operational notice plus reputable reporting where available. If confirmation is incomplete, classify as monitoring-only with an explicit uncertainty label; never present it as confirmed. Avoid delaying detection solely to collect optional details.
- Notify only for newly verified P0/P1 events or material change (closure, reopening, new routes affected, materially changed cancellation impact, new official traveller action). Do not repeat unchanged alerts. Distinguish event resolution from residual passenger disruption.
- Each notification must include: priority, event type (ground stop vs airspace closure vs airport closure), event time and update time with timezone, precise affected area, current status, traveller consequence, supported action, official link, corroborating link where available, and what changed.
- Never auto-publish to TikTok, Facebook, Telegram or X. Editor approval remains required.
- Quality audit: record detection timestamp, verification timestamp, notified/not notified, reason, and coverage gaps when a durable log is available. Do not claim persistence when no logging integration exists.
- Acceptance tests: (A) simulated nationwide ground stop classified P0, without mislabelling it an airspace closure; (B) reopening triggers one material update; (C) stale article with no new development is rejected; (D) official source inaccessible produces coverage-gap notice; (E) repeated unchanged story produces no duplicate. These are rule tests, not evidence of historical notification.
- A GitHub skill is guidance, not a standalone live feed. The hourly automation is the execution mechanism; detection can lag an incident by up to the check interval plus source and execution delays. Review actual run records and delivery before declaring end-to-end success.


## HARD STOP: STORY-LEVEL DEDUPLICATION (2026-11-16)

This gate is mandatory before any daily briefing, radar notification, shortlist, draft, or publication. A new article, new URL, new publication timestamp, social trend, or another outlet repeating a story does NOT make the underlying event new.

1. **Load history first:** retrieve the accessible Content & Source Log, previous 72 hours of research/briefings, published platform posts, and prior radar notifications; check the last 30 days for the same incident or standing advisory. Record which sources were actually accessible. If history is unavailable, mark HISTORY_UNVERIFIED and do not assert an item is new; seek editor review before presenting it as a fresh alert.
2. **Normalize incident identity:** create a stable story key from event type + country + specific airport/border/location/route + responsible authority + original event/effective date. Match semantically, not by headline or URL; aliases, translations, syndication, and different platform posts count as the same incident.
3. **Compare factual delta:** for every matched story, record previous verified state, current verified state, exact newly changed fact, source and timestamp. Only a verified material change qualifies: new closure/reopening, new binding restriction or effective date, newly affected route/population, significant verified escalation/de-escalation, or new actionable official instruction. Mere restatement, unchanged warning, rolling delay statistics, speculation, updated article timestamps, and residual effects already covered are NOT material changes unless the new impact is demonstrably significant and actionable.
4. **Decision:** NEW_VERIFIED (no prior match, original event genuinely new); MATERIAL_UPDATE_VERIFIED (matched story, substantive evidenced delta); DUPLICATE_REJECTED; STALE_REJECTED; MONITOR_ONLY; or HISTORY_UNVERIFIED. Only the first two enter the fresh editorial shortlist. Mark material updates explicitly as 'UPDATE' and explain the delta; never present them as a new incident.
5. **Quota is never a target:** report fewer stories, including zero, rather than substitute repeated or unverified items to fill regional counts. If a previously reported story has no new verified change, omit it from the new-alert list. Keep ongoing context in a separate labelled section only when specifically useful, never as a fresh alert.
6. **Before delivery, second-pass audit:** compare all candidate story keys against each other, against the historical log, and against yesterday's briefing. Reject cross-region duplicate coverage of the same incident unless there is a distinct newly verified traveller consequence. Record per-item story key, last-covered date/platform, delta, evidence, decision and reason.
7. **After delivery:** record researched, rejected, shortlisted, approved and published status separately with event time, source time, first-seen time and publication time in EAT. A research mention is not proof of publication, but it is prior coverage for briefing deduplication. If a durable log cannot be written, explicitly report LOG_WRITE_UNAVAILABLE and do not claim cross-run deduplication is guaranteed.

**Acceptance tests:** yesterday's Bahrain warning repeated today => DUPLICATE_REJECTED; a newly published article about the same US ground stop => DUPLICATE_REJECTED; officially verified airport reopening after yesterday's closure => MATERIAL_UPDATE_VERIFIED; an inaccessible content log => HISTORY_UNVERIFIED; request for nine stories with only four eligible => return four, not nine.


## X editorial handoff — verified publishing route (2026-11-16)

This radar **never publishes automatically**. Produce up to five distinct verified X drafts only when new, material and publication-worthy incidents qualify; require explicit editor approval for each publication. Before drafting or publishing, check the accessible prior-coverage log and recent sent/scheduled posts to avoid duplicates.

**When the editor explicitly approves an X post:** Follow the primary workflow in repository `CHATGPT.md`, section **TRAVEL ALERTS.KE — X PUBLISHING ROUTE**: ChatGPT → Composio → Buffer → @travelalertss. Discover the current Composio Buffer tools, verify active Buffer connection and exact unlocked X channel, inspect recent sent posts, then call `BUFFER_PUBLISH_POSTS` with `delivery_mode: "share_now"` for the approved text only. Verify `status: "sent"` before reporting success; record the returned post ID and timestamp. Do not mistake a missing direct X connection for a missing Buffer connection. Do not fall back to paid providers or spend without explicit authorization. Never auto-publish, auto-schedule or pad the X draft quota.


## EXPANDED BREAKING-NEWS DISCOVERY (2026-11-16)

At each scheduled hourly run, when accessible, scan public reporting from Reuters, AP, AFP, BBC, Al Jazeera, Africanews and AllAfrica plus relevant local African publishers; consult France 24/RFI, DW, CNN, The EastAfrican and aviation specialists FlightGlobal, AeroTime and Simple Flying as appropriate. Samsung News, Google News and Microsoft Start/MSN are OPTIONAL discovery aggregators, not guaranteed machine-accessible integrations. Do not block the run on an unavailable feed; record SOURCE_UNAVAILABLE and last successful check. Never claim a channel was monitored without evidence of a successful check.

Normalize leads to original publisher and URL, publication/update EAT, event EAT, location, travel impact and canonical incident key. Verify urgent aviation/airport/airspace, border/visa, safety/health and passenger transport claims against relevant authorities; cross-check independent reporting where possible. Syndicated copies do not count as independent corroboration. Prioritize P0/P1 real-world disruptions; no speculative forecast or fabricated closure. Compare prior research, yesterday's briefing and published content by incident and material delta. Record checked/not checked per channel, failures, candidate count, verified count and publication status. Preserve all existing escalation and editor-approval gates. No paid calls without explicit approval; no auto-publishing.


## X-only post optimization — isolated from radar detection (2026-11-16)

**Radar first, X check last.** Complete the independent last-hour/24-hour regional searches, official corroboration, P0/P1 classification, material-change and historical deduplication checks, and notification decision **without Grok or X algorithm analysis as a prerequisite**. No mandatory Grok Search, Grok API calls or algorithm checks during detection. Never delay urgent P0/P1 escalation.

Only if one or more **new, verified, publish-worthy X drafts** qualify (maximum five, never padded), run the **lightweight qualitative X-only algorithm/editorial checklist** in `CHATGPT.md` on those drafts: specific headline/location, factual consequence, practical action, credible source link, clarity and restrained tags. Grok is not X's recommendation algorithm; use freely accessible official X algorithm documentation only if helpful and available, without slowing the run. Skip this step when there are no X drafts. No reach guarantees, paid calls, new API integrations or changes to other channels. Preserve editor approval and Composio → Buffer publishing rules; never auto-publish.
