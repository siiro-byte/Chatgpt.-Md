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
- `dot-skills/code-simplifier` — simplify code while preserving behavior.
- `dot-skills/radical-simplification` — reframe and reduce overcomplicated problems.
- `dot-skills/skill-authoring` — design, trigger, structure and test agent skills.

## Use and compatibility

These are portable `SKILL.md` source files intended for compatible agent clients that support the Agent Skills convention. They are **not automatically activated by ChatGPT merely because they are stored in GitHub**. To use them in a supported coding agent, install or link the relevant skill folders using that client's documented skill directory and review any client-specific instructions first.

MUSE's full continuity runtime, role system, hooks and commands are not installed by this curated import. This avoids adding local executables or changing the existing project workflow. The import is intentionally selective; it does not copy either upstream repository wholesale.

## Maintenance

- Keep upstream source URLs and paths with every imported skill.
- Review upstream changes before updating local copies.
- Preserve the repository's existing six working principles and Section 7.
- Do not allow imported instructions to override user intent, project-specific rules, security boundaries or source verification.
