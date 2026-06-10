---
name: gro-copy
description: Generate ad copy variations (headline + primary text) for a product using Gro's AI copy engine.
---

# Generate Ad Copy with Gro

Generate Facebook/Meta ad copy variations for a product.

## How to use

Invoke with: `/gro:copy`

## Steps Claude will follow

1. Call `list_products` to show available products
2. Ask which product and the core concept or angle (e.g. "pain-point focused", "social proof", "urgency")
3. Ask how many variations (1–5) — default: 3
4. Call `generate_ad_copy` with product_id, concept, and num_variations
5. Present the variations in a clear format with headline and primary text for each

## MCP setup

Same as `/gro:image` — see that skill for setup instructions.
