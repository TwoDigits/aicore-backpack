# Ollama

> Get up and running with large language models locally with a simple CLI and API.

- **URL**: https://ollama.com
- **GitHub**: https://github.com/ollama/ollama
- **License**: MIT
- **Category**: Local & Self-Hosted AI

## Description

Ollama is a streamlined tool for downloading, running, and managing large language models on your local machine. Written in Go, it provides a simple command-line interface and REST API that makes running models like Llama, Gemma, DeepSeek, and many others as easy as a single command. With 157k+ GitHub stars, it has become the de facto standard for local LLM deployment.

The platform handles all the complexity of model management, quantization, and inference optimization, allowing developers to focus on building applications rather than wrestling with model deployment.

## Key Features

- **Extensive Model Library**: Access to models ranging from 1B to 671B parameters including Llama 3.2, Gemma 3, DeepSeek-R1, Mistral, and many more
- **Simple CLI**: Run any model with `ollama run <model-name>`
- **REST API**: OpenAI-compatible API for easy integration with existing tools
- **Multimodal Support**: Vision models for processing both text and images (Llama 3.2 Vision)
- **Embeddings**: Generate vector embeddings for RAG and semantic search applications
- **Custom Models**: Create custom models using Modelfiles with system prompts and parameters
- **Cross-Platform**: Native support for macOS, Windows, and Linux
- **Docker Support**: Official Docker images for containerized deployment
- **GGUF/Safetensors**: Import models from various formats

## Why It's Cool

Ollama democratizes access to powerful language models by making local deployment trivially easy. No GPU cluster, no cloud bills, no data leaving your machine. For AI-powered development:

- **Privacy**: Keep your code and prompts completely local
- **Zero Latency Concerns**: No network round-trips to cloud APIs
- **Cost-Free Experimentation**: Try different models without API costs
- **Offline Development**: Work on AI features without internet connectivity
- **80+ Integrations**: Massive ecosystem including Open WebUI, Continue, LangChain, and more

## Getting Started

### Installation

**macOS:**
```bash
brew install ollama
```

**Linux:**
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

**Windows:**
Download from [ollama.com/download](https://ollama.com/download)

### Quick Start

```bash
# Run a model (downloads automatically if not present)
ollama run llama3.2

# Run with a specific prompt
ollama run llama3.2 "Explain recursion in one sentence"

# List available models
ollama list

# Pull a model without running
ollama pull codellama
```

### API Usage

```bash
# Start the server (runs automatically on install)
ollama serve

# Chat completion
curl http://localhost:11434/api/chat -d '{
  "model": "llama3.2",
  "messages": [{"role": "user", "content": "Hello!"}]
}'
```

### Python Integration

```python
import ollama

response = ollama.chat(model='llama3.2', messages=[
    {'role': 'user', 'content': 'Why is the sky blue?'}
])
print(response['message']['content'])
```

For more details, see the [official documentation](https://github.com/ollama/ollama/blob/main/README.md).
