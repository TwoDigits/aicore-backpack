# Ralph Loop

> Self-referential AI development loop that enables Claude Code to autonomously iterate on tasks until completion

- **URL**: https://github.com/anthropics/claude-plugins-official/tree/main/plugins/ralph-loop
- **GitHub**: https://github.com/anthropics/claude-plugins-official
- **License**: Anthropic Official Plugin
- **Category**: Claude Code

## Description

Ralph Loop is an official Claude Code plugin that implements an iterative, self-referential development methodology. Inspired by the "Ralph Wiggum technique," it creates a feedback loop where Claude autonomously works on tasks through repeated cycles, continuously improving until a completion marker is output.

The core concept is elegantly simple: "Ralph is a Bash loop" - a `while true` that repeatedly feeds an AI agent a prompt file. When Claude attempts to exit, a Stop hook intercepts the exit and feeds the same prompt back. Claude's previous work persists in files and git history, allowing each iteration to see and improve upon modified files.

## Key Features

- **Self-Referential Feedback Loop**: Automatic re-prompting when Claude exits, enabling continuous iteration
- **Persistent Context**: Work persists in files and git history between iterations
- **Configurable Iteration Limits**: Set maximum iterations with `--max-iterations` for safety
- **Completion Promises**: Define clear exit criteria with `--completion-promise`
- **Simple Commands**: `/ralph-loop` to start, `/cancel-ralph` to stop

## Why It's Cool

Ralph Loop enables truly autonomous development sessions where you can "walk away" while Claude iteratively builds features, fixes bugs, and runs tests. Real-world results are impressive:

- Successfully generated 6 repositories overnight in Y Combinator hackathon testing
- One $50k contract completed for $297 in API costs
- Created an entire programming language over 3 months using this approach

It's particularly powerful for tasks with automatic verification (tests, linters) where success criteria are objectively measurable.

## Getting Started

Install via Claude Code plugin system:

```bash
/plugin install ralph-loop@claude-plugin-directory
```

Basic usage:

```bash
/ralph-loop "Build a REST API for todos. Requirements: CRUD operations, input validation, tests. Output <promise>COMPLETE</promise> when done." --completion-promise "COMPLETE" --max-iterations 50
```

**Best practices for prompts:**
1. Define clear completion criteria with a completion promise
2. Break complex tasks into incremental phases
3. Include self-correction instructions (e.g., "run tests, if fail, fix and retry")
4. Always use `--max-iterations` as a safety net

## When to Use

**Good for:**
- Well-defined tasks with clear success criteria
- Tasks requiring iteration and refinement (getting tests to pass)
- Greenfield projects where you can walk away
- Tasks with automatic verification

**Not good for:**
- Tasks requiring human judgment or design decisions
- One-shot operations
- Tasks with unclear success criteria

## Learn More

- Original technique: https://ghuntley.com/ralph/
- Ralph Orchestrator: https://github.com/mikeyobrien/ralph-orchestrator
