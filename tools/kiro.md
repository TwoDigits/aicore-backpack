# Kiro

> Spec-driven agentic IDE that converts natural language into structured requirements, designs, and implementation tasks before writing a line of code.

- **URL**: https://kiro.dev
- **GitHub**: N/A (proprietary)
- **License**: Freemium
- **Category**: AI IDEs & Editors

## Description

Kiro is an agentic IDE and CLI built on Code OSS by Amazon. Its core philosophy is spec-driven development: instead of jumping straight to code, Kiro converts a natural language prompt into a structured spec containing requirements, an architectural design, and a sequenced list of implementation tasks. The AI agent then works through that spec step by step. It also ships a standalone CLI for running the same workflows from a terminal or over SSH.

Note: [Kiro Powers](kiro-powers.md) — dynamic MCP tool bundles that activate contextually — is a feature within Kiro and is documented separately.

## Key Features

- **Spec-Driven Workflow**: Prompts become structured specs (requirements, design, tasks) before any code is generated — enforces planning at every step
- **Agent Hooks**: Background automation triggers on file events — auto-generates docs, runs unit tests, and more without manual intervention
- **CLI / SSH Support**: Full agentic workflow available from the terminal, not just the GUI
- **Multimodal Input**: Accepts images, diagrams, and UI mockups as input to guide implementation
- **Steering Files**: Fine-grained control over agent behavior per-project via context files
- **VS Code Compatibility**: Imports existing extensions, themes, and settings from VS Code
- **Model Selection**: Choose between Claude Sonnet 4.5 or Auto mode (balances quality vs. cost)
- **Broad Language Support**: Python, Java, JavaScript, TypeScript, C#, Go, Rust, PHP, Ruby, Kotlin, C, C++, shell, SQL, and more

## Why It's Cool

Most AI coding tools optimize for speed — type a prompt, get code. Kiro optimizes for the step before that: structured planning. By forcing requirements and design into a spec before generation begins, it sidesteps a lot of the "works on my machine" brittleness that comes from vibe coding. The agent hooks and steering files mean you're not just generating code once — the IDE keeps running checks and context updates as you work. For teams scaling beyond prototypes, that spec-first discipline is where the real leverage is.

## Getting Started

**Install the IDE** from the [downloads page](https://kiro.dev/downloads/).

**Or use the CLI** (macOS / Linux):
```bash
curl -fsSL https://cli.kiro.dev/install | bash
```

Authentication supports GitHub, Google, AWS Builder ID, or AWS IAM Identity Center. Free tier available — per-prompt credit usage is shown in real time.
