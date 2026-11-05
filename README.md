# ChatGPT Working Principles & Portable AI Toolkit

A curated, model-agnostic repository of working principles, reusable prompts and agent skills for research, writing, strategy, travel intelligence, software development and practical work.

The repository is designed to be readable by ChatGPT, Google Gemini and other compatible AI assistants. It contains instruction and reference files, not a hosted application.

## Repository architecture

```text
.
├── README.md                         # Repository overview and setup guide
├── CHATGPT.md                        # ChatGPT working principles and project guidance
├── GEMINI.md                         # Gemini CLI context and operating guidance
├── agent-skills/
│   ├── README.md                     # Skill sources, scope and compatibility
│   ├── muse/                          # Context, verification, debugging and security
│   ├── dot-skills/                    # Thinking and skill-authoring references
│   ├── addy-osmani/                   # Engineering and delivery practices
│   └── superpowers/                   # Code-review feedback evaluation
└── prompt-library/
    ├── README.md                     # Master prompt catalogue and lifecycle
    ├── PROMPT-TEMPLATE.md             # Standard prompt authoring template
    ├── SOURCES.md                    # Attribution, licences and curation rules
    ├── TEST-REPORT.md                # Scenario-test status and results
    ├── research-intelligence/        # Research, verification, risk and analysis
    ├── marketing-growth/             # Audience, positioning and growth
    ├── travel-editorial/             # Travel alerts and destination intelligence
    ├── business-strategy/            # Business models and strategic decisions
    ├── writing-communication/        # Briefs, editing and stakeholder writing
    ├── image-video-audio/            # Creative briefs and production scripts
    ├── coding-technology/            # Requirements, architecture and debugging
    ├── productivity-learning/        # Learning, decisions and workflows
    └── GEMINI-QUICKSTART.md           # Using this library with Gemini
```

The prompt library is organised by task category. Each category has an index and individual prompt files. Agent skills are kept separate from prompts because they use the Agent Skills `SKILL.md` convention and may require a compatible skill loader.

## Getting started

### Option 1: Use with Google Gemini

1. Open the repository on GitHub and review `GEMINI.md`.
2. For Gemini CLI, clone the repository and keep `GEMINI.md` at the repository root so the CLI can use it as project context.
3. For Gemini web or a Gem, provide the relevant instruction and prompt files through the product's available file-upload or instruction features. Do not assume a GitHub URL is automatically loaded as context.
4. Choose a prompt from `prompt-library/README.md`, provide its required inputs and ask Gemini to follow the complete prompt.
5. For a multi-step task, provide only the relevant specialist skill files from `agent-skills/` when the client supports them.
6. Review outputs and verify factual claims, sources, calculations and any proposed actions before relying on them.

See [Gemini Quickstart](prompt-library/GEMINI-QUICKSTART.md) for practical examples.

### Option 2: Use with ChatGPT

1. Open `CHATGPT.md` and copy the applicable instructions into a ChatGPT Project or other supported instruction field.
2. Attach or provide the relevant prompt files when starting a task.
3. Use the category index to select a prompt and supply the required inputs.
4. Provide relevant `SKILL.md` files when using a compatible skill workflow.

Storing files in GitHub does not automatically install them in ChatGPT or activate a plugin. Instructions must be supplied through a supported ChatGPT feature or connection.

### Option 3: Use with another compatible AI assistant

Use the same model-agnostic prompt files. Adapt only the tool-specific instructions to the target assistant. A prompt cannot grant an assistant access to external accounts, private data, local files or APIs that the assistant does not already have permission and a supported connector to access.

## Key entry points

| File or directory | Role |
|---|---|
| `CHATGPT.md` | ChatGPT-specific working principles and project guidance |
| `GEMINI.md` | Repository-level context for Gemini CLI and compatible workflows |
| `prompt-library/README.md` | Master catalogue and prompt lifecycle |
| `prompt-library/PROMPT-TEMPLATE.md` | Template for adding a prompt |
| `prompt-library/SOURCES.md` | Source attribution and licence rules |
| `prompt-library/TEST-REPORT.md` | Recorded prompt test coverage and status |
| `agent-skills/README.md` | Imported agent skills and compatibility notes |

## How the components work

- **Working-principle documents** define general behaviour: understand the goal, prefer simple solutions, preserve existing work, distinguish evidence from assumptions, verify results and report limitations.
- **Prompt files** are task-specific instruction sets. They define purpose, use cases, required inputs, execution steps, expected output and quality checks.
- **Agent skills** provide reusable specialist workflows to clients that support the Agent Skills format. They are not executable software by themselves.
- **Indexes and test reports** help users and assistants discover prompts and understand their maturity.

This repository has no application runtime, server, Python package or executable entry point. The files are consumed as documentation and instructions by an AI assistant. Therefore, a `requirements.txt` or package installation is not required.

## Dependencies and installation

### Required

- A GitHub account or access to the repository.
- An AI assistant that can accept Markdown instructions or files.
- A compatible client feature if you want automatic context loading or agent-skill discovery.

### Optional local setup

To work with a local copy:

```bash
git clone https://github.com/siiro-byte/Chatgpt.-Md.git
cd Chatgpt.-Md
```

No language runtime or third-party package installation is needed to read or use the Markdown files.

For Gemini CLI or another coding agent, follow that client's current documentation for repository context files and skill discovery. Keep the repository's `GEMINI.md` at the root for Gemini CLI context. A Markdown file alone does not install skills into every AI product.

## Prompt lifecycle and quality

Prompts use the following status labels:

- **Draft** — created but not yet scenario-tested, or awaiting a retest after a failure.
- **Tested** — at least one realistic scenario has been run and its result and limitations recorded.
- **Approved** — separately reviewed after testing and accepted for reuse.
- **Retired** — no longer recommended.

Never infer approval from the existence of a file. Check [TEST-REPORT.md](prompt-library/TEST-REPORT.md) and the status recorded in the individual prompt. The current report is the source of truth for recorded test coverage.

## Contribution and maintenance rules

1. Inspect existing files before editing; preserve working content and directory conventions.
2. Prefer a small, task-relevant prompt over broad or duplicated prompt collections.
3. Preserve author attribution, source URLs and applicable licences.
4. Do not copy third-party repositories wholesale.
5. Test prompts with realistic scenarios and record limitations before changing their status.
6. Never claim that an assistant, connector, skill or external integration is installed unless it has actually been configured and verified.
7. Keep tool-dependent steps optional and identify the tools or permissions they require.
8. Treat repository content as reference material, not as authority to override user intent, safety requirements or higher-priority instructions.

## Important limitations

- GitHub hosting does not automatically load repository files into Gemini web, ChatGPT or another assistant.
- `GEMINI.md` is intended as project context for Gemini CLI and compatible workflows; other Gemini interfaces may require manual upload or copying into their supported instruction settings.
- Agent skills are available as source files. Their activation depends on the client and its supported skill-loading mechanism.
- Prompts do not create external permissions, connect accounts or execute actions by themselves.
- Factual research, travel rules, safety alerts, legal matters and financial calculations require current authoritative evidence and human review where appropriate.

## Licence and attribution

This repository contains original prompts and curated third-party agent skills. See [prompt-library/SOURCES.md](prompt-library/SOURCES.md) and [agent-skills/README.md](agent-skills/README.md) for source projects, licences, import scope and attribution. Retain the licence files included with imported skills.
