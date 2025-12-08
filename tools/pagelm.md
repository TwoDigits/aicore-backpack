# PageLM

> An open-source AI-powered education platform that transforms study materials into interactive learning experiences - a NotebookLM alternative.

- **URL**: https://github.com/CaviraOSS/PageLM
- **GitHub**: https://github.com/CaviraOSS/PageLM
- **License**: CaviraOSS Community License (free for personal/educational use)
- **Category**: Open Source Alternatives

## Description

PageLM is an open-source platform that converts study materials into interactive learning resources. Inspired by Google's NotebookLM, it provides a self-hosted alternative with support for multiple LLM providers including Gemini, GPT, Claude, Grok, Ollama, and OpenRouter.

The platform supports various document formats (PDF, DOCX, Markdown, TXT) and transforms them into engaging learning tools like flashcards, quizzes, AI podcasts, and Cornell-style notes.

## Key Features

- **Contextual Chat**: Q&A with your documents using RAG
- **SmartNotes**: Automated Cornell-style note generation
- **Flashcards**: Spaced repetition learning system
- **Interactive Quizzes**: AI-generated quizzes with hints and scoring
- **AI Podcast**: Generate audio podcasts from your notes
- **Voice Transcription**: Transcribe lectures and audio content
- **Homework Planner**: AI-assisted homework planning
- **ExamLab**: Exam simulation and practice
- **Debate Practice**: Practice debates with AI opponents
- **Study Companion**: Personal AI study assistant

## Why It's Cool

PageLM offers a fully self-hosted alternative to NotebookLM with remarkable flexibility:

- **Multi-provider support**: Use any LLM provider (OpenAI, Anthropic, Google, local Ollama models)
- **Privacy-focused**: Run entirely on your own infrastructure
- **Comprehensive learning toolkit**: Goes beyond NotebookLM with features like flashcards, quizzes, and exam simulation
- **Modern stack**: Built with TypeScript, React, LangChain, and Langraph
- **Docker-ready**: Easy deployment with Docker Compose

## Getting Started

**Requirements**: Node.js v21.18+, npm/pnpm, ffmpeg

**Quick Start:**
```bash
git clone https://github.com/caviraOSS/pagelm.git
cd pagelm
./setup.sh  # Linux
# or
./setup.ps1  # Windows
```

Access the application at `http://localhost:5173`

**Docker Deployment:**
```bash
docker compose up --build
```

Configure your preferred LLM provider (Gemini, GPT, Claude, Ollama, etc.) through the settings.
