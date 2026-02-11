# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

AICore Backpack is a curated collection of cool AI tools, extensions, and open-source alternatives for software developers. This is not a list of essential tools, but rather interesting discoveries to enhance AI-powered development workflows.

## Repository Structure

```
├── README.md                    # Main list with categorized tools
├── tools/                       # Detailed documentation for each tool
│   └── [tool-name].md           # Individual tool documentation
└── .claude/commands/            # Custom Claude Code commands
    ├── add-tool.md              # Command to add new tools
    ├── discover-tools.md        # Command to discover new tools via research agents
    └── reorganize-categories.md # Command to reorganize categories
```

## Commands

### `/add-tool [url]`

Adds a new tool to the curated list:
1. Analyzes the provided URL
2. Creates documentation in `tools/[tool-name].md`
3. Categorizes and adds entry to README.md
4. Prompts for category selection if unclear

### `/discover-tools`

Discovers new AI tools via parallel research agents:
1. Reads existing tools to build an exclusion list
2. Launches 8 parallel sub-agents, each covering a different research angle (IDEs, frameworks, MCP, methodologies, open-source, Claude Code/Copilot, observability, trending)
3. Deduplicates and ranks findings by confidence
4. Presents a curated summary grouped by category
5. Lets the user multi-select which tools to add
6. Adds selected tools via `/add-tool`

### `/reorganize-categories`

Analyzes and reorganizes tool categorizations:
1. Reads all categories and tools from README.md
2. Reads each tool's documentation for context
3. Evaluates if current categorizations are optimal
4. Presents suggestions for recategorization
5. Implements approved changes after user confirmation

## Tool Categories

Tools are organized by these categories (defined in README.md):
- `agent-frameworks` - Frameworks and libraries for building AI agents
- `platforms` - Central platforms for AI model discovery and collaboration
- `local-ai` - Local/self-hosted AI solutions
- `mcp` - MCP servers and integrations
- `observability` - LLM monitoring, tracing, and debugging
- `methodologies` - Structured methodologies for AI-assisted development
- `prompt-engineering` - Prompt tools and management
- `claude-code` - Tools specifically for Claude Code
- `documentation` - Docs generation and knowledge tools
- `open-source` - Open-source alternatives
- `ai-mindset` - Videos and talks about AI mindset, ROI, and adoption
- `experimental` - Research and experimental tools

## Adding Tools Manually

If adding a tool without the command:
1. Create `tools/[tool-name].md` with standard template
2. Add entry to README.md between the appropriate `<!-- TOOLS:[category] -->` markers
