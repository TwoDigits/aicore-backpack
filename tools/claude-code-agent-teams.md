# Claude Code Agent Teams

> Built-in multi-agent orchestration that coordinates multiple Claude Code sessions with shared tasks, inter-agent messaging, and parallel execution.

- **URL**: https://code.claude.com/docs/en/agent-teams
- **GitHub**: N/A (built-in Claude Code feature)
- **License**: Proprietary (Claude Code)
- **Category**: Claude Code

## Description

Agent Teams is an experimental built-in feature that lets you orchestrate multiple Claude Code instances working together as a coordinated team. One session acts as the team lead — spawning teammates, assigning tasks, and synthesizing results — while teammates work independently in their own context windows and communicate directly with each other. Unlike subagents (which run within a single session and only report back), teammates are full Claude Code sessions that can message each other, self-claim tasks, and be interacted with directly.

## Key Features

- **Multi-session orchestration**: A lead session spawns and coordinates independent Claude Code teammate instances, each with its own context window
- **Shared task list with dependencies**: Tasks are tracked centrally with pending/in-progress/completed states and automatic dependency resolution via file locking
- **Inter-agent messaging**: Teammates send direct messages and broadcasts to each other — not just back to the lead
- **Direct teammate interaction**: Message any teammate individually using Shift+Up/Down (in-process) or click into their pane (split mode)
- **Delegate mode**: Restricts the lead to coordination-only (Shift+Tab), preventing it from implementing tasks itself
- **Plan approval gates**: Require teammates to plan in read-only mode before implementing; the lead reviews and approves/rejects
- **Split-pane display**: Each teammate gets its own terminal pane via tmux or iTerm2 for simultaneous visibility
- **Quality enforcement hooks**: `TeammateIdle` and `TaskCompleted` hooks let you enforce rules when teammates finish work

## Why It's Cool

Agent Teams turns Claude Code from a single-agent tool into a multi-agent development platform. Instead of working through tasks sequentially, you can spin up parallel reviewers that each apply a different lens to a PR, investigators that debate competing hypotheses about a bug, or builders that each own a separate module. The direct peer-to-peer communication is the differentiator — teammates can challenge each other's findings and converge on answers, something subagents can't do. The delegate mode and plan approval gates give you fine-grained control over how autonomous the team gets.

## Getting Started

1. Enable the experimental feature:
   ```json
   // settings.json
   {
     "env": {
       "CLAUDE_CODE_EXPERIMENTAL_AGENT_TEAMS": "1"
     }
   }
   ```

2. Describe your team in natural language:
   ```
   Create an agent team to review PR #142. Spawn three reviewers:
   - One focused on security implications
   - One checking performance impact
   - One validating test coverage
   ```

3. Choose a display mode (optional):
   ```json
   // settings.json — "auto" (default), "in-process", or "tmux"
   {
     "teammateMode": "in-process"
   }
   ```

4. Interact with teammates using Shift+Up/Down, use Shift+Tab for delegate mode, and press Ctrl+T to toggle the task list.

**Note**: Agent teams are experimental with known limitations around session resumption, task coordination, and shutdown behavior. Each teammate is a separate Claude instance, so token usage scales with team size.
