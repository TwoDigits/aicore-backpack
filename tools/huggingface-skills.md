# Hugging Face Skills

> Packaged instruction sets that empower coding agents to manage LLM fine-tuning through natural language commands.

- **URL**: https://huggingface.co/blog/hf-skills-training
- **GitHub**: https://github.com/huggingface-skills/hf-llm-trainer
- **License**: Apache 2.0
- **Category**: Claude Code

## Description

Hugging Face Skills is a framework that enables coding agents (Claude Code, OpenAI Codex, Google Gemini CLI) to handle the complete lifecycle of language model fine-tuning through conversational commands. Instead of writing training scripts or managing infrastructure, developers can simply describe what they want to train in natural language.

The flagship `hf-llm-trainer` skill handles everything from dataset validation to GPU selection, training execution, and model deployment - all through your IDE's AI assistant.

## Key Features

- **Natural Language Training**: Submit fine-tuning jobs by describing what you want (e.g., "Fine-tune Qwen3-0.6B on the codeforces dataset")
- **Multiple Training Methods**: Supports SFT (Supervised Fine-Tuning), DPO (Direct Preference Optimization), and GRPO (Group Relative Policy Optimization)
- **Automatic Hardware Selection**: Intelligently picks GPUs from t4-small to a100-large based on model size
- **Cost Transparency**: Provides hardware cost estimates before committing to training
- **Dataset Validation**: Validates formats before training to prevent expensive failed runs
- **Real-time Monitoring**: Trackio integration for visualizing training metrics
- **Model Export**: Automatic push to Hugging Face Hub and GGUF conversion for local deployment
- **Async Execution**: Jobs run in the background so you can continue working

## Why It's Cool

This tool democratizes LLM fine-tuning by removing the infrastructure expertise barrier. Instead of wrestling with CUDA configurations, training scripts, and cloud GPU management, you can customize models through a conversation with your coding agent. The built-in safety checks (dataset validation, cost estimates) prevent costly mistakes, while the async nature keeps you productive. It's particularly powerful for developers who want to create domain-specific models without becoming ML infrastructure experts.

## Getting Started

**Installation varies by coding agent:**

```bash
# Claude Code
/plugin install hf-llm-trainer@huggingface-skills

# Gemini CLI
gemini extensions install huggingface-skills/hf-llm-trainer

# Codex
# Loads automatically via AGENTS.md file in your repo
```

**Authentication:**
```bash
hf auth login
# Use a write-access token
```

**Example Usage:**
Simply tell your coding agent what you want to train:
```
Fine-tune Qwen3-0.6B on the open-r1/codeforces-cots dataset using SFT
```

The agent will:
1. Validate your configuration and dataset
2. Show hardware selection and cost estimate
3. Submit the job after your approval
4. Provide a monitoring link for real-time progress
