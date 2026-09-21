---
aliases:
  - ClickUp MCP
tags:
  - roco
  - clickup
  - mcp
type: reference
status: collected
created: 2026-09-18
updated: 2026-09-18
---

# ClickUp MCP Server Reference

## Provenance and purpose

User-supplied documentation captured on 2026-09-18 for the ClickUp project knowledge base and future brainstorming. Setup directions and example actions are reference material, not a request to configure a connection or perform actions. No connection, account or Workspace settings were changed.

The official overview, setup and supported-tools pages were checked on the capture date. Details can change during beta. The source's relative “Updated about 1 month ago” label does not establish an exact publication date.

## Summary of the supplied documentation

- MCP lets external AI assistants interact with ClickUp tasks, Lists, Folders and Docs through natural-language requests.
- The server is described as public beta and available on all plans.
- Endpoint: `https://mcp.clickup.com/mcp`.
- Authentication uses OAuth; personal API keys or existing Auth access tokens are not accepted.
- Uses include task workflows with assignees, priorities and dates; reports and release notes; time entries and timers; questions about tasks, Docs and comments; and comment/chat collaboration.
- The source describes support for major MCP clients and apps. Custom clients must implement JSON-RPC 2.0 over HTTP, OAuth 2.1 with PKCE, and the MCP specification.
- Connected Search cannot search connected apps through this server, according to the supplied FAQ.

## Rate limits recorded from the supplied text

| Workspace setup | Stated limit |
| --- | --- |
| Everything AI add-on purchased | Public API limits for the Workspace plan |
| No Everything AI add-on, Free Forever | 50 calls per rolling 24 hours |
| No Everything AI add-on, Unlimited or above | 300 calls per rolling 24 hours |

The text describes a window beginning with the first request. Its example uses 200 calls on Monday at 13:00 and 100 on Tuesday at 11:00, then blocks further calls until Tuesday at 13:00. Blocked attempts do not extend the window; limits cannot be reset. Fair-use terms apply, and future restrictions or changes may occur. These are recorded documentation values, not measured usage or confirmation of this project's plan/add-on.

## Documentation discrepancy: deletion

The pasted FAQ and live overview say deletion tools have not been added. However, the [supported-tools page](https://developer.clickup.com/docs/mcp-tools), checked on 2026-09-18, explicitly lists a Delete task tool for tasks/subtasks. The documentation is inconsistent. Treat actual deletion support as unresolved until the connected client's available tools and permissions are inspected. Do not assume every client exposes every documented tool.

The supported-tools page also says actions are constrained by the user's ClickUp permissions.

## Sources and setup references

- [Official MCP overview](https://developer.clickup.com/docs/connect-an-ai-assistant-to-clickups-mcp-server)
- [AI assistant setup instructions](https://developer.clickup.com/docs/connect-an-ai-assistant-to-clickups-mcp-server-1)
- [Supported tools and example prompts](https://developer.clickup.com/docs/mcp-tools)
- [Public API rate limits](https://developer.clickup.com/docs/rate-limits)
- [Purchase or remove add-ons](https://help.clickup.com/hc/en-us/articles/6303101719831-Purchase-or-remove-ClickUp-add-ons)
- [AI fair-use terms](https://clickup.com/terms/ai)
- [ClickUp pricing](https://clickup.com/pricing)
- [Official MCP feedback request](https://feedback.clickup.com/public-api/p/clickup-mcp-server-first-party-and-official)

Only the overview, setup and tools pages were fetched for this capture; other links are retained from the supplied documentation.

## Future discussion topics

Possible topics, not approved implementation steps: use MCP to retrieve project context for brainstorming, prepare status reports, or draft task changes for review. Before choosing an integration, identify the intended client, authorized Workspaces, actual tool availability and applicable rate limit.

## Related notes

- [[01 Projects/RocoBroker/ClickUp/ClickUp Tips and Future Ideas]]
- [[01 Projects/RocoBroker/ClickUp/RocoBroker ClickUp Task and Documentation Structure]]
