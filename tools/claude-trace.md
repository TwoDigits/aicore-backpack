# Claude Trace

> Logging and visualization tool that records all interactions with Claude Code as developers work on projects.

- **URL**: https://github.com/badlogic/lemmy/tree/main/apps/claude-trace
- **GitHub**: https://github.com/badlogic/lemmy
- **License**: MIT
- **Category**: Claude Code

## Description

Claude Trace is a debugging and analysis tool that captures the complete conversation flow between developers and Claude Code. It reveals hidden system prompts, tool outputs, raw API data, and thinking blocks that Claude normally conceals, presenting everything in an intuitive web interface.

## Key Features

- **System Prompt Visibility** - See the hidden system prompts Claude receives
- **Tool Definition & Output Logging** - Capture all tool calls and their results
- **Thinking Block Inspection** - View Claude's reasoning process in thinking blocks
- **Token Usage Breakdown** - Detailed analytics including cache statistics
- **Raw JSONL Logs** - Access raw API data for detailed analysis
- **Interactive HTML Viewer** - Browse conversations with model filtering
- **Debug Views** - Inspect all HTTP requests
- **AI-Powered Summaries** - Generate conversation summaries and searchable session indexes

## Why It's Cool

Developers gain transparency into Claude's reasoning process, tool interactions, and decision-making—essential for debugging, understanding model behavior, and optimizing agent workflows. The indexing feature enables quick discovery across multiple sessions, making it invaluable for understanding how Claude Code works under the hood.

## Getting Started

### Installation

```bash
npm install -g @mariozechner/claude-trace
```

### Requirements

- Node.js 16+
- Claude Code CLI installed

### Usage

```bash
# Start logging Claude Code interactions
claude-trace

# Capture all API calls including non-conversation requests
claude-trace --include-all-requests

# Generate HTML report from logs
claude-trace --generate-html logs.jsonl report.html
```

Logs are saved to `.claude-trace/` as self-contained HTML files that can be viewed in any browser.
