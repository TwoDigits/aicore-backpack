# OpenClaw

> Open-source personal AI assistant that runs locally and automates tasks across email, calendars, smart home, and 50+ integrations via chat platforms.

- **URL**: https://openclaw.ai/
- **GitHub**: https://github.com/openclaw/openclaw
- **License**: MIT
- **Category**: Personal AI Assistants

## Description

OpenClaw is a local-first personal AI assistant that connects to your chat platforms — WhatsApp, Telegram, Discord, Slack, Signal, or iMessage — and autonomously handles everyday tasks. It clears inboxes, manages calendars, handles flight check-ins, browses websites, fills forms, controls smart home devices, and executes shell commands. All data stays on your machine, and the assistant maintains persistent memory across conversations, learning your preferences over time.

## Key Features

- **Chat-native interface**: Operates through WhatsApp, Telegram, Discord, Slack, Signal, or iMessage — no separate app needed
- **Persistent memory**: Maintains context across conversations, building a personalized "second brain" of preferences and patterns
- **50+ integrations**: Gmail, GitHub, Spotify, Obsidian, Twitter, Hue smart lights, calendars, and more
- **Self-extending skills**: Can autonomously write, test, and deploy new plugins based on conversational requests
- **Local-first & private**: Runs on your hardware (Mac, Windows, Linux); data never leaves your machine
- **Model flexibility**: Works with Claude, GPT, or local models
- **Community skill hub**: ClawHub marketplace for sharing and discovering community-built skills
- **Companion app**: macOS menubar application (beta) for quick access

## Why It's Cool

With 184k GitHub stars, OpenClaw has become one of the most popular open-source AI projects. It represents a fundamental shift from cloud-dependent AI assistants (Siri, Alexa, Google Assistant) to a fully hackable, privacy-respecting alternative that runs on your own hardware. The self-extending skill system is particularly compelling — ask it to integrate with a new service and it writes the plugin itself. Built by Peter Steinberger and an active community, it's the kind of tool where developers quickly go from "let me try this" to running it 24/7 with access to their entire digital life.

## Getting Started

One-liner install (recommended):

```bash
curl -fsSL https://openclaw.ai/install.sh | bash
```

Or via npm:

```bash
npm i -g openclaw
openclaw onboard
```

Or clone from GitHub for source-level customization:

```bash
git clone https://github.com/openclaw/openclaw.git
cd openclaw
pnpm install
```

Requires Node.js 22+. The onboarding wizard walks you through connecting your first chat platform and configuring your AI model (Claude, GPT, or local).
