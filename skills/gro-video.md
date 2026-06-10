---
name: gro-video
description: Generate a video ad using the Gro AI ad engine. Takes 2–10 minutes. Requires a product with an image.
---

# Generate Video Ad with Gro

Generate a short-form video ad for a product.

## How to use

Invoke with: `/gro:video`

**Note:** Video generation takes 2–10 minutes. Claude will show progress while it renders.

## Steps Claude will follow

1. Call `list_products` to show available products (video requires a product image)
2. Ask which product and describe the video concept
3. Ask for duration preference: 4, 6, or 8 seconds — default: 6
4. Call `generate_video_ad` with product_id, concept, and duration
5. Wait for generation — Claude will show progress notifications
6. Present the video URL

## MCP setup

Same as `/gro:image` — see that skill for setup instructions.
