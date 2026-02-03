# Codex CLI

> OpenAI's open-source, Rust-powered terminal coding agent with autonomous file editing, command execution, and MCP support.

- **URL**: https://openai.com/codex/
- **GitHub**: https://github.com/openai/codex
- **License**: Apache-2.0
- **Category**: ai-ides-editors

## Description

Codex CLI is OpenAI's locally-running, autonomous coding agent built in Rust. It operates entirely from your terminal — reading files, writing code, and executing commands in your project directory without requiring a browser or IDE. The agent mode is on by default, meaning it can autonomously iterate on tasks: understanding your codebase, implementing features, fixing bugs, and running tests in a single loop. Code stays local unless you explicitly share it; only prompts and high-level context are sent to the model.

## Key Features

- **Autonomous agent mode** — reads, modifies, and executes code in your project directory by default, with configurable approval levels for safety
- **MCP (Model Context Protocol) support** — expose third-party tools and additional context to the agent, or run Codex itself as an MCP server for orchestration
- **Multi-agent orchestration** — integrates with the OpenAI Agents SDK to build deterministic, auditable software delivery pipelines
- **Image and screenshot inputs** — attach wireframes or design specs alongside text prompts for visual-to-code workflows
- **AGENTS.md custom instructions** — layered, per-project instruction files that set consistent expectations before each task
- **Model switching** — toggle between GPT-5-Codex and GPT-5 models at runtime via the `/model` command
- **Built-in code review and web search** — run local reviews before committing, and pull in up-to-date information during tasks
- **Cross-platform** — native binaries for macOS and Linux; experimental Windows support via WSL

## Why It's Cool

Codex CLI brings OpenAI's frontier coding model directly into your terminal as a fully autonomous agent — no IDE required. For developers who already live in the terminal, it's the most direct path to agentic coding: drop into a directory, describe what you need, and let it iterate. The Rust-based architecture keeps it fast and lightweight, MCP integration means it slots cleanly into existing tool chains, and the ability to orchestrate it as part of a multi-agent pipeline via the Agents SDK opens the door to scripted, auditable software workflows that go well beyond single-shot code generation.

## Getting Started

Install via npm or Homebrew:

```sh
npm i -g @openai/codex
# or
brew install --cask codex
```

Precompiled binaries are also available on the [GitHub Releases](https://github.com/openai/codex/releases) page for macOS (Apple Silicon & x86_64) and Linux (x86_64 & arm64).

Authenticate with a ChatGPT account (included with Plus, Pro, Business, Edu, and Enterprise plans) or an OpenAI API key, then run:

```sh
codex
```

This starts an interactive agent session in your current directory. Place an `AGENTS.md` file at the repo root to provide project-specific instructions that Codex reads automatically before each task.
