# Berrys AI — MCP Server

**Your agent turns product photos into on-brand listing images, ads, and short videos on one canvas.**

Berrys connects to the AI agent you already use: Claude, Claude Code, ChatGPT, Codex, Cursor, Gemini CLI, or VS Code. You plan the work with your agent. Berrys builds it on your visual canvas and runs the generation, with your credits and your approval.

## What it does

- **Listing production** — one product photo becomes hero, lifestyle, and detail shots for your storefront.
- **Campaign rollouts** — hand over a brief; your agent plans the shot list, generates coordinated image sets and copy variants on a shared canvas.
- **Short product videos** — storyboard a multi-shot clip and keep the product identical across cuts: the last frame of one shot seeds the next.
- **Live review** — the agent shares a canvas link after each step so you can edit, undo, or restore.

## Connect

The server is remote (Streamable HTTP + OAuth). There are no keys to copy — you sign in to Berrys in the browser on first connect.

**Server URL:** `https://app.berrys.io/api/mcp`

| Client | How to add |
|---|---|
| **Claude (web/desktop)** | Settings → Connectors → Add custom connector → paste the URL |
| **Claude Code** | `claude mcp add --transport http berrys https://app.berrys.io/api/mcp` |
| **ChatGPT** | Settings → Apps & Connectors → Advanced → Developer mode → Create connector with the URL |
| **Codex** | `codex mcp add berrys --url https://app.berrys.io/api/mcp` then `codex mcp login berrys` |
| **Cursor** | Add `.mcp.json` from this repo (or paste the URL in MCP settings) |
| **VS Code** | Add the `mcpServers` entry from `.mcp.json` |
| **Gemini CLI** | `gemini mcp add --transport http berrys https://app.berrys.io/api/mcp` |

First check (free): ask your agent **"List my Berrys projects."**

## Repo layout

| Path | Purpose |
|---|---|
| `.mcp.json` | MCP server descriptor (auto-detected by Cursor Directory and Open Plugins clients) |
| `skills/berrys/SKILL.md` | Agent skill — how agents should drive Berrys (quotes, approvals, canvas workflows) |
| `rules/berrys.mdc` | Cursor rule for a consistent agent experience |

## Spending credits

Building and browsing are free. Only generation spends Berrys credits. The agent shows an itemized quote first and waits for your explicit confirmation before submitting a charge.

## Documentation

- Setup guides for every client: [berrys.io/plugins](https://berrys.io/plugins)
- User guide: [app.berrys.io](https://app.berrys.io)
- Registry listing: `io.github.GeneralBerrys/berrys-canvas` on the [Official MCP Registry](https://registry.modelcontextprotocol.io)
