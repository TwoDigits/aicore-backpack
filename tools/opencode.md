# OpenCode

> Open-source, provider-agnostic AI coding agent with autonomous build and plan modes, available as a terminal, desktop app, and IDE extension.

- **URL**: https://opencode.ai/
- **GitHub**: https://github.com/anomalyco/opencode
- **License**: MIT
- **Category**: AI IDEs & Editors

## Description

OpenCode is a fully open-source AI coding agent built by the creators of terminal.shop. Its core value proposition for autonomous coding is a dual-agent architecture: a **build agent** with full read/write/execute access for hands-on development, and a **plan agent** that performs read-only analysis and requests permission before running any commands. This gives developers a tunable level of autonomy depending on the task.

Rather than being tied to a single model provider, OpenCode is provider-agnostic — it works with Claude, OpenAI, Google, and 75+ other LLM providers including locally-hosted models. A client/server architecture lets it operate remotely, and it ships as a terminal UI, a desktop app (macOS, Windows, Linux), and an IDE extension, so it fits into whatever workflow a developer already uses.

## Key Features

- **Dual-agent modes** — "build" agent for full autonomous coding; "plan" agent for read-only analysis with explicit permission gates before executing commands
- **Provider-agnostic** — connects to 75+ LLM providers (Claude, OpenAI, Google, local models) with no lock-in
- **LSP integration** — Language Server Protocol support loads automatically, giving the agent IDE-grade code intelligence
- **Multi-session** — run multiple coding agents concurrently within a single instance
- **Client/server architecture** — decouple the agent runtime from the interface; operate remotely or swap clients freely
- **Cross-platform** — terminal UI, desktop app (macOS Intel/Apple Silicon, Windows, Linux), and IDE extension
- **Session sharing** — shareable links let teammates inspect or resume an agent's session
- **Privacy-first** — no user code or context is stored or sent outside the chosen model provider

## Why It's Cool

For developers evaluating autonomous coding agents, OpenCode stands out on two fronts. First, the build/plan agent split is a practical answer to the "how much should the agent do unsupervised?" question — you get full autonomy when you want speed, and a permission-gated planning mode when you want control. Second, its genuine provider-agnosticism means you're never locked into one model or one cost structure; switch between cloud APIs and local models based on sensitivity or budget without changing your workflow. With 96k+ GitHub stars and an MIT license, it's one of the most actively developed open-source coding agents available.

## Getting Started

Quick install via curl:

```bash
curl -fsSL https://opencode.ai/install | bash
```

Alternative installation methods:

- **npm**: `npm install -g opencode`
- **Homebrew** (macOS): `brew install opencode`
- **Scoop** (Windows): `scoop install opencode`
- **Arch Linux**: `paru -S opencode`
- **Desktop app**: Download from [opencode.ai/download](https://opencode.ai/download)
