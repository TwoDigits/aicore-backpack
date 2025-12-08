# Context7

> MCP server that delivers up-to-date, version-specific documentation and code examples directly into LLM prompts.

- **URL**: https://context7.com
- **GitHub**: https://github.com/upstash/context7
- **License**: MIT
- **Category**: MCP Servers & Integrations

## Description

Context7 is an MCP (Model Context Protocol) server by Upstash that solves a common problem with AI coding assistants: outdated or hallucinated API references. LLMs typically rely on training data that can be months or years old, leading to code suggestions that reference deprecated APIs or features that don't exist.

Context7 pulls live, version-specific documentation and code examples directly from source repositories, ensuring your AI assistant provides accurate, current information for the libraries you're using.

## Key Features

- **Live documentation**: Fetches current documentation directly from library sources
- **Version-specific examples**: Get code examples that match your actual library version
- **Eliminates hallucinations**: No more AI-generated APIs that don't exist
- **Wide MCP client support**: Works with Cursor, Claude Code, VS Code, Windsurf, Zed, Cline, and more
- **Extensive library coverage**: Indexes popular libraries including React, Next.js, and many others
- **Multi-language docs**: Documentation available in 15+ languages

## Why It's Cool

Context7 addresses one of the most frustrating aspects of AI-assisted coding: when the AI confidently suggests code using APIs that don't exist or are outdated. With 38.8k GitHub stars, it's become an essential tool for developers who want their AI assistant to give accurate, up-to-date coding advice. Just add "use context7" to your prompt and get documentation that actually matches the library version you're using.

## Getting Started

### Claude Code

```bash
claude mcp add --transport http context7 https://mcp.context7.com/mcp
```

### Cursor / VS Code / Windsurf

Add to your MCP configuration:

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp@latest"]
    }
  }
}
```

### Usage

Simply add "use context7" to any prompt where you need accurate library documentation:

```
Create a Next.js middleware that checks for a valid JWT in cookies
and redirects unauthenticated users to /login. use context7
```

### Requirements

- Node.js >= v18.0.0
- MCP-compatible client
- Optional: Context7 API key for higher rate limits (get one at context7.com/dashboard)
