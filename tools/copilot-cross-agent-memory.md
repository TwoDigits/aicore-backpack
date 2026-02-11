# Copilot Cross-Agent Memory

> Agentic memory system that lets GitHub Copilot agents remember and learn across coding, code review, and CLI sessions.

- **URL**: https://github.blog/ai-and-ml/github-copilot/building-an-agentic-memory-system-for-github-copilot/
- **GitHub**: N/A (built-in Copilot feature)
- **License**: Proprietary (GitHub Copilot)
- **Category**: GitHub Copilot

## Description

Cross-Agent Memory is a built-in system that enables GitHub Copilot agents to retain and share knowledge across your entire development workflow. When the coding agent, code review agent, or CLI agent discovers a pattern — such as keeping API version numbers synchronized across client SDK, server routes, and documentation — it stores that knowledge with citations to specific code locations. Other agents then verify and reuse these memories in future sessions, creating a persistent learning loop without requiring explicit user instructions each time.

## Key Features

- **Cross-agent knowledge sharing**: Memories created by one agent (e.g., code review) are automatically available to others (coding agent, CLI), enabling workflow-wide learning
- **Just-in-time verification with citations**: Memories store references to specific code locations; agents verify citations against the current codebase before acting on them
- **Self-healing memories**: When agents detect outdated or contradictory information, they store corrected versions automatically
- **Repository-scoped access**: Memories are bound to their source repository and respect existing code permissions
- **Measurable impact**: A/B testing showed a 7% increase in PR merge rates and 2% improvement in positive code review feedback
- **Adversarial resilience**: Deliberately seeded false memories were consistently caught and corrected through citation verification

## Why It's Cool

This is one of the first production-scale implementations of persistent memory across multiple AI coding agents. Rather than treating each Copilot interaction as stateless, the system builds a shared knowledge base that grows with your codebase. The citation-based verification approach is particularly elegant — instead of expensive offline curation, memories are validated in real-time with lightweight read operations. The result: a code review agent learns your logging conventions, and the coding agent automatically applies them to new microservices, while the CLI uses those patterns for debugging.

## Getting Started

1. Enable memory in your GitHub Copilot settings (currently in public preview)
2. Available for all paid Copilot plans
3. Works automatically across the Copilot coding agent, code review, and CLI
4. Agents will begin extracting and verifying learnings as you work — no manual configuration needed
