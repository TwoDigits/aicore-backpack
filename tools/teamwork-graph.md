# Teamwork Graph

> Atlassian's unified data layer that centralizes teamwork data across applications via GraphQL API for AI-driven insights.

- **URL**: https://developer.atlassian.com/platform/teamwork-graph/
- **Category**: AI Platforms & Hubs

## Description

Teamwork Graph is Atlassian's unified data layer that breaks down data silos by centralizing teamwork data from across multiple Atlassian applications (Jira, Confluence, etc.) and external tools (Google Drive, Slack, Salesforce). It provides a single GraphQL endpoint for querying unified cross-app and cross-tool data, enabling developers to build intelligent, context-aware experiences.

The platform operates in two complementary modes:
1. **Data Access**: Query unified data via the Teamwork Graph API to power intelligent experiences in your apps
2. **Data Ingestion**: Build connectors to bring external tool data into the graph

## Key Features

- **Unified Data Model**: Represents foundational teamwork building blocks across platforms with consistent object types and relationships
- **GraphQL API**: Single endpoint for querying unified data across Atlassian and third-party tools
- **Object Types**: Categorizes data instances with defined properties (Jira issues, Confluence pages, messages, documents)
- **Relationship Mapping**: Maps connections between objects to detect patterns, dependencies, and blockers
- **Custom Connectors**: SDK for building connectors to bring external tool data into the graph
- **AI-Ready Data**: Aggregated information optimized for analytics, reporting, and AI-driven insights

## Why It's Cool

Teamwork Graph solves the fundamental challenge of data fragmentation in modern development workflows. Instead of writing multiple app-specific API integrations, developers can access comprehensive organizational data through a single GraphQL endpoint. This is particularly powerful for:

- **AI-Powered Development Tools**: Build Rovo agents and intelligent assistants that understand the full context of projects, including Jira issues, Confluence docs, Slack conversations, and external tool data
- **Cross-App Insights**: Detect patterns across tools - like finding which documents relate to blocked issues or which team communications are linked to specific projects
- **Smart Recommendations**: Power context-aware features that understand relationships between work items, people, and content

## Getting Started

Teamwork Graph is currently in Early Access Program (EAP). To get started:

1. **Apply for EAP Access**: Contact Atlassian to join the Early Access Program
2. **Explore the API**: Use the GraphQL endpoint to query unified data
3. **Build Connectors**: Use the SDK to bring external tool data into the graph
4. **Example Implementations**: Reference provided examples for Dashboard widgets and Rovo agents

```graphql
# Example: Query related objects across apps
query {
  workItems {
    title
    relatedDocuments {
      name
      lastModified
    }
    linkedMessages {
      content
      author
    }
  }
}
```
