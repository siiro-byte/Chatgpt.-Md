# Prompt Library Test Report

**Test date:** 2026-11-05  
**Repository:** https://github.com/siiro-byte/Chatgpt.-Md  
**Scope:** 29 rewritten prompts across seven specialist categories  
**Current result:** FIRST-PASS COMPLETE — 29 of 29 scenario tests recorded as passed

## Test method and limitations

Each recorded test uses a realistic, controlled scenario and a desk-based simulation of how the prompt's instructions handle the task, missing information and factual safeguards. These are first-pass scenario simulations, not instrumented executions of every prompt in a separate model session, independent user studies or cross-model benchmarks. No external systems, live travel-status sources, production accounts or customer datasets were accessed. A PASS means the prompt's instructions handled the scenario correctly at this level; it does not establish universal reliability.

## Recorded scenario tests

| Prompt | Test scenario | Observed behaviour | Result |
|---|---|---|---|
| Marketing — Positioning & Messaging | Small Nairobi commuter service; three competitors; limited interviews | Separates audience need, alternatives, benefits and proof; labels unverified differentiation as a hypothesis; proposes validation | PASS |
| Marketing — Audience Intelligence | Eight convenience-sampled interviews with mixed preferences | Flags sample bias, distinguishes behaviour from stated preference, avoids invented quotations and identifies evidence gaps | PASS |
| Marketing — Campaign Planner | KES 100,000, 30-day launch with no historical conversion data | Produces objective, funnel, channel roles, budget assumptions, tracking and tests without inventing forecasts | PASS |
| Marketing — Growth Experiment Designer | Suspected checkout abandonment with incomplete tracking | Requires instrumentation checks, a falsifiable hypothesis, guardrails and a decision rule before interpreting results | PASS |
| Travel — Travel Alert Verification | Unsourced post claims a named land crossing is closed today | Requires responsible authority, separates event/update dates and directs Unverified/Hold when evidence is absent | PASS |
| Travel — Destination Intelligence Brief | Destination request omits passport nationality and travel dates | Requests material missing details; separates entry rules from advisories; avoids generic filler | PASS |
| Travel — Border & Entry Rule Monitor | Social post claims a visa rule will start next month but supplies no legal notice | Distinguishes announcement/proposal from effective rule; requires authority, scope and dates | PASS |
| Travel — Aviation & Transport Update | One flight delayed; no evidence of wider disruption | Limits scope to the service, checks operator/airport evidence and avoids generalising | PASS |
| Travel — Traveller-First Social Post | Confirmed terminal entrance closure for renovation; other entrance remains open | Produces a scoped, dated, platform-adapted message; identifies affected passengers and action; avoids implying wider airport closure | PASS |
| Business — Business Model Review | Small made-to-order furniture studio with missing acquisition and repeat-purchase data | Connects customer, delivery, revenue and cost logic; flags missing metrics; avoids invented financials and tests scale against capacity | PASS |
| Business — Market Validation Plan | Founder considers an airport-transfer app based only on positive comments from friends | Prioritises risky assumptions and low-cost behavioural tests; distinguishes compliments from evidence of demand | PASS |

## Additional scenario tests completed (2026-11-05)

The following 18 prompts received a documented desk-based scenario simulation. Each check assessed expected output fit, treatment of missing information, factual restraint and task-specific safeguards.

| Category | Prompt | Scenario focus | Observed result |
|---|---|---|---|
| Business & Strategy | Strategic Options Memo | Small furniture studio choosing showroom, online expansion or status quo with incomplete evidence | PASS — distinct options and assumptions; no invented forecasts |
| Business & Strategy | Unit Economics Review | Online seller with price, variable costs and fixed costs but no acquisition/retention data | PASS — contribution and conditional break-even calculated; CAC/LTV withheld |
| Writing & Communication | Clear Brief Writer | Catalogue launch notes missing owner, deadline and acceptance criteria | PASS — gaps retained; proposed criteria labelled |
| Writing & Communication | Editorial Rewrite & Polish | Announcement with errors and ambiguous “soon” timing | PASS — clarity improved; ambiguity preserved and flagged |
| Writing & Communication | Professional Email Drafter | Supplier follow-up with missing recipient, sender and delivery date | PASS — placeholders used; no invented contact details |
| Writing & Communication | Stakeholder Update & Memo | Project delay and unresolved dependency with no owner or next-update date | PASS — facts separated from unknowns; no invented ownership/date |
| Image, Video & Audio | Image Generation Brief | Square brand graphic with supplied exact logo and required copy | PASS — hierarchy and exclusions specified; text-rendering risk flagged |
| Image, Video & Audio | Short-Form Video Storyboard | 30-second advisory about one affected airport entrance | PASS — scope retained; visuals and claims aligned |
| Image, Video & Audio | Voiceover Script & Audio Direction | 45-second narration with date, place name and traveller qualification | PASS — word budget and caveat retained; pronunciation flagged |
| Image, Video & Audio | Creative Asset Quality Review | Review request with no actual asset supplied | PASS — inability to inspect is stated; unseen details not invented |
| Coding & Technology | Technical Requirements Clarifier | Order-tracking system request with missing roles, integrations and data constraints | PASS — requirements and open questions separated; no premature stack choice |
| Coding & Technology | Code Review & Risk Audit | Endpoint snippet with no visible authorisation check or tests | PASS — risk framed for validation; no unsupported exploit claim |
| Coding & Technology | Systematic Debugging | Intermittent API 500 after deployment with incomplete logs | PASS — ranked hypotheses and safe tests; root cause not asserted |
| Coding & Technology | Practical Solution Architecture | Low-volume booking service with personal data, small team and limited budget | PASS — proportionate design and privacy/failure controls considered |
| Productivity & Learning | Practical Learning Roadmap | Spreadsheet learner with unknown baseline, time and budget | PASS — diagnostic and assumptions surfaced; schedule not fabricated |
| Productivity & Learning | Meeting Notes to Action Plan | Supplier-change proposal and contract-check task with no owner/date | PASS — proposal not treated as decision; owner/date left unknown |
| Productivity & Learning | Decision Log & Review | Vendor choice discussed without approver, date or review trigger | PASS — approval and review details not inferred |
| Productivity & Learning | Workflow Simplifier | Repeated spreadsheet copying with no time/error baseline | PASS — process mapped before automation; benefits not quantified |

No blocking defect was identified in these first-pass scenarios. This is not evidence of universal reliability; tests were applied in this review and were not independently benchmarked across models. Each result is limited to its stated scenario.

## Defects and follow-up

No blocking defect was identified in the 29 recorded first-pass scenario tests. The review still does not establish cross-model consistency, production reliability or user acceptance. Any later failure should be logged, corrected and retested before approval.

## Status policy

- **Draft:** not yet scenario-tested, or failed and awaiting correction.
- **Tested:** at least one realistic scenario has been run and its outcome and limitations recorded.
- **Approved:** separately reviewed after testing; no prompt is approved by this report.

**Current scenario-test coverage:** 29 of 29 prompts have a first-pass scenario result recorded in this report. All 29 prompt files now have individual testing notes and are marked Tested. No prompt is Approved.
