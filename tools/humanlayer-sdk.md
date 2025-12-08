# HumanLayer SDK

> API and SDK that enables AI agents to contact humans for feedback, input, and approvals with guaranteed human oversight.

- **URL**: https://www.humanlayer.dev/
- **GitHub**: https://github.com/humanlayer/humanlayer
- **License**: Apache 2.0
- **Category**: Agent Frameworks

## Description

HumanLayer is an API and SDK that enables AI agents to communicate with humans in tool-based and async workflows. It guarantees human oversight of high-stakes function calls with approval workflows across Slack, email, Discord, and more.

The problem it solves: high-stakes functions are the most valuable and promise the most impact in automating workflows, but "90% accuracy" is not acceptable for these operations. HumanLayer provides deterministic guarantees for human oversight, even if the LLM makes mistakes or hallucinates.

## Key Features

- **Require Human Approval**: The `@hl.require_approval()` decorator blocks specific function calls until a human approves
- **Human as Tool**: Generic `hl.human_as_tool()` allows AI to contact humans for answers, advice, or feedback
- **OmniChannel Contact**: Reach humans across Slack, Email, SMS, Discord, and more
- **Granular Routing**: Route approvals to specific teams or individuals
- **Framework Agnostic**: Works with any LLM (OpenAI, Claude, Llama) and frameworks (LangChain, CrewAI, etc.)
- **Multi-Language Support**: SDKs available for Python and TypeScript/JavaScript

## Why It's Cool

HumanLayer emerged from a real problem: the founders tried to build an AI system to manage SQL databases (including removing unused tables), but realized granting unsupervised control to AI could result in unintended data deletions. Instead of avoiding automation, they built HumanLayer to enable powerful AI capabilities with appropriate human oversight.

This is the missing piece for deploying AI agents in production environments where mistakes have real consequences.

## Getting Started

### Python

```bash
pip install humanlayer
```

```python
from humanlayer import HumanLayer

hl = HumanLayer()

@hl.require_approval()
def delete_database_table(table_name: str):
    # This will require human approval before executing
    db.drop_table(table_name)

# Or use human as a tool for feedback
human_tool = hl.human_as_tool()
```

### TypeScript

```bash
npm install humanlayer
```

See the [GitHub repository](https://github.com/humanlayer/humanlayer) for full documentation and examples.
