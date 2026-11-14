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
