# Superpowers

> A skills framework for Claude Code that enables structured, test-driven development workflows with extended autonomous operation

- **URL**: https://github.com/obra/superpowers
- **GitHub**: https://github.com/obra/superpowers
- **License**: MIT
- **Category**: Claude Code

## Description

Superpowers is an open-source skills library that transforms Claude Code into a more structured and autonomous development partner. It provides composable, reusable workflows that enforce best practices like test-driven development and systematic planning. The framework is designed to prevent premature coding by first validating specifications and creating detailed plans before execution.

The tool enables Claude to work autonomously for extended periods (often a couple of hours at a time) by using fresh subagents per task, reducing context confusion and maintaining focus throughout complex implementations.

## Key Features

- **Design Refinement**: Interactive brainstorming to validate and refine specifications before implementation
- **Implementation Planning**: Breaks work into bite-sized tasks (2-5 minutes each) for manageable execution
- **Test-Driven Development**: Enforces RED-GREEN-REFACTOR cycles for quality assurance
- **Subagent-Driven Execution**: Spawns fresh subagents per task for parallel execution without context pollution
- **Automated Code Review**: Built-in review processes to catch issues early
- **Git Worktree Management**: Isolated development environments for each feature or task
- **Skills Library**: Includes testing, debugging, collaboration, and meta-skills categories

## Why It's Cool

Superpowers addresses one of the key challenges with AI coding assistants: maintaining consistent quality over extended autonomous work sessions. By enforcing structured workflows and TDD practices, it helps Claude Code produce more reliable, well-tested code. The subagent architecture means each task starts fresh, avoiding the context degradation that can happen in long sessions. With 9.8k+ GitHub stars, it's become a popular choice for developers wanting to maximize their Claude Code productivity.

## Getting Started

**Install via Claude Code Plugin Marketplace:**

```bash
/plugin marketplace add obra/superpowers-marketplace
/plugin install superpowers@superpowers-marketplace
```

**For other platforms** (Codex, OpenCode), check the repository's platform-specific directories for installation instructions.

Once installed, Superpowers provides skills that can be invoked during your development workflow to guide Claude through structured design, planning, implementation, and review phases.
