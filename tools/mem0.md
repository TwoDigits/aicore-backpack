# Mem0

> Intelligent memory layer that enables AI agents and assistants to remember user preferences and learn continuously over time.

- **URL**: https://mem0.ai
- **GitHub**: https://github.com/mem0ai/mem0
- **License**: Apache 2.0
- **Category**: Agent Frameworks

## Description

Mem0 (pronounced "mem-zero") is a universal memory layer designed to enhance AI assistants and agents with personalized, persistent memory. It enables AI systems to remember user preferences, adapt to individual needs, and continuously improve through learning. The system works by retrieving relevant stored memories based on user queries, injecting them into LLM context before generating responses, and automatically creating new memories from conversations.

Mem0 offers both a managed hosted platform and self-hosted open-source options, making it flexible for different deployment needs. It integrates seamlessly with existing LLMs (defaulting to OpenAI's gpt-4.1-nano but supporting various alternatives) and popular agent frameworks like LangGraph and CrewAI.

## Key Features

- **Multi-Level Memory**: Retains User, Session, and Agent state with adaptive personalization
- **Cross-Platform SDKs**: Available for Python and Node.js with intuitive APIs
- **Performance Optimized**: 91% faster responses than full-context approaches
- **Token Efficient**: 90% lower token usage compared to including full context
- **Accuracy**: +26% accuracy over OpenAI Memory on the LOCOMO benchmark
- **Flexible Deployment**: Choose between managed service or self-hosted with custom vector stores
- **Framework Integrations**: Works with LangGraph, CrewAI, and other popular agent frameworks

## Why It's Cool

Mem0 solves one of the fundamental challenges in AI agent development: persistent, personalized memory. Instead of agents starting fresh with each conversation or requiring full context to be passed every time, Mem0 provides an intelligent memory layer that recalls relevant information automatically. The performance gains (91% faster, 90% fewer tokens) make it practical for production use, and the peer-reviewed research backing demonstrates measurable improvements over alternatives. For developers building AI agents that need to maintain context across sessions or personalize to individual users, Mem0 provides a battle-tested solution.

## Getting Started

### Python

```bash
pip install mem0ai
```

```python
from mem0 import Memory

# Initialize memory
m = Memory()

# Add memories
m.add("I prefer morning meetings", user_id="alice")

# Search memories
results = m.search("When does the user like to have meetings?", user_id="alice")
```

### Node.js

```bash
npm install mem0ai
```

```javascript
import { Memory } from 'mem0ai';

const m = new Memory();

// Add and search memories
await m.add("I prefer morning meetings", { user_id: "alice" });
const results = await m.search("meeting preferences", { user_id: "alice" });
```

For more details, see the [official documentation](https://docs.mem0.ai/).
