# Travel Disruption Radar — Skill
Version: 1.0 (2026-11-14)
Purpose: Catch high-impact emerging travel disruptions missed by routine editorial research. This is a detection and verification skill, not automatic publication.

## Trigger
Run before every Travel Alerts.ke daily briefing and when explicitly requested. The separate hourly automation is disabled. Scan the preceding 24 hours plus developing incidents and meaningful status changes. Use EAT for editorial timestamps.

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
Flag verified P0/P1 findings first in the current run and notify the editor when the workflow supports it. Do not post publicly without explicit authorization. If no new verified impact, report no material change, not a manufactured alert.

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
- A GitHub skill is guidance, not a standalone live feed. The current setup runs this checklist as part of the daily briefing. Report actual source coverage and delivery evidence. Review actual run records and delivery before declaring end-to-end success.


## Incident deduplication and publication

For a standalone sweep, provide up to five distinct verified X drafts when requested. The daily briefing has its own item count.

Use the [shared incident deduplication procedure](https://github.com/siiro-byte/Chatgpt.-Md/blob/main/TRAVELALERTS_RESEARCH.md#hard-stop-story-level-deduplication-2026-11-16) before escalating or drafting. For an approved publication request, follow the [publishing runbook](https://github.com/siiro-byte/Chatgpt.-Md/blob/main/TRAVELALERTS_PUBLISHING.md).

## EXPANDED BREAKING-NEWS DISCOVERY (2026-11-16)

For each daily or on-demand sweep, when accessible, scan public reporting from Reuters, AP, AFP, BBC, Al Jazeera, Africanews and AllAfrica plus relevant local African publishers; consult France 24/RFI, DW, CNN, The EastAfrican and aviation specialists FlightGlobal, AeroTime and Simple Flying as appropriate. Accessible Google News and Microsoft Start/MSN are optional discovery leads. Samsung News is optional for manual discovery only until 21 December 2026 at 03:00 EAT. Omit it from scheduled discovery and retire it after that date. Do not block the run on an unavailable feed; record SOURCE_UNAVAILABLE and last successful check. Never claim a channel was monitored without evidence of a successful check.

Normalize leads to original publisher and URL, publication/update EAT, event EAT, location, travel impact and canonical incident key. Verify urgent aviation/airport/airspace, border/visa, safety/health and passenger transport claims against relevant authorities; cross-check independent reporting where possible. Syndicated copies do not count as independent corroboration. Prioritize P0/P1 real-world disruptions; no speculative forecast or fabricated closure. Compare prior research, yesterday's briefing and published content by incident and material delta. Record checked/not checked per channel, failures, candidate count, verified count and publication status. Preserve all existing escalation and editor-approval gates. No paid calls without explicit approval; no auto-publishing.


## X-only post optimization

The optional X editorial check applies only to qualified @travelalertss drafts after verification and deduplication. It must never delay urgent alerts. Do not use Grok.

### Research-source retirement — 16 Nov 2026
- Grok/xAI via Composio is **removed from the research and radar workflow**. Do not discover, call, test, or require Grok for research. This does **not** remove the separately approved Composio → Buffer X publishing route.
- End-to-end gate: retrieve instructions, discover candidates, corroborate with primary authority, compare ledger and historical posts, assign P0/P1 only on verified material impact, prepare approval-only drafts, record each check and its limitations. No automatic publication. Use existing access at KES 0 by default. Obtain specific approval before any new paid usage.
