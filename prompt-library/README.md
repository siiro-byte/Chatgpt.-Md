# Master AI Prompt Library

A curated, source-aware collection of reusable prompts for research, analysis, communication, strategy and practical work.

This library uses the **Fabric** open-source prompt framework as a foundation and selectively incorporates useful material and techniques from Fabric, prompts.chat and the DAIR.AI Prompt Engineering Guide. It is curated rather than a wholesale mirror: prompts should be relevant, attributable, reviewed and tested before approval.

For Google Gemini usage, see the [Gemini Quickstart](GEMINI-QUICKSTART.md). For repository-level Gemini CLI context, see the root [GEMINI.md](../GEMINI.md).

## Working principles
- Quality over quantity; avoid duplicate or low-value prompts.
- Preserve source attribution and applicable licences.
- Test prompts on realistic tasks before marking them approved.
- Require evidence and source transparency for factual research.
- Protect private, confidential and personal information.
- Keep prompts portable across compatible AI assistants; note tool-specific requirements.

## Categories
| Category | Purpose | Status |
|---|---|---|
| [Research & Intelligence](research-intelligence/README.md) | Research, verification, monitoring, risk, trends and analysis | In progress |
| [Marketing & Growth](marketing-growth/README.md) | Positioning, audience insight, campaigns and measurable growth | In progress |
| [Travel Editorial](travel-editorial/README.md) | Travel alerts, destination intelligence, border and transport developments | In progress |
| [Business & Strategy](business-strategy/README.md) | Business models, validation, strategic choices and commercial logic | In progress |
| [Writing & Communication](writing-communication/README.md) | Clear writing, editing and stakeholder communication | In progress |
| [Image, Video & Audio](image-video-audio/README.md) | Creative briefs, storyboards, scripts and quality review | In progress |
| [Coding & Technology](coding-technology/README.md) | Requirements, code review, debugging and architecture | In progress |
| [Productivity & Learning](productivity-learning/README.md) | Learning plans, decisions, meetings and workflows | In progress |

## Prompt lifecycle
- **Draft** — created, not yet tested, or awaiting a retest after a failure.
- **Tested** — at least one realistic scenario has been run and its result and limitations recorded.
- **Approved** — separately reviewed after testing.
- **Retired** — no longer recommended.

Do not label a prompt Tested or Approved without a recorded test. Consult [TEST-REPORT.md](TEST-REPORT.md) for the current recorded coverage.

## Adding or updating a prompt
Use [PROMPT-TEMPLATE.md](PROMPT-TEMPLATE.md). Each prompt should include purpose, use case, required inputs, complete instructions, expected output, quality checks, source and attribution, testing notes and status.

See [SOURCES.md](SOURCES.md) for source projects and curation rules.

**Quality standard:** A prompt is useful when it produces a repeatable, relevant result while making uncertainty, limitations and evidence visible. Prefer small, testable improvements over large unverified collections.
