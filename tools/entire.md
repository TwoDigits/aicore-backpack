# Entire

> Developer platform that captures AI agent sessions as searchable checkpoints on every Git push.

- **URL**: https://entire.io/
- **GitHub**: https://github.com/entireio/cli
- **License**: MIT
- **Category**: Observability

## Description

Entire hooks into your Git workflow to automatically capture AI agent sessions on every push, unifying your code with its context and reasoning. Traditional version control tracks *what* changed but not *why*. When agent sessions close, the prompts, decisions, and reasoning chains are lost forever. Entire solves this by creating **Checkpoints** — versioned captures of the full agent context stored alongside your code.

Session metadata is stored on a separate `entire/checkpoints/v1` branch, keeping your code commits clean while preserving the complete AI development context.

## Key Features

- **Automatic Checkpoint Capture**: Git hooks record agent sessions on every push without manual effort
- **Full Session Context**: Captures transcripts, prompts, files modified, token consumption, tool invocations, and reasoning chains
- **Searchable History**: Every agent conversation is indexed and searchable across your codebase
- **Multi-Agent Support**: Works with Claude Code and Gemini CLI, with both hooks enabled simultaneously
- **Local-First**: Runs locally without hosted services — your data stays yours
- **Clean Git History**: All session metadata lives on a separate branch, not in your code commits
- **Open Source**: MIT licensed, written in Go

## Why It's Cool

As AI agents become central to development workflows, the reasoning behind code changes becomes as important as the changes themselves. Entire preserves the "why" alongside the "what" — making AI-generated code reproducible, auditable, and collaborative. You can navigate to any prior checkpoint with full agent context intact, which is invaluable for code reviews, onboarding, and debugging AI-assisted changes. Backed by a $60M seed round, this is a serious bet on agent-aware version control.

## Getting Started

Install via Homebrew (macOS):

```bash
brew install entireio/tap/entire
```

Linux/WSL:

```bash
curl -fsSL https://entire.io/install.sh | bash
```

Or build from source (requires Go):

```bash
go install github.com/entireio/cli/cmd/entire@latest
```

Enable in your repository:

```bash
cd your-repo
entire enable
```

This installs Git hooks that automatically capture checkpoints. Start your AI agent (`claude` or `gemini`) and work as usual — on push, you'll be prompted to link commits to your active session.
