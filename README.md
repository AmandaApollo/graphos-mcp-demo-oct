# October MCP Builder Series Demo Code
This repo contains code demoed at mcp server builder meetups in Oct 2025 in SF and NYC.

It contains the following files:
CLAUDE.md - this provides the steps for the agent to follow for building with [Connectors](https://www.apollographql.com/docs/graphos/connectors) for REST APIs and GraphOS MCP tools.  Agents are constantly evolving and may behave differently when provided markdown instructions.  This md file can be modified for your use case and agent behavior. 

[Space Devs](https://thespacedevs.com/llapi) Open API spec and [aviation weather](https://aviationweather.gov/data/api/) Open API spec - these open api specs can be used with the prompts below. You do not have to use these and can replace with your own prompts and specs.  Providing API endpoints or json response examples is also supported by the GraphOS MCP tools

## Add GraphOS MCP Tools

[GraphOS MCP Tools](https://www.apollographql.com/docs/graphos/platform/graphos-mcp-tools) provide your agent with tools to rapidly generate graphs and orchestrate APIs. To add these tools to Claude Code, run the following command:

`claude mcp add --transport http graphos-mcp-tools https://mcp.apollographql.com`

Restart your Claude code session before continuing

## Generating connectors and running an Apollo MCP Server with Claude Code

The prompts below are similar to what was shown in the live demos.  Please adjust for your needs and add more specificity as required.

1. Prompt:  I just started a new graph with Apollo, I’m providing the endpoint for the Space Devs Launch Library at LaunchLibrary API v2.3.0 (v2.3.0).json in the local folder.
I want to get the details with fields for launches.
2. Ask Claude to run the project locally for you, then test your queries
3. Prompt: Add weather on the pad type. use the aviationweather.yaml file in this workspace
4. Prompt: can you start this project locally with an Apollo MCP Server?

## Get in touch

Subscribe to our [Luma Calendar](https://luma.com/mcp-server?k=c&utm_source=github) to keep up with all our in person and virtual MCP Builder Events

YouTube playlist for demo sessions showing the above flow from October - Coming Soon

If you have any questions or feedback, please open an issue on this repo or reach out to [Amanda Martin](https://www.linkedin.com/in/amandamartin-dev) or Michael Watson
