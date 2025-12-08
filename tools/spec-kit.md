# Spec Kit

> A toolkit for spec-driven development where specifications become executable and directly generate working implementations.

- **URL**: https://github.com/github/spec-kit
- **GitHub**: https://github.com/github/spec-kit
- **License**: MIT
- **Category**: Methodologies & Approaches

## Description

Spec Kit is an open-source toolkit from GitHub that enables spec-driven development. Instead of treating specifications as documentation that guides manual coding, Spec Kit makes specifications executable - they directly generate working implementations through AI coding agents.

The approach flips traditional development: rather than "vibe coding" every piece from scratch, developers focus on product scenarios and predictable outcomes. The toolkit works with 10+ AI coding agents including Claude Code, GitHub Copilot, Cursor, Gemini, Windsurf, and Qwen.

## Key Features

- **Constitution**: Establish project governing principles and development guidelines
- **Specify**: Define requirements in plain language without focusing on technical implementation
- **Plan**: Create technical implementation strategies with chosen technology stacks
- **Tasks**: Generate actionable task lists from implementation plans
- **Implement**: Execute all tasks to build features according to specifications
- **Clarify**: Address underspecified areas before implementation
- **Analyze**: Check cross-artifact consistency
- **Checklist**: Generate quality validation checklists

## Why It's Cool

Spec Kit represents a fundamental shift in AI-assisted development:

- **Structure over chaos**: Provides a repeatable methodology instead of ad-hoc prompting
- **Multi-step refinement**: Breaks down complex features into constitution → spec → plan → tasks → implementation
- **Agent-agnostic**: Works with any major AI coding assistant
- **Quality built-in**: Includes consistency analysis and checklist generation
- **Enterprise-ready**: Supports organizational constraints and compliance requirements
- **GitHub-backed**: Developed and maintained by GitHub, signaling strong commitment

## Getting Started

**Install permanently (recommended):**
```bash
uv tool install specify-cli --from git+https://github.com/github/spec-kit.git
```

**One-time usage:**
```bash
uvx --from git+https://github.com/github/spec-kit.git specify init <PROJECT_NAME>
```

**Basic workflow:**
1. `specify constitution` - Set up project principles
2. `specify specify` - Define feature requirements
3. `specify plan` - Create technical plan
4. `specify tasks` - Generate task list
5. `specify implement` - Build the feature

The CLI integrates directly with your AI coding agent of choice.
