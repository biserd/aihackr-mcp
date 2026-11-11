# AIHackr MCP

Read public webpages as Markdown or HTML, discover links, extract structured JSON, and crawl sites from your AI client.

Connect to `https://aihackr.com/mcp` using Streamable HTTP. Sign in to AIHackr when your client prompts you to authorize the connection. Tool calls use credits from your AIHackr workspace. You can revoke an app's access from [Connections](https://aihackr.com/connections).

- **Claude** · In Customize → Connectors, add a custom connector named AIHackr and paste the endpoint.
- **Cursor** · Add the configuration below to your MCP settings.
- **VS Code** · Run **MCP: Add Server**, choose **HTTP**, and enter the endpoint. Then start the server from **MCP: List Servers** and follow the sign-in prompt.

```json
{
  "mcpServers": {
    "aihackr": {
      "url": "https://aihackr.com/mcp"
    }
  }
}
```

Try asking your client: “Read https://fixtures.aihackr.com and tell me the heading and the JavaScript-rendered marker. Cite the source URL.”

[MCP documentation](https://aihackr.com/docs/mcp) · [Pricing](https://aihackr.com/pricing) · [Privacy](https://aihackr.com/privacy) · [Support](https://aihackr.com/support)

This repository contains the install configuration and listing manifest. The server implementation is in the [AIHackr repository](https://github.com/biserd/AI-Hackr).
