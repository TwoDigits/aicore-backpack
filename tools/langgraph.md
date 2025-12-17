# LangGraph

> Open-source framework for building stateful, multi-actor AI agent applications with cyclic workflows and human-in-the-loop support.

- **URL**: https://www.langchain.com/langgraph
- **GitHub**: https://github.com/langchain-ai/langgraph
- **License**: MIT
- **Category**: Agent Frameworks

## Description

LangGraph is an MIT-licensed open-source framework from LangChain for building agentic AI applications. It provides low-level control over agent workflows while maintaining reliability for production environments. Unlike traditional DAG-based systems, LangGraph supports cycles, which is essential for agentic behaviors where agents need to loop through reasoning steps.

## Key Features

- **Stateful Graph Architecture**: Define agent workflows as graphs where nodes represent computation steps (LLM calls, tool executions) and edges define flow between nodes with conditional routing
- **Cycles Support**: Full support for cyclic workflows, enabling iterative reasoning patterns like ReAct
- **Human-in-the-Loop**: Built-in statefulness for human-agent collaboration - agents can write drafts, await approval, and operators can inspect and "time-travel" to correct course
- **First-Class Streaming**: Native token-by-token and intermediate step streaming for real-time visibility into agent reasoning
- **Persistence & Memory**: Built-in memory stores maintain conversation histories and context across sessions
- **Multi-Agent Support**: Build single-agent, multi-agent, and hierarchical systems with customizable workflows
- **Moderation & Control**: Easy-to-add quality checks and moderation loops to prevent agents from deviating

## Why It's Cool

LangGraph provides the low-level primitives needed for production-grade agent systems without black-box constraints. It's designed for complex task automation beyond simple scenarios - handling long-running research jobs, multi-step background tasks, and guest-facing AI solutions requiring granular control. The framework adds no performance overhead and integrates seamlessly with LangChain's ecosystem.

## Getting Started

```bash
pip install langgraph
```

```python
from langgraph.graph import StateGraph, END

# Define your state
class AgentState(TypedDict):
    messages: list

# Create a graph
workflow = StateGraph(AgentState)

# Add nodes and edges
workflow.add_node("agent", call_agent)
workflow.add_node("tools", call_tools)
workflow.add_edge("agent", "tools")
workflow.add_conditional_edges("tools", should_continue)

# Compile and run
app = workflow.compile()
```

## Deployment Options

- **Fully Managed Cloud**: Deploy via LangSmith
- **Hybrid**: SaaS control plane with self-hosted data plane
- **Self-Hosted**: Complete self-hosted infrastructure
