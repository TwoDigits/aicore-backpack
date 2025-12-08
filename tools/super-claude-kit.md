# Super Claude Kit

> A persistence layer that transforms Claude Code from stateless to stateful with cross-session context memory.

- **URL**: https://github.com/arpitnath/super-claude-kit
- **GitHub**: https://github.com/arpitnath/super-claude-kit
- **License**: MIT
- **Category**: Claude Code

## Description

Super Claude Kit is a persistence layer for Claude Code that adds persistent context memory, eliminating the need to repeatedly explain your project structure and decisions across sessions. It works by capturing and restoring project context automatically through hooks, making Claude Code "remember" your codebase between sessions.

The tool uses a custom TOON format for storage that achieves 52% token reduction compared to JSON, making context restoration more efficient. It integrates seamlessly with existing Claude Code installations and requires no changes to your workflow.

## Key Features

- **Persistent Memory**: Eliminates redundant file re-reads by remembering what Claude has already learned about your codebase
- **Context Capsule**: Displays git state, accessed files, discoveries, and task tracking in a compact format
- **Dependency Intelligence**: Scanning tools that help Claude understand code relationships and dependencies
- **Progressive Reader**: Handles large files with semantic chunking for better comprehension
- **Specialized Sub-agents**: Architecture exploration and database navigation agents
- **Token Efficient**: TOON format achieves 52% token reduction vs JSON

## Why It's Cool

Claude Code's statelessness means every new session starts from scratch - you have to re-explain your project structure, coding conventions, and previous decisions. Super Claude Kit solves this by providing "hands-free context restoration between sessions." This dramatically reduces cognitive overhead and token consumption during extended development sessions, making Claude Code feel more like a teammate who actually remembers your project.

## Getting Started

Install from your project root:

```bash
curl -fsSL https://raw.githubusercontent.com/arpitnath/super-claude-kit/master/install | bash
```

**Requirements:**
- Claude Code (Desktop CLI or VSCode extension)
- macOS or Linux (WSL supported)
- Go 1.23+
- Bash 4.0+
- Git (optional, for enhanced branch tracking)

The tool installs to `.claude/` directory and works alongside vanilla Claude Code without any conflicts.
