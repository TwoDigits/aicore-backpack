# Harness Engineering

> OpenAI's methodology for agent-first software development where engineers design environments, specify intent, and build feedback loops instead of writing code.

- **URL**: https://openai.com/index/harness-engineering/
- **License**: N/A (methodology / blog post)
- **Category**: Methodologies & Approaches

## Description

Harness Engineering is a structured methodology published by OpenAI describing how a team of three engineers used Codex to build a million-line codebase in roughly five months — without writing a single line of code by hand. The methodology redefines the engineer's role: instead of coding, engineers design agent environments, curate context, and create feedback loops that enable AI agents to do reliable, autonomous work.

The approach grew out of practical necessity. Early progress was slower than expected — not because Codex was incapable, but because the environment was underspecified. The team's primary insight: the bottleneck is not the agent's ability, but the quality of the scaffolding around it. From this, a set of repeatable principles emerged for structuring repositories, managing knowledge, and enforcing code quality in agent-first workflows.

## Key Features

- **Depth-First Task Decomposition**: Break large goals into small building blocks (design, code, review, test), prompt the agent to construct them, then compose into more complex tasks
- **Map-Not-Manual Context Strategy**: Keep the root-level AGENTS.md short (~100 lines) as a table of contents pointing to deeper docs, rather than a monolithic instruction file
- **Repository as System of Record**: Catalogue and index design documentation with verification status and core beliefs that define agent-first operating principles
- **Boring Technology Preference**: Favor dependencies that are composable, API-stable, and well-represented in training data so agents can reason about them reliably
- **Enforcement Through Custom Linting**: Custom linters and structural tests inject remediation instructions into agent context — covering structured logging, naming conventions, file size limits, and reliability requirements
- **Golden Principles for Cleanup**: Encode opinionated, mechanical rules directly in the repo (e.g., prefer shared utility packages, validate data boundaries) and run recurring cleanup processes to keep the codebase legible for future agent runs
- **No Human Code Rule**: A core operating philosophy — humans never directly contribute code, maintaining the agent-first workflow throughout

## Why It's Cool

This is the most detailed public case study of building a production-scale codebase entirely with AI agents. The methodology tackles the hard problems that emerge when you go beyond "use an AI coding tool" to "make AI agents your primary developers": how to structure context so agents stay on track, how to enforce quality without manual code review, and how to maintain a million-line codebase that agents can continue to navigate. The 10x speed estimate (1/10th the time of manual coding) and 3.5 PRs per engineer per day throughput give concrete benchmarks for what agent-first development looks like at scale.

## Getting Started

1. Read the full article: [Harness Engineering: Leveraging Codex in an Agent-First World](https://openai.com/index/harness-engineering/)

2. Key principles to adopt in your own projects:
   - Keep your agent instruction file short — use it as a map, not a manual
   - Structure your docs/ directory as the system of record, indexed and catalogued
   - Write custom linters with error messages designed to guide agents toward fixes
   - Encode "golden principles" for code quality directly in the repository
   - Prefer boring, well-documented dependencies over novel ones
   - Break work depth-first into small, composable building blocks

3. Related OpenAI posts in the series:
   - [Unlocking the Codex Harness: How We Built the App Server](https://openai.com/index/unlocking-the-codex-harness/)
   - [Unrolling the Codex Agent Loop](https://openai.com/index/unrolling-the-codex-agent-loop/)
