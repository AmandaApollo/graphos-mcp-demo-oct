# graphos-mcp-demo-oct
This repo contains code demoed at mcp server builder meetups in Oct 2025

## Add GraphOS MCP Tools

GraphOS MCP Tools provide your agent with tools to rapidly generate graphs and orchestrate APIs. To add these tools to Claude Code, run the following command:

`claude mcp add --transport http graphos-mcp-tools https://mcp.apollographql.com`

Restart your Claude code session before continuing

## Generating connectors and running an Apollo MCP Server with Claude Code
1. Prompt:  I just started a new graph with Apollo, I’m providing the endpoint for the Space Devs Launch Library at LaunchLibrary API v2.3.0 (v2.3.0).json in the local folder.
I want to get the details with fields for launches.
2. Ask Claude to run the project locally for you, then test your queries
3. Prompt: Add weather on the pad type. use the aviationweather.yaml file in this workspace
4. Prompt: can you start this project locally with an Apollo MCP Server?
