# LM Studio

> Desktop application for running large language models locally with OpenAI-compatible API and developer SDKs.

- **URL**: https://lmstudio.ai/
- **GitHub**: https://github.com/lmstudio-ai
- **License**: Free for home and work use
- **Category**: Local & Self-Hosted AI

## Description

LM Studio is a desktop application that enables users to download and run open-source large language models locally on their computers. It provides a user-friendly interface for model discovery, download, and execution without requiring internet connectivity or cloud dependencies. The platform supports models like Qwen3, Gemma3, DeepSeek, and many others from the open-source community.

## Key Features

- **Cross-Platform Support**: Available for macOS, Windows, and Linux
- **OpenAI-Compatible API**: Drop-in replacement for OpenAI API endpoints, enabling seamless integration with existing tools
- **Developer SDKs**: JavaScript (`@lmstudio/sdk`) and Python (`lmstudio`) SDKs for programmatic integration
- **MCP Client**: Built-in Model Context Protocol client functionality for AI assistant integrations
- **Apple MLX Support**: Optimized model support for Apple Silicon via MLX
- **CLI Tool**: Command-line interface (`lms`) for automation and scripting
- **LM Studio Hub**: Integrated model discovery and download from community repositories

## Why It's Cool

LM Studio bridges the gap between local LLM execution and developer workflows. The OpenAI-compatible API means you can prototype with local models and switch to cloud services (or vice versa) without changing your code. This is particularly valuable for:

- **Privacy-sensitive development**: Keep your code and data completely local
- **Cost reduction**: No API fees during development and testing
- **Offline development**: Work without internet connectivity
- **Model experimentation**: Easily try different open-source models

## Getting Started

1. Download LM Studio from [lmstudio.ai/download](https://lmstudio.ai/download) (current version: 0.3.33)

2. Launch the application and browse models in the LM Studio Hub

3. Download a model and start the local server

4. For SDK integration:
   ```bash
   # JavaScript
   npm install @lmstudio/sdk

   # Python
   pip install lmstudio
   ```

5. Use the OpenAI-compatible endpoint at `http://localhost:1234/v1` with any OpenAI client library
