# DevSkills

> MCP server for sharing AI agent skills across coding tools

- **URL**: https://github.com/mk0e/devskills
- **GitHub**: https://github.com/mk0e/devskills
- **License**: MIT
- **Category**: MCP Servers & Integrations

## Description

DevSkills brings Anthropic's Agent Skills framework to any MCP-compatible coding agent. It enables teams to create a centralized repository of development workflows that any team member's AI assistant can access, regardless of which tool they use (Claude Code, Cursor, GitHub Copilot, etc.).

The tool acts as a bridge between skill definitions and AI coding agents, exposing skills through the Model Context Protocol. Agents can discover available workflows, load detailed instructions on demand, and execute tasks following predefined patterns.

## Key Features

- **Shared Skill Repository**: Define workflows once and reuse them across multiple AI agents
- **MCP Protocol Support**: Works with Claude Code, Cursor, GitHub Copilot, and other MCP-compatible tools
- **Progressive Disclosure**: Agents see skill summaries first, load detailed instructions only when needed
- **Bundled Skills**: Includes default skills with custom extension capability
- **Built-in Skill Creator**: Guided workflow for creating new skills with correct structure

## Why It's Cool

DevSkills solves a key challenge in AI-assisted development: consistency across teams and tools. Instead of each developer explaining the same workflows to their AI assistant repeatedly, teams can encode best practices into reusable skills that work across any MCP-compatible tool. This reduces friction, improves collaboration, and ensures everyone's AI assistant follows the same development patterns.

## Getting Started

Initialize a new skills repository:

```bash
uvx devskills init my-team-skills
cd my-team-skills
git init && git add . && git commit -m "Initial commit"
```

Configure in your MCP client with a `--skills-path` argument pointing to your skills directory.
