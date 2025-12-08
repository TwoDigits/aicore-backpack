# Claude Code Plugins

> Official plugin system for extending Claude Code with shareable commands, agents, skills, hooks, and MCP servers.

- **URL**: https://code.claude.com/docs/en/plugins
- **GitHub**: N/A (Official Anthropic documentation)
- **License**: N/A
- **Category**: Claude Code

## Description

Claude Code Plugins is the official extension system that allows developers to extend Claude Code with custom functionality. Plugins can include commands, specialized agents, skills (autonomous agent capabilities), hooks (event handlers), and MCP server integrations. The system supports both installation from plugin marketplaces and custom plugin development, enabling teams to share and standardize their AI-assisted development workflows.

## Key Features

- **Commands**: Custom slash commands in markdown format that extend Claude Code's capabilities
- **Agents**: Specialized agent definitions for domain-specific tasks
- **Skills**: Autonomous capabilities that Claude invokes based on task context
- **Hooks**: Event handlers for workflow automation triggered by Claude Code events
- **MCP Servers**: External tool integrations through the Model Context Protocol
- **Plugin Marketplaces**: Discovery and distribution through curated plugin catalogs
- **Team Sharing**: Repository-level plugin configurations for consistent team tooling

## Why It's Cool

The plugin system transforms Claude Code from a standalone tool into an extensible platform. Teams can create standardized workflows, share best practices through plugins, and automate repetitive tasks. The marketplace approach enables community-driven innovation while maintaining quality through curation. For organizations, repository-level plugin specifications ensure everyone uses the same tooling automatically.

## Getting Started

**Installing Plugins:**
```bash
# Interactive discovery
/plugin

# Direct installation
/plugin install plugin-name@organization
```

**Creating Plugins:**
1. Set up a marketplace structure
2. Create `.claude-plugin/plugin.json` manifest
3. Add commands in `commands/` directory
4. Test locally before distribution

**Team Distribution:**
Configure `.claude/settings.json` at repository level for automatic team-wide installation.
