# Long-Running Agent Harness

> A methodology for enabling AI agents to work effectively across multiple context windows by maintaining state and progress through discrete coding sessions.

- **URL**: https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents
- **GitHub**: https://github.com/anthropics/claude-quickstarts/tree/main/autonomous-coding
- **License**: MIT (quickstart examples)
- **Category**: Methodologies & Approaches

## Description

The Long-Running Agent Harness is a two-part solution developed by Anthropic that enables AI agents to maintain continuity across multiple context windows. It addresses the fundamental challenge of context window limitations by providing a structured approach to session initialization, progress tracking, and incremental feature development.

The methodology consists of two specialized agents:

**Initializer Agent**: Sets up the development environment on first run by creating an `init.sh` script for development server startup, generating a `claude-progress.txt` file for tracking work history, producing an initial git commit, and building a comprehensive feature list (200+ features in test examples).

**Coding Agent**: Works on single features per session, leaving structured updates for subsequent sessions, committing changes with descriptive git messages, and using browser automation for end-to-end testing.

## Key Features

- **Progress Tracking**: Git history combined with progress notes enables quick context recovery between sessions
- **Feature List Management**: Structured JSON file tracking end-to-end feature descriptions marked as passing/failing
- **Session Initialization Protocol**: Agents run `pwd`, read progress files, and check git logs before starting work
- **Browser Automation Testing**: Uses Puppeteer MCP for human-like verification beyond unit tests
- **Incremental Development**: Prevents agents from attempting full implementation in a single session
- **Clean Code State**: Maintains mergeable, production-quality code throughout development

## Why It's Cool

This methodology solves one of the biggest challenges with autonomous AI coding agents: context window exhaustion. Instead of trying to build everything at once (and failing mid-feature), agents work incrementally like human developers, maintaining clear documentation of progress. The structured approach to session handoffs means agents can identify and fix accumulated bugs before adding new features, resulting in cleaner, more maintainable code.

## Getting Started

1. Clone the quickstart repository:
   ```bash
   git clone https://github.com/anthropics/claude-quickstarts.git
   cd claude-quickstarts/autonomous-coding
   ```

2. Review the example initializer and coding agent configurations

3. Key components to implement:
   - `init.sh` - Development server startup script
   - `claude-progress.txt` - Progress tracking file
   - Feature list JSON - Structured feature tracking
   - Session initialization prompts that read existing state

4. Ensure your agent reads progress files, git logs, and feature status before beginning each session
