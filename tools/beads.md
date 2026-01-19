# Beads (bd)

> Git-backed distributed graph issue tracker designed for AI agents with persistent memory

- **URL**: https://github.com/steveyegge/beads
- **GitHub**: https://github.com/steveyegge/beads
- **License**: MIT
- **Category**: claude-code

## Description

Beads provides persistent, structured memory for coding agents by replacing unorganized markdown plans with a dependency-aware task graph. Tasks are stored as JSONL files in a `.beads/` directory, enabling version control, branching, and merging like source code. This allows AI agents to maintain context and handle extended tasks without losing information across multiple sessions.

## Key Features

- **Git-Based Storage**: Tasks stored as JSONL files in `.beads/` directory with full version control support
- **Agent Optimized**: JSON output format, automatic dependency tracking, and task-readiness detection
- **Collision Prevention**: Hash-based IDs (e.g., `bd-a1b2`) eliminate merge conflicts in multi-agent or multi-branch scenarios
- **Performance Architecture**: SQLite caching for speed with background daemon for synchronization
- **Memory Efficiency**: Semantic compaction summarizes completed tasks to reduce context window usage
- **Hierarchical Tasks**: Support for epics and sub-tasks with IDs like `bd-a3f8.1.1`
- **Stealth Mode**: Private local use without repository commits
- **Community Extensions**: Terminal, web, and editor integrations available

## Why It's Cool

Beads solves a critical problem for AI coding agents: maintaining persistent memory and context across multiple sessions. Instead of losing track of complex task dependencies or forgetting completed work, agents can use Beads to:

- Track what needs to be done and what's blocking progress
- Understand task relationships and dependencies
- Resume work seamlessly across context windows
- Collaborate across multiple branches or agents without conflicts
- Compact completed work to save context window space

The git-backed architecture means task history is versioned alongside code, making it natural to branch strategies and merge workflows. With 11.2k GitHub stars and growing community support, it's becoming a standard tool for extended autonomous development sessions.

## Getting Started

Install via your preferred method:

```bash
# npm
npm install -g @beads/bd

# Homebrew
brew install steveyegge/beads/bd

# Go
go install github.com/steveyegge/beads/cmd/bd@latest
```

Basic usage:

```bash
# Display tasks without blockers
bd ready

# Create a priority task
bd create "Implement user authentication" -p 0

# Add task dependencies
bd dep add <child-task-id> <parent-task-id>

# View task details and history
bd show <task-id>
```

The tool integrates naturally with git workflows and is designed to be used by both humans and AI agents.
