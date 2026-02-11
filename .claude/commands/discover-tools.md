---
description: Discover new AI tools, frameworks, and resources via parallel research agents
---

You are a discovery coordinator for the AICore Backpack curated list. Your job is to find new, interesting AI development tools, frameworks, methodologies, and resources that are NOT yet in the list — and present them to the user for review.

## Phase 1: Understand What We Already Have

1. **Read README.md** to extract:
   - All existing categories with their descriptions
   - Every tool/resource already listed (names and URLs)
   - This is your **exclusion list** — never suggest something already present

2. Build a mental inventory of the current coverage so agents can focus on gaps and new developments.

## Phase 2: Launch Parallel Research Agents

Launch **at least 6 sub-agents in parallel** using the Task tool (subagent_type: "general-purpose"). Each agent focuses on a different research angle. Give every agent the full exclusion list of existing tools so they don't suggest duplicates.

**Important rules for every agent prompt:**
- Include the complete list of already-known tools/URLs so the agent skips them
- Instruct agents to use WebSearch extensively
- Agents should find tools that appeared or gained traction recently (last ~3 months)
- Each agent must return a structured list (see format below)
- Agents should verify that tools actually exist (check GitHub stars, website accessibility)
- Focus on quality over quantity — only suggest genuinely interesting finds

### Agent Assignments

1. **Agent "AI IDEs & Coding Agents"** — Search for new AI-powered IDEs, coding agents, code editors, CLI tools for autonomous coding, and agentic development environments. Include new major features/releases of existing tools that we don't track yet.

2. **Agent "Agent Frameworks & Infrastructure"** — Search for new agent frameworks, multi-agent orchestration libraries, agent memory systems, tool-use frameworks, and agent infrastructure. Cover LangChain ecosystem, CrewAI alternatives, and emerging players.

3. **Agent "MCP & Integrations"** — Search for new MCP servers, notable MCP integrations, and protocol-level tooling for AI assistants. Also cover new API integrations and developer tool connectors.

4. **Agent "Methodologies & Best Practices"** — Search for new AI-assisted development methodologies, prompt engineering techniques, workflow patterns, research papers on AI productivity, and notable blog posts or talks about AI in software engineering.

5. **Agent "Open Source & Local AI"** — Search for new open-source AI tools, self-hosted LLM solutions, privacy-focused alternatives, open-weight models with developer tooling, and inference engines.

6. **Agent "Claude Code & GitHub Copilot Ecosystem"** — Search for new plugins, extensions, skills, commands, and community tools specifically for Claude Code and GitHub Copilot. Include new official features and notable community contributions.

7. **Agent "Observability, Testing & DevOps"** — Search for new AI observability tools, LLM testing frameworks, AI-powered CI/CD, code review bots, and AI DevOps tooling.

8. **Agent "Trending & Viral"** — Search broadly for AI developer tools that are currently trending on Hacker News, Product Hunt, GitHub Trending, Reddit r/programming and r/MachineLearning, and X/Twitter dev communities. Cast a wide net for things the other agents might miss.

### Required Output Format for Each Agent

Instruct each agent to return results in this format:

```
## Discoveries

### [Tool Name]
- **URL**: [primary url]
- **GitHub**: [if available, with star count]
- **What it does**: [2-3 sentence description]
- **Why it's interesting**: [1-2 sentences on why this deserves a spot]
- **Suggested category**: [best fitting category from our list]
- **Confidence**: [HIGH / MEDIUM / LOW — how confident the agent is this is genuinely new and noteworthy]
```

## Phase 3: Collect and Curate Results

After all agents return:

1. **Deduplicate** — Remove any tools suggested by multiple agents (keep the best description)
2. **Filter out already-listed tools** — Double-check against the exclusion list
3. **Sort by confidence** — HIGH first, then MEDIUM, then LOW
4. **Group by category** — Organize findings by their suggested category

## Phase 4: Present Summary to User

Present a concise, scannable summary grouped by category. For each discovery:

```
### [Category Name]

1. **[Tool Name]** — [One-line description]
   [URL] | [GitHub stars if available]
   *Why it's cool: [brief reason]*

2. ...
```

At the end, use **AskUserQuestion** with multiSelect to let the user pick which tools to add:
- List the top discoveries (up to ~15-20 most interesting ones)
- Let the user select multiple
- Include a "None of these" option

## Phase 5: Add Selected Tools

For each tool the user selects:
- Use the `/add-tool` skill with the tool's URL to properly add it to the repository
- This ensures consistent documentation and formatting

## Important Notes

- **Recency bias**: Prefer tools from the last 3 months, but don't exclude older gems that are still under the radar
- **Quality bar**: This is a curated list for experienced developers — skip beginner tutorials, trivial wrappers, and unmaintained repos (< 50 GitHub stars unless genuinely innovative)
- **No duplicates**: The most important rule — never suggest a tool we already have
- **Verify existence**: Agents should confirm tools are real and active, not vaporware
- **Be opinionated**: It's better to surface 10 great finds than 50 mediocre ones
