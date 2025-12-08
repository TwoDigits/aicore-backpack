# Kiro Powers

> Dynamic MCP tool bundles with framework expertise that activate contextually in AI-assisted development.

- **URL**: https://kiro.dev/blog/introducing-powers/
- **GitHub**: N/A (proprietary feature)
- **License**: Proprietary (part of Kiro IDE)
- **Category**: MCP Servers & Integrations

## Description

Kiro Powers is a feature within Kiro's agentic IDE that bundles MCP (Model Context Protocol) tools with framework expertise, enabling dynamic context loading for AI agents. Instead of loading all tools upfront and consuming valuable context window space, powers activate contextually based on what you're working on - mentioning "database" triggers the Neon power while deployment discussions activate Netlify.

Powers address "context rot" - the problem of overwhelming tool definitions consuming your context window before you even start working.

## Key Features

- **Dynamic MCP Tool Loading**: Tools load only when relevant, keeping baseline context usage minimal
- **One-Click Installation**: Browse and install powers directly from the IDE or kiro.dev website without JSON configuration
- **Contextual Activation**: Powers activate automatically based on keywords and current tasks
- **Partner Ecosystem**: Launch partners include Stripe, Supabase, Figma, Neon, Netlify, and Postman
- **Community Powers**: Support for GitHub URL imports for community-built tools and private repositories
- **Cross-Compatibility (Planned)**: Future support for Cursor, Claude Code, and Cline

## Power Structure

A power consists of:
- **POWER.md**: Entry point document defining available MCP tools and activation keywords
- **MCP server configuration**: Tool definitions and connection details
- **Workflow-specific steering**: Context files loaded on-demand based on current tasks

## Why It's Cool

Powers solve a real problem with MCP adoption - having too many tools configured means burning context on tool definitions before you even start working. By loading expertise dynamically, you can have access to dozens of frameworks and services without the context overhead. The partner ecosystem (Stripe, Supabase, Figma) means high-quality integrations out of the box, and the planned cross-IDE compatibility could make this a universal standard for MCP tool distribution.

## Getting Started

1. Download and install [Kiro IDE](https://kiro.dev)
2. Browse available powers in the IDE or at kiro.dev
3. Click to install - API keys are prompted on first use
4. Start working - powers activate automatically based on context

For community powers, you can import directly from GitHub URLs.
