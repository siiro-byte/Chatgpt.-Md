# Prompt Library Test Report

**Test date:** 2026-11-05  
**Repository:** https://github.com/siiro-byte/Chatgpt.-Md  
**Scope:** 29 rewritten prompts across seven specialist categories  
**Current result:** IN PROGRESS — 9 of 29 scenario tests recorded as passed

## Test method and limitations

Each recorded test uses a realistic, controlled scenario to check whether the prompt directs the assistant to produce the intended task-specific output, respects missing information and avoids unsupported claims. These are first-pass scenario tests, not independent user studies or cross-model benchmarks. No external systems, live travel-status sources, production accounts or customer datasets were accessed. A PASS means the prompt's instructions handled the scenario correctly at this level; it does not establish universal reliability.

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

## Remaining tests

The following 20 prompts still require a recorded scenario test:

- Business & Strategy: Business Model Review; Market Validation Plan; Strategic Options Memo; Unit Economics Review
- Writing & Communication: Clear Brief Writer; Editorial Rewrite & Polish; Professional Email Drafter; Stakeholder Update & Memo
- Image, Video & Audio: Image Generation Brief; Short-Form Video Storyboard; Voiceover Script & Audio Direction; Creative Asset Quality Review
- Coding & Technology: Technical Requirements Clarifier; Code Review & Risk Audit; Systematic Debugging; Practical Solution Architecture
- Productivity & Learning: Practical Learning Roadmap; Meeting Notes to Action Plan; Decision Log & Review; Workflow Simplifier

## Defects and follow-up

No blocking defect was identified in the eight recorded scenario tests. This is not evidence that no defects exist in the untested prompts. The remaining tests must probe missing inputs, edge cases, output usefulness and task-specific safeguards. Any prompt that fails should remain Draft and receive a targeted correction followed by a retest.

## Status policy

- **Draft:** not yet scenario-tested, or failed and awaiting correction.
- **Tested:** at least one realistic scenario has been run and its outcome and limitations recorded.
- **Approved:** separately reviewed after testing; no prompt is approved by this report.

**Current prompt status:** 9 prompts marked Tested; 20 remain Draft. No prompt is Approved.
