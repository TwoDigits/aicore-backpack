# Tomcat AI-Enabled

> Apache Tomcat 12.0 transformed into an AI-First development proof of concept, demonstrating how to make 726K+ LOC codebases navigable for AI agents.

- **URL**: https://github.com/thorstenmaier/tomcat-ai-enabled
- **GitHub**: https://github.com/thorstenmaier/tomcat-ai-enabled
- **License**: Apache-2.0
- **Category**: Experimental & Research

## Description

Tomcat AI-Enabled is Apache Tomcat 12.0 augmented with AI-first infrastructure. It addresses the fundamental constraint that even advanced AI models can only hold about 1% of a large codebase in their working memory. The project demonstrates practical patterns for making enterprise-scale codebases navigable and maintainable by AI agents.

## Key Features

- **CLAUDE.md Entry Point**: Specialized entry point providing essential commands, architecture overview, and dynamic loading instructions—keeping AI agents oriented without overwhelming context windows
- **Dynamic Context Loading**: Hierarchical documentation with on-demand loading across 10 specialized domains, service interactions, patterns, and semantic navigation maps
- **Sub-Agent Orchestration**: Specialized agents for focused tasks including research-context-optimizer, test-orchestrator, dependency-analyzer, and code-validator
- **Persistent Knowledge Management**: Every AI session contributes to a growing knowledge base via the `/improve-yourself` command
- **MCP Server Integration**: Access to 31,279 Tomcat documentation snippets via Model Context Protocol
- **Foundation-First Documentation Integrity**: Bottom-up approach where truth flows from implementation to abstraction, with `/sync-comments` ensuring inline comments match actual code

## Why It's Cool

This project solves real problems that developers face when using AI with large codebases:

1. **Context Window Limits**: Shows practical solutions for AI agents working with code 100x larger than their context capacity
2. **Documentation Decay**: Demonstrates automated verification to maintain accurate, trustworthy documentation
3. **Architectural Governance**: "Architecture as Code, Living in Code"—architectural decisions versioned with implementation and continuously validated
4. **Enterprise Scale**: Patterns applicable to Fortune 500 codebases where knowledge silos create business risks
5. **Collaborative AI**: Treats AI as an intelligent assistant for navigating complexity rather than a developer replacement

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/thorstenmaier/tomcat-ai-enabled.git
   ```

2. The AI-specific infrastructure lives in `/.claude/` directory with:
   - Custom commands for common workflows
   - Sub-agent definitions for specialized tasks
   - MCP server configuration in `.mcp.json`

3. Start with `CLAUDE.md` as the primary entry point for AI agents to understand the codebase structure and available commands.
