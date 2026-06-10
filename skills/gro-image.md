---
name: gro-image
description: Generate image ad creatives for a product using the Gro ad engine. Produces square, story, or landscape format ads.
---

# Generate Image Ad with Gro

Generate high-quality ad images for a product using Gro's AI ad generation engine.

## How to use

1. Make sure the `gro` MCP server is connected in your Claude Code settings
2. Invoke this skill with: `/gro:image`

## Steps Claude will follow

1. Call `list_products` to show available products
2. Ask which product and what concept/brief (e.g. "summer sale 20% off")
3. Ask for format preference: square (1:1), story (9:16), or landscape (16:9) — default: square
4. Call `generate_image_ad` with the product_id, concept, and format
5. Wait for generation (30–90 seconds) — progress will show in Claude
6. Present the generated image URLs

## MCP setup

Add to your Claude Code `.claude/settings.json`:
```json
{
  "mcpServers": {
    "gro": {
      "url": "https://api.gro.app/api/v1/mcp/public"
    }
  }
}
```

On first connection, Gro will open a browser window to authenticate your account.
