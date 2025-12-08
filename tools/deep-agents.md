# Deep Agents

> Open-source agent framework with planning capabilities, filesystem access, and sub-agent delegation for complex workflows.

- **URL**: https://github.com/langchain-ai/deepagents
- **GitHub**: https://github.com/langchain-ai/deepagents
- **License**: MIT
- **Category**: Agent Frameworks

## Description

Deep Agents is an open-source agent framework built on LangChain and LangGraph that equips AI agents with planning capabilities, filesystem access, and the ability to spawn specialized sub-agents for handling intricate agentic workflows. It implements patterns used by advanced systems like Claude Code and Manus, enabling agents to manage complex, multi-step tasks through planning, computational resource access, and task delegation.

## Key Features

- **Built-in Planning Tool** - Task decomposition for complex multi-step workflows
- **Filesystem Backend** - Multiple storage options (ephemeral, persistent, hybrid)
- **Sub-agent Delegation** - Spawn specialized sub-agents with isolated execution contexts
- **Human-in-the-Loop** - Workflow support via interrupts for human oversight
- **Long-term Memory** - Persistent memory across conversations
- **Pre-built Middleware** - Todos, filesystem operations, and summarization out of the box
- **Prompt Caching** - Optimization for Anthropic models
- **MCP Integration** - Model Context Protocol tool integration

## Why It's Cool

Deep Agents addresses real challenges in long-horizon agent tasks by reducing costs and improving reliability. Built by LangChain, it provides a battle-tested harness implementing production patterns from systems like Claude Code. The middleware architecture and sub-agent delegation make it highly extensible for domain-specific use cases while maintaining the reliability needed for complex autonomous workflows.

## Getting Started

```bash
# Install with pip
pip install deepagents

# Optional: Add Tavily for web search capability
pip install tavily-python
```

Configure your API keys and start building agents with planning and delegation capabilities. Check the [GitHub repository](https://github.com/langchain-ai/deepagents) for full documentation and examples.
