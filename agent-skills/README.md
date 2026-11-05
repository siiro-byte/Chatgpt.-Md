# External Agent Skills

This directory contains a small, curated import of reusable skills from two MIT-licensed open-source projects. Original skill instructions are retained in their own folders; source attribution and upstream paths are recorded here.

## Sources

- **MUSE** — https://github.com/myths-labs/muse (MIT). Skills are adapted from its `skills/core` and `skills/toolkit` directories.
- **Dot Skills** — https://github.com/pproenca/dot-skills (MIT). Skills are adapted from its `skills/.curated` directory.

## Imported skills

### MUSE
- `muse/context-health-check` — distinguish observed context data from unknowns; preserve useful work at handoff points.
- `muse/verification-before-completion` — require fresh evidence before claiming completion.
- `muse/systematic-debugging` — structured root-cause investigation.
- `muse/security-review` — security-focused review prompts and checks.

### Dot Skills
- `dot-skills/think` — structured reasoning and problem framing.
- `dot-skills/skill-authoring` — design, trigger, structure and test agent skills (includes its referenced template).

## Use and compatibility

These are portable `SKILL.md` source files intended for compatible agent clients that support the Agent Skills convention. They are **not automatically activated by ChatGPT merely because they are stored in GitHub**. To use them in a supported coding agent, install or link the relevant skill folders using that client's documented skill directory and review any client-specific instructions first.

MUSE's full continuity runtime, role system, hooks and commands are not installed by this curated import. This avoids adding local executables or changing the existing project workflow. The import is intentionally selective; it does not copy either upstream repository wholesale.

## Maintenance

- Keep upstream source URLs and paths with every imported skill.
- Review upstream changes before updating local copies.
- Preserve the repository's existing six working principles and Section 7.
- Do not allow imported instructions to override user intent, project-specific rules, security boundaries or source verification.


## Import scope and known exclusions

Only skills whose required local references were included are listed as imported. Two initially reviewed Dot Skills (`code-simplifier` and `radical-simplification`) were not retained because their SKILL.md files depend on large sets of additional reference documents that have not been imported. They remain available in the upstream repository and can be added later as complete bundles.


### Addy Osmani Agent Skills

Source: [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) — MIT License (copy included at `addy-osmani/LICENSE`).

- `addy-osmani/context-engineering` — manage context deliberately and keep task-relevant information available.
- `addy-osmani/planning-and-task-breakdown` — turn goals into sequenced, verifiable tasks.
- `addy-osmani/source-driven-development` — ground implementation in the actual codebase and authoritative sources.
- `addy-osmani/doubt-driven-development` — challenge assumptions and test uncertain claims.
- `addy-osmani/interview-me` — clarify requirements through focused questions.
- `addy-osmani/shipping-and-launch` — prepare changes for release and verify readiness.
- `addy-osmani/code-review-and-quality` — review changes for correctness and maintainability.
- `addy-osmani/test-driven-development` — use tests to define and verify expected behavior.

These are instruction-only SKILL.md files; no scripts or external dependencies were imported. They were reviewed for obvious local file references before import. This is a static review, not a guarantee of safety or correctness.


### Superpowers

Source: [obra/superpowers](https://github.com/obra/superpowers) — MIT License (copy included at `superpowers/LICENSE`).

- `superpowers/receiving-code-review` — evaluate review feedback against the actual codebase before implementing it; clarify ambiguity, test fixes individually, and push back with evidence when necessary.

Only this self-contained skill was imported from Superpowers in this pass. Other candidates were excluded where they duplicated existing skills, depended on unimported supporting files, or imposed workflow gates that conflict with the repository's working principles. The source skill was reviewed statically; this is not a guarantee of safety or correctness.
