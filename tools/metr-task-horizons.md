# METR Task Horizons

> Research measuring how long AI agents can autonomously complete tasks, with open-source evaluation infrastructure.

- **URL**: https://metr.org/blog/2025-03-19-measuring-ai-ability-to-complete-long-tasks/
- **Paper**: https://arxiv.org/abs/2503.14499
- **GitHub**: https://github.com/METR/vivaria (evaluation infrastructure)
- **Analysis Code**: https://github.com/METR/eval-analysis-public
- **License**: Open source
- **Category**: Experimental & Research

## Description

METR's research introduces a metric called "time horizon" - the length of tasks (measured in human expert completion time) that AI models can successfully complete with a given probability. This provides a more intuitive measure of AI capability than traditional benchmarks, helping developers understand what AI agents can realistically accomplish.

The research evaluates 30+ frontier AI models across software development, reasoning, and multi-step problems, tracking how task completion capabilities have evolved over time.

## Key Features

- **Time Horizon Metric**: Measures AI capability in human-interpretable terms (minutes/hours of work)
- **Interactive Visualization**: Compare 30+ AI models with confidence intervals on linear/logarithmic scales
- **Trend Analysis**: Shows task completion length has doubled approximately every 7 months
- **Vivaria**: Open-source evaluation infrastructure for running agent evaluations
- **Robustness Testing**: Analyses across task subsets and methodologies

## Key Findings

- Best models (like Claude 3.7 Sonnet) reliably complete tasks up to ~1 hour in length
- Task completion capability has been doubling every ~7 months over 6 years
- If trends continue, frontier AI could handle week-long tasks within 2-4 years
- Success rates of 50% vs 80% show different capability profiles

## Why It's Cool

This research bridges the gap between impressive benchmark scores (where AI often exceeds human performance) and practical automation potential. For developers, it provides:

- Realistic expectations for what AI agents can handle autonomously
- A framework for planning which tasks to delegate to AI
- Forecasting for future AI capability growth
- Open-source infrastructure to run your own evaluations

## Getting Started

### Explore the Research
1. Read the [blog post](https://metr.org/blog/2025-03-19-measuring-ai-ability-to-complete-long-tasks/) with interactive visualizations
2. Dive into the [full paper on arXiv](https://arxiv.org/abs/2503.14499) for methodology details

### Use the Evaluation Infrastructure
```bash
# Clone Vivaria - METR's open-source evaluation platform
git clone https://github.com/METR/vivaria

# For analysis code and raw data
git clone https://github.com/METR/eval-analysis-public
```

Vivaria provides the infrastructure to run agent evaluations on tasks and measure time-horizon capabilities for your own models or agents.
