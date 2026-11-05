# Gemini Quickstart

This guide explains how to use the repository's prompts and agent skills with Google Gemini. The exact loading method depends on which Gemini product or client you use.

## Gemini CLI

1. Install a supported Node.js version and Gemini CLI by following the [official installation guide](https://github.com/google-gemini/gemini-cli/blob/main/docs/installation.md). The documented npm installation command is:
   ```bash
   npm install -g @google/gemini-cli
   ```
2. Clone the repository:
   ```bash
   git clone https://github.com/siiro-byte/Chatgpt.-Md.git
   cd Chatgpt.-Md
   ```
3. Confirm that `GEMINI.md` is present at the repository root.
4. Start Gemini CLI from the repository directory:
   ```bash
   gemini
   ```
5. Verify that the project instructions loaded by running `/memory show`. The output should include the repository's root `GEMINI.md`. If it does not, check the working directory, trusted-folder status and context-file settings.
6. Ask Gemini to read `prompt-library/README.md`, select the relevant category and open the complete prompt file before beginning the task.
7. For specialist workflows, ask Gemini to inspect the relevant `agent-skills/<source>/<skill>/SKILL.md` and any referenced local resources. Do not assume every imported skill is automatically registered as an installed extension.

Example request:

> Read GEMINI.md and prompt-library/README.md. Select the most relevant prompt for my task, read it completely, identify any essential missing inputs, then carry out the work. Follow the prompt's quality checks and distinguish verified results from assumptions.

## Gemini web, Gems or AI Studio

These interfaces may not automatically read a GitHub repository or its root `GEMINI.md`.

1. Open the repository on GitHub.
2. Download or copy `GEMINI.md` and the relevant prompt file.
3. Add the instructions and files through the interface's supported Gem instructions, knowledge files or chat attachments.
4. If file limits apply, provide only the root instructions, the category index and the single relevant prompt rather than uploading the entire repository.
5. Ask Gemini to confirm which files it can actually read before relying on them.

Example request:

> Use the attached GEMINI.md as project guidance. Read the attached prompt in full and apply it to the task below. Do not assume access to files or tools that are not attached or connected.

## Selecting a prompt

Start at [Master Prompt Library](README.md). The current categories are:

- [Research & Intelligence](research-intelligence/README.md)
- [Marketing & Growth](marketing-growth/README.md)
- [Travel Editorial](travel-editorial/README.md)
- [Business & Strategy](business-strategy/README.md)
- [Writing & Communication](writing-communication/README.md)
- [Image, Video & Audio](image-video-audio/README.md)
- [Coding & Technology](coding-technology/README.md)
- [Productivity & Learning](productivity-learning/README.md)

Read the selected prompt from beginning to end. It contains the purpose, when to use it, required inputs, instructions, expected output, quality checks, source and current status.

## Reusable task wrapper

Use this wrapper when you want Gemini to apply a prompt consistently:

```text
TASK
[Describe the outcome you need.]

SOURCE MATERIAL
[Paste or attach the relevant text, data or files.]

PROMPT TO APPLY
[Path to the selected prompt file.]

CONSTRAINTS
[State deadlines, audience, format, budget, tools or other material limits.]

EXECUTION RULES
- Read the complete selected prompt before starting.
- Ask only for missing information that materially changes the result.
- Do not invent facts, sources, figures, permissions or completed actions.
- Use tools only when they are available and authorised in this Gemini session.
- Separate facts, assumptions, hypotheses and recommendations.
- Follow the prompt's expected output and quality checks.
- State which checks were actually performed and what remains unverified.
```

## Tool and access limitations

A prompt cannot grant access to external services. Browsing, GitHub writes, code execution, email, calendars, local files and other integrations depend on the Gemini product, enabled tools, account permissions and user authorisation.

Do not ask Gemini to claim it has searched, tested, committed, deployed or connected something unless the corresponding action was actually completed. For repository changes, require a reviewed diff and a verified commit.

## Prompt status

Check [TEST-REPORT.md](TEST-REPORT.md) before relying on a prompt as tested. A prompt marked Draft has not completed the required scenario testing. Tested does not mean universally reliable, and Approved requires a separate review.

## Dependencies

No Python, Node.js or package dependencies are required to read or use this Markdown library. Gemini CLI itself is an optional client and requires Node.js; install it separately using Google's [official Gemini CLI instructions](https://github.com/google-gemini/gemini-cli).
