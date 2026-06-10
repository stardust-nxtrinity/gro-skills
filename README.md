# gro-skills

Claude Code skills for [Gro](https://gro.app) — the AI ad agent.

Connect Gro to Claude Code and generate, refine, and launch ads directly from your terminal.

## Install

```bash
npx skills add stardust-nxtrinity/gro-skills
```

## Setup

Add the Gro MCP server to your Claude Code `.claude/settings.json`:

```json
{
  "mcpServers": {
    "gro": {
      "url": "https://api.gro.app/api/v1/mcp/public"
    }
  }
}
```

On first connection, Gro opens a browser window to authenticate. No API key needed.

For programmatic/B2B access, generate an API key in [Gro Settings → API Keys](https://gro.app) and add it:

```json
{
  "mcpServers": {
    "gro": {
      "url": "https://api.gro.app/api/v1/mcp/public",
      "headers": { "Authorization": "Bearer gro_your_api_key_here" }
    }
  }
}
```

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| Generate image ad | `/gro:image` | Generate image creatives (30–90s) |
| Generate video ad | `/gro:video` | Generate video creatives (2–10 min) |
| Generate ad copy | `/gro:copy` | Generate headline + primary text variations |
| Launch ad | `/gro:launch` | Launch creative to Meta Ads as a live campaign |

## Requirements

- [Claude Code](https://claude.ai/code) installed
- A [Gro account](https://gro.app) (free to start)
- For launching ads: Meta Ads account connected in Gro

## About Gro

Gro is an AI ad agent that handles the full Create→Launch loop. Connect tracking tools, ad platforms, and automation systems to Gro via MCP.
