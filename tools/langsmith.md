# LangSmith

> Observability platform for debugging, monitoring, and understanding LLM application behavior.

- **URL**: https://www.langchain.com/langsmith
- **GitHub**: https://github.com/langchain-ai/langsmith-sdk
- **License**: Proprietary (Free tier available)
- **Category**: Observability

## Description

LangSmith is a monitoring and debugging platform from LangChain that provides visibility into agent behavior and LLM application performance. It offers step-by-step tracing of agent execution, live dashboards for business-critical metrics, and automatic clustering of conversations to identify patterns and issues.

## Key Features

- **Step-by-Step Tracing**: Debug non-deterministic LLM behavior with detailed execution traces
- **Live Dashboards**: Track costs, latency, and response quality in real-time
- **Alerting**: Get notified when problems occur in production
- **Insights**: Automatic clustering of similar conversations to understand user needs and systemic issues
- **Framework Agnostic**: Works with any framework, one-line setup for LangChain/LangGraph
- **Zero Latency Impact**: Asynchronous callback handler ensures no performance overhead
- **Flexible Deployment**: Cloud-hosted or self-hosted on Kubernetes (AWS, GCP, Azure)

## Why It's Cool

Debugging LLM applications is notoriously difficult due to their non-deterministic nature. LangSmith solves this by capturing every step of agent execution, making it possible to understand why an agent made certain decisions. The Insights feature is particularly powerful - it automatically groups similar conversations to reveal patterns you wouldn't notice by looking at individual traces. Used by Klarna, GitLab, LinkedIn, and Elastic.

## Getting Started

For LangChain/LangGraph applications, just set one environment variable:

```bash
export LANGCHAIN_TRACING_V2=true
export LANGCHAIN_API_KEY=<your-api-key>
```

For other frameworks, use the SDK:

```bash
pip install langsmith
```

```python
from langsmith import traceable

@traceable
def my_llm_function(input):
    # Your LLM logic here
    return response
```
