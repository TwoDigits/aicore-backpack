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

3. **Read the current README.md** to get the actual category list, their slugs, and their descriptions. Do not use a hardcoded list — the categories and descriptions in the README are the source of truth.

4. **Categorize the tool**:
   - Analyze which category fits best based on the category descriptions in the README
   - If no category is a good fit, use AskUserQuestion to:
     - Propose a new category OR
     - Let the user choose from existing categories OR
     - Let the user provide a custom category name
   - If multiple categories could fit, ask the user to choose

5. **Apply the category lens** — take the category description you read from the README in step 3 and use it as the editorial lens for everything you write. The description defines what readers in that section care about. Concretely:
   - **Description**: lead with the capability the category description highlights most, not just what the tool does in general
   - **Key Features**: order and frame features so the ones that map to the category description come first; skip or deprioritise features that are tangential to it
   - **Why It's Cool**: make the argument anchored to the category. Ask "why does this matter *for someone browsing this specific section*?" and answer that
   - **README entry** (one-liner): the short description should land on the same emphasis — a reader should be able to tell from the entry alone why it belongs in this category

6. **Create a tool documentation file** in `tools/[tool-name].md` with this structure, written through the category lens from step 5:
   ```markdown
   # [Tool Name]

   > [Short one-line description — should reflect the category lens]

   - **URL**: [main url]
   - **GitHub**: [github url if available]
   - **License**: [license if known]
   - **Category**: [category name]

   ## Description

   [Detailed description, leading with what the category lens says matters most]

   ## Key Features

   - [Feature 1 — order and frame features around what the category lens highlights]
   - [Feature 2]
   - ...

   ## Why It's Cool

   [Why this tool is interesting — anchored to the category lens. E.g. for AI IDEs & Editors, center the argument on autonomous coding capabilities]

   ## Getting Started

   [Brief installation or usage instructions if available]
   ```

7. **Update the README.md**:
   - Find the correct category section (between `<!-- TOOLS:[category] -->` and `<!-- /TOOLS:[category] -->`)
   - Add a new entry in this format (the short description should also reflect the category lens):
     ```markdown
     - **[Tool Name](tools/[tool-name].md)** - [Short description] ([Website]([url]))
     ```
   - If creating a new category, add the new section in alphabetical order with proper HTML comments

8. **Confirm completion** by showing:
   - Tool name and category
   - Link to the created documentation file
   - The entry added to README.md

## Important Notes

- Use kebab-case for tool file names (e.g., `my-cool-tool.md`)
- Keep descriptions concise but informative
- Always verify the URL is accessible before proceeding
- If the URL is not reachable or doesn't contain useful information, inform the user
