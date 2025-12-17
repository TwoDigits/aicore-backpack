# CrewAI

> Multi-agent platform for building, deploying, and managing collaborative AI agent workflows.

- **URL**: https://www.crewai.com/
- **GitHub**: https://github.com/crewAIInc/crewAI
- **License**: MIT
- **Category**: Agent Frameworks

## Description

CrewAI is a multi-agent platform that enables building, deploying, and managing AI agent workflows. It provides both a Python framework for developers and a no-code UI Studio for creating multi-agent automations. The platform allows agents to collaborate on complex tasks with role-based specialization, making it ideal for orchestrating intelligent workflows.

## Key Features

- **Role-Based Agent Design**: Define agents with specific roles, goals, and backstories for specialized task execution
- **Flexible Orchestration**: Sequential, hierarchical, or custom process flows for agent collaboration
- **Framework + UI Studio**: Code from scratch or use no-code templates
- **Deployment Options**: Cloud, self-hosted, or local environments
- **Any LLM Support**: Works with OpenAI, Anthropic, local models, and more
- **Human-in-the-Loop**: Built-in feedback mechanisms and approval workflows
- **Performance Monitoring**: Track crew performance, progress, and ROI
- **Auto-Generated UI**: Deployed crews get automatic user interfaces

## Why It's Cool

CrewAI makes multi-agent orchestration accessible with its role-playing approach - each agent has a defined role, goal, and backstory that shapes its behavior. With 40K+ GitHub stars and adoption by 60% of Fortune 500 companies, it's become a go-to framework for production multi-agent systems. The combination of code-first framework and no-code studio means both developers and non-technical users can build agent workflows.

## Getting Started

```bash
pip install crewai crewai-tools
```

```python
from crewai import Agent, Task, Crew

# Create agents with roles
researcher = Agent(
    role="Senior Research Analyst",
    goal="Uncover cutting-edge developments in AI",
    backstory="You're a seasoned researcher with a keen eye for emerging trends."
)

writer = Agent(
    role="Tech Content Writer",
    goal="Create engaging content about AI discoveries",
    backstory="You're a skilled writer who makes complex topics accessible."
)

# Define tasks
research_task = Task(
    description="Research the latest AI agent frameworks",
    agent=researcher
)

write_task = Task(
    description="Write a blog post about the findings",
    agent=writer
)

# Create and run crew
crew = Crew(agents=[researcher, writer], tasks=[research_task, write_task])
result = crew.kickoff()
```
