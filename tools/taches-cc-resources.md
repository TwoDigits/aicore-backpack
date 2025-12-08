# TACHES Claude Code Resources

> Comprehensive collection of 27 commands, 7 skills, and 3 specialized agents for enhanced AI-assisted development workflows.

- **URL**: https://github.com/glittercowboy/taches-cc-resources
- **GitHub**: https://github.com/glittercowboy/taches-cc-resources
- **License**: Not specified
- **Category**: Claude Code

## Description

TACHES is a sophisticated toolkit for Claude Code that provides structured workflows for building, planning, and debugging. It features a meta-prompting system that separates analysis from execution, 12 thinking model commands (including Pareto analysis, first principles, and inversion), and specialized agents for quality assurance. The project emphasizes context management for multi-session work and self-healing capabilities for sustained AI collaboration.

## Key Features

- **27 Commands**: Including meta-prompting, todo management, context handoff, and 12 thinking model commands
- **7 Skills**: Autonomous workflows for hierarchical planning, agent skill creation, meta-prompt generation, slash command building, and expert-level debugging
- **3 Specialized Agents**: Auditor subagents for quality assurance of skills, commands, and agent configurations
- **Deep Analysis Debugging**: Evidence-gathering methodology for complex debugging scenarios
- **Context Handoff**: Capabilities for maintaining context across multi-session work
- **Self-Healing Skills**: Automatic recovery and adaptation mechanisms

## Why It's Cool

TACHES represents an advanced approach to AI-assisted development that goes beyond simple prompts. The hierarchical planning system is optimized for solo developers, making complex projects more manageable. The meta-prompting architecture (separating thinking from doing) and domain-aware expertise loading suggest patterns that could significantly improve how developers collaborate with AI on sustained, complex projects.

## Getting Started

**Option 1 - Plugin Installation (Recommended):**
```bash
claude plugin marketplace add glittercowboy/taches-cc-resources
claude plugin install taches-cc-resources
```

**Option 2 - Manual Installation:**
1. Clone the repository
2. Copy commands to `~/.claude/commands/`
3. Copy skills to `~/.claude/skills/`
