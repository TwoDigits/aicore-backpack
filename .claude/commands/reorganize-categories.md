---
description: Analyze and reorganize tool categorizations in the README
---

You are reorganizing the tool categories in AICore Backpack to ensure all tools are optimally categorized.

## Your Task

### 1. Read Current State

First, read the README.md to understand the current structure:
- Identify all categories and their descriptions
- List all tools with their current category assignments

### 2. Read Tool Documentation

For each tool listed in the README, read its documentation from `tools/[tool-name].md` to understand:
- What the tool actually does
- Its key features
- Its primary use case

### 3. Analyze Categorization

For each tool, evaluate if its current category is the best fit by considering:
- Does the tool's primary function match the category description?
- Could another existing category be a better fit?
- Are there tools that would benefit from a new category?
- Are there categories that are too broad or too narrow?

### 4. Present Findings

Create a summary table showing:
```
| Tool | Current Category | Recommended Category | Reason |
|------|------------------|---------------------|--------|
```

Only include tools where you recommend a change or want to discuss the categorization.

### 5. Ask for Confirmation

Use AskUserQuestion to:
- Present tools that might need recategorization
- Let the user approve, reject, or modify each suggestion
- Ask about creating new categories if needed
- Ask about merging similar categories if applicable

### 6. Implement Changes

For approved changes:
1. Update the README.md:
   - Remove the tool entry from its old category section
   - Add the tool entry to its new category section
   - Maintain alphabetical order within categories
2. Update the tool's documentation file:
   - Change the `Category:` field to reflect the new category

### 7. Handle Empty Categories

If a category becomes empty after reorganization:
- Ask the user if they want to:
  - Keep the empty category for future tools
  - Remove the category entirely

### 8. Report Results

After all changes are complete, show:
- Summary of changes made
- New category distribution
- Any categories that remain empty

## Category Reference

Current categories in the README:
- **code-assistants**: IDE extensions, editor plugins, coding enhancements
- **local-ai**: Local/self-hosted AI, privacy-focused alternatives
- **mcp**: Model Context Protocol servers and integrations
- **methodologies**: Structured methodologies and frameworks for AI-assisted development
- **prompt-engineering**: Prompt creation, testing, management, optimization
- **claude-code**: Tools specifically for Claude Code
- **code-review**: AI-powered review, testing, quality assurance
- **documentation**: Docs generation, knowledge management
- **devops**: CI/CD, infrastructure, automation
- **security**: Security scanning, code analysis, vulnerability detection
- **open-source**: Open-source alternatives to commercial tools
- **experimental**: Research projects, cutting-edge experimental tools

## Important Notes

- Keep changes minimal and well-reasoned
- When in doubt, ask the user
- Preserve the original formatting and style of README.md
- Ensure no tools are lost during reorganization
- Maintain alphabetical order within each category section
