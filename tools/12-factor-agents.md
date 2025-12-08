# 12-Factor Agents

> Design principles for building reliable, production-ready LLM-powered software applications.

- **URL**: https://github.com/humanlayer/12-factor-agents
- **GitHub**: https://github.com/humanlayer/12-factor-agents
- **License**: Open Source
- **Category**: Methodologies & Approaches

## Description

12-Factor Agents is a comprehensive methodology that establishes design principles for building reliable, production-ready LLM-powered software. Created by Dex Horthy from HumanLayer, it adapts the philosophy of the original 12-Factor Apps methodology to AI agent systems.

The framework addresses the fundamental question: "What are the principles we can use to build LLM-powered software that is actually good enough to put in the hands of production customers?"

This repository coined the term "Context Engineering" back in April 2025.

## The 12 Principles

1. **Natural Language to Tool Calls** - Convert natural language into structured tool calls
2. **Own Your Prompts** - Take control of your prompt engineering
3. **Own Your Context Window** - Manage what goes into your context effectively
4. **Tools Are Just Structured Outputs** - Treat tools as a way to get structured responses
5. **Unify Execution State and Business State** - Keep state management coherent
6. **Launch/Pause/Resume with Simple APIs** - Design for interruptible workflows
7. **Contact Humans with Tool Calls** - Build in human-in-the-loop capabilities
8. **Own Your Control Flow** - Don't delegate control flow entirely to the LLM
9. **Compact Errors into Context Window** - Handle errors gracefully within context
10. **Small, Focused Agents** - Build modular, single-purpose agents
11. **Trigger from Anywhere** - Enable flexible invocation patterns
12. **Make Your Agent a Stateless Reducer** - Design for predictability and testability

## Why It's Cool

Unlike frameworks that promote "autonomous agent" patterns with a prompt and bag of tools looping until a goal is reached, 12-Factor Agents recognizes that good agents are "comprised of mostly just software." This pragmatic approach helps developers avoid common pitfalls and build AI features that actually work reliably in production.

The methodology recommends taking small, modular concepts from agent building and incorporating them into existing products rather than pursuing greenfield rewrites with heavy frameworks.

## Getting Started

Visit the GitHub repository to read the full guide:

```bash
git clone https://github.com/humanlayer/12-factor-agents.git
```

The repository contains detailed explanations of each principle with practical examples and code patterns.
