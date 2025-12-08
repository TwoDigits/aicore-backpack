---
description: Add a new AI tool to the curated list by analyzing a URL
argument-hint: [url]
---

You are adding a new AI development tool to the AICore Backpack curated list.

## Your Task

1. **Fetch and analyze the URL**: $ARGUMENTS
   - Use WebFetch to retrieve information about the tool
   - If needed, use WebSearch to find additional information (GitHub stats, reviews, documentation)

2. **Extract tool information**:
   - Tool name
   - Short description (1-2 sentences)
   - What it does and its main features
   - Installation/usage instructions (if available)
   - GitHub URL (if applicable)
   - License (if applicable)
   - Why it's interesting/cool for developers

3. **Read the current README.md** to see existing categories:
   - code-assistants: Code Assistants & Extensions
   - local-ai: Local & Self-Hosted AI
   - mcp: MCP Servers & Integrations
   - prompt-engineering: Prompt Engineering & Management
   - code-review: Code Review & Testing
   - documentation: Documentation & Knowledge
   - devops: DevOps & Automation
   - security: Security & Analysis
   - open-source: Open Source Alternatives
   - experimental: Experimental & Research

4. **Categorize the tool**:
   - Analyze which category fits best
   - If no category is a good fit, use AskUserQuestion to:
     - Propose a new category OR
     - Let the user choose from existing categories OR
     - Let the user provide a custom category name
   - If multiple categories could fit, ask the user to choose

5. **Create a tool documentation file** in `tools/[tool-name].md` with this structure:
   ```markdown
   # [Tool Name]

   > [Short one-line description]

   - **URL**: [main url]
   - **GitHub**: [github url if available]
   - **License**: [license if known]
   - **Category**: [category name]

   ## Description

   [Detailed description of what the tool does]

   ## Key Features

   - [Feature 1]
   - [Feature 2]
   - ...

   ## Why It's Cool

   [Why this tool is interesting for AI-powered development]

   ## Getting Started

   [Brief installation or usage instructions if available]
   ```

6. **Update the README.md**:
   - Find the correct category section (between `<!-- TOOLS:[category] -->` and `<!-- /TOOLS:[category] -->`)
   - Add a new entry in this format:
     ```markdown
     - **[Tool Name](tools/[tool-name].md)** - [Short description] ([Website]([url]))
     ```
   - If creating a new category, add the new section in alphabetical order with proper HTML comments

7. **Confirm completion** by showing:
   - Tool name and category
   - Link to the created documentation file
   - The entry added to README.md

## Important Notes

- Use kebab-case for tool file names (e.g., `my-cool-tool.md`)
- Keep descriptions concise but informative
- Always verify the URL is accessible before proceeding
- If the URL is not reachable or doesn't contain useful information, inform the user
