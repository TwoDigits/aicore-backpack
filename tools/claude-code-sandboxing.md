# Claude Code Sandboxing

> Built-in filesystem and network isolation for safer AI agent execution in Claude Code.

- **URL**: https://code.claude.com/docs/en/sandboxing
- **License**: Proprietary (part of Claude Code)
- **Category**: Claude Code

## Description

Claude Code Sandboxing provides OS-level isolation to protect your system during autonomous AI-assisted development. Rather than requiring permission approvals for each bash command, sandboxing establishes security boundaries upfront, allowing Claude to work more autonomously while maintaining protection against malicious actions.

The feature uses platform-native sandboxing technologies: **bubblewrap** on Linux and **Seatbelt** on macOS. All child processes inherit these restrictions, ensuring subprocesses cannot bypass security boundaries.

## Key Features

- **Filesystem Isolation**: Restricts file access to specified directories (default: read/write to current working directory, read-only elsewhere)
- **Network Isolation**: Proxy server controls outbound connections, only allowing approved domains
- **OS-Level Enforcement**: Uses bubblewrap (Linux) or Seatbelt (macOS) for robust protection
- **Two Sandbox Modes**: Auto-allow mode for autonomous execution, or regular permissions mode for more control
- **Prompt Injection Protection**: Prevents unauthorized file modifications and network access from malicious prompts
- **Data Exfiltration Prevention**: Blocks unauthorized network connections to prevent data theft

## Why It's Cool

Sandboxing addresses a critical concern with AI agents: how do you give them the autonomy to be productive while preventing damage from mistakes, hallucinations, or prompt injection attacks? Claude Code's sandboxing provides a practical answer by establishing clear boundaries upfront. This means:

- You can let Claude execute bash commands automatically without constant approval prompts
- Malicious dependencies or compromised scripts can't exfiltrate data or modify system files
- Even if a prompt injection attack occurs, the damage is contained within the sandbox
- All boundary violations trigger immediate notifications, keeping you informed and in control

## Getting Started

Sandboxing is configured through Claude Code's `settings.json`. Key configuration options:

1. **Sandbox Modes**:
   - **Auto-Allow Mode**: Sandboxed bash commands execute automatically
   - **Regular Permissions Mode**: All commands go through standard permission flows

2. **Domain Permissions**: Network access is granted per-domain during use, and permissions become permanent once approved

3. **Command Exclusions**: Use `excludedCommands` to force specific commands (like `watchman`) to execute outside the sandbox

## Important Limitations

- Network sandboxing doesn't inspect traffic content - ensure only trusted domains are permitted
- Overly broad filesystem permissions can create vulnerabilities
- Linux's nested sandbox mode for Docker environments provides weaker security
- Unix socket access can potentially be exploited for privilege escalation
