# AIHackr MCP

Read public webpages as Markdown or HTML, discover links, extract structured JSON, and run bounded crawls from your AI client.

## Connect with OAuth

1. Add `https://aihackr.com/mcp` as a remote MCP server using **Streamable HTTP**.
2. Choose **OAuth** if prompted. Sign in to AIHackr with your email and review the permissions before authorizing the connection.
3. Once connected, try the example below. You can revoke the connection from [Connected apps](https://aihackr.com/connections).

If your client uses bearer authentication, create an API key in the [AIHackr dashboard](https://aihackr.com/dashboard) and set `Authorization: Bearer YOUR_AIHACKR_API_KEY` using the client's secure credential settings.

## Client setup

- **ChatGPT** · Add AIHackr as a custom MCP server with OAuth if your workspace supports custom MCP connections. [MCP setup guide](https://aihackr.com/docs/mcp)
- **Claude** · In Customize → Connectors, add a custom connector named AIHackr and paste the endpoint.
- **Cursor** · Add the configuration below to your MCP settings.
- **Gemini CLI** · Run `gemini extensions install https://github.com/biserd/aihackr-mcp`, then use `/mcp auth aihackr` in Gemini CLI to connect your account.
- **VS Code** · [Install AIHackr in VS Code](https://vscode.dev/redirect?url=vscode%3Amcp%2Finstall%3F%257B%2522name%2522%253A%2522aihackr%2522%252C%2522type%2522%253A%2522http%2522%252C%2522url%2522%253A%2522https%253A%252F%252Faihackr.com%252Fmcp%2522%257D), or run **MCP: Add Server**, choose **HTTP**, and enter the endpoint. Then start the server from **MCP: List Servers** and follow the sign-in prompt.

```json
{
  "mcpServers": {
    "aihackr": {
      "url": "https://aihackr.com/mcp"
    }
  }
}
```

## Try one page

> Use AIHackr to read https://fixtures.aihackr.com/ as Markdown. Return the page heading and source URL. Use one page.

The expected heading is “Native engine fixture.” A successful Markdown scrape uses one credit.

## Plans and credits

Verified accounts receive **1,200 free credits per UTC calendar month**. The playground, REST API, and MCP use the same workspace balance.

| Plan | USD per month | Credits per month |
| --- | ---: | ---: |
| Starter | $7 | 3,000 |
| Builder | $15 | 7,500 |
| Scale | $29 | 20,000 |

A successful scrape or link map uses one credit. Structured extraction uses five credits. A crawl reserves its requested page limit, charges one credit for each successful page with retained content, and releases unused credits when the job ends. [Current plans](https://aihackr.com/plans) · [Usage and limits](https://aihackr.com/docs/limits)

[MCP documentation](https://aihackr.com/docs/mcp) · [Privacy](https://aihackr.com/privacy) · [Support](https://aihackr.com/support)

This repository contains the install configuration and listing manifest. The server implementation is in the [AIHackr repository](https://github.com/biserd/AI-Hackr).
