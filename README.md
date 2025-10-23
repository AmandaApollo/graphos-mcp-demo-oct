# October MCP Builder Series Demo Code
This repo contains code demoed at mcp server builder meetups in Oct 2025 in SF and NYC. The demo you saw may have included the [flightradar API](https://fr24api.flightradar24.com/) .  This API requires a paid subscription to use so has been replaced with a free API that is similar in nature.

Explanation of files:
CLAUDE.md - this provides the steps for the agent to follow for building with [Connectors](https://www.apollographql.com/docs/graphos/connectors) for REST APIs and GraphOS MCP tools.  Agents are constantly evolving and may behave differently when provided markdown instructions.  This md file can be modified for your use case and agent behavior. 

[Space Devs](https://thespacedevs.com/llapi) Open API spec
[aviation weather](https://aviationweather.gov/data/api/) Open API spec - use this only if you are utilizing the flight radar API. This API only returns US based locations and does not have full coverage for the space devs data.  For spacedevs, open weather API is a better choice.

mcp-config.yaml - when you run prompt 4 below, it will use this file as your base mcp configuration.  To see all configuration options, please check out the [mcp config docs](https://www.apollographql.com/docs/apollo-mcp-server/config-file) You can modify the prompt or claude.md file further if you would like claude code to generate this file for you.

## Add GraphOS MCP Tools

[GraphOS MCP Tools](https://www.apollographql.com/docs/graphos/platform/graphos-mcp-tools) provide your agent with tools to rapidly generate graphs and orchestrate APIs. To add these tools to Claude Code, run the following command:

`claude mcp add --transport http graphos-mcp-tools https://mcp.apollographql.com`

Restart your Claude code session before continuing

## Generating connectors and running an Apollo MCP Server with Claude Code

The prompts below are similar to what was shown in the live demos.  Please adjust for your needs and add more specificity as required.

If you choose to use the [Open Weather API](https://openweathermap.org/current), while free - it does require a signup and API key. 

1. Prompt:  I just started a new graph with Apollo, I’m providing the endpoint for the Space Devs Launch Library at LaunchLibrary API v2.3.0 (v2.3.0).json in the local folder.
I want to get the only the important details with fields for launches. Pad information must be included with lat/long values.
2. Ask Claude to run the project locally for you, then test your queries
3. Prompt:  Add a field-level conector on Pad.weather. use the open weather endpoint and the OPEN_WEATHER_KEY in the env file to research and understand this API https://api.openweathermap.org/data/2.5/weather?lat={lat}&lon={lon}&appid={API key} 
4. Prompt: can you start this project locally with an Apollo MCP Server?

## Get in touch

Subscribe to our [Luma Calendar](https://luma.com/mcp-server?k=c&utm_source=github) to keep up with all our in person and virtual MCP Builder Events

YouTube playlist for demo sessions showing the above flow from October - Coming Soon

If you have any questions or feedback, please open an issue on this repo or reach out to [Amanda Martin](https://www.linkedin.com/in/amandamartin-dev) or Michael Watson
