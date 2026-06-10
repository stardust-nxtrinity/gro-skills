---
name: gro-launch
description: Launch a generated ad creative to Meta Ads as a live campaign using the Gro ad engine.
---

# Launch Ad to Meta with Gro

Launch a generated creative as a live Meta ad campaign.

## Prerequisites

- Your Meta Ads account must be connected in Gro (visit https://gro.app to connect)
- You need a generated creative URL (from `/gro:image` or `/gro:video`)

## How to use

Invoke with: `/gro:launch`

## Steps Claude will follow

1. Ask for the creative URL (from a previous `/gro:image` or `/gro:video` generation)
2. Ask for the Meta ad account ID (format: `act_XXXXXXXXX`)
3. Ask for: headline, primary text, destination URL, daily budget (in your account currency), objective
4. Call `launch_ad` with all parameters
5. Present the campaign ID, ad IDs, and Ads Manager link

## Objectives

- `OUTCOME_SALES` — optimise for purchases (default)
- `OUTCOME_LEADS` — optimise for lead form fills
- `OUTCOME_TRAFFIC` — optimise for link clicks
- `OUTCOME_AWARENESS` — optimise for reach/impressions

## MCP setup

Same as `/gro:image` — see that skill for setup instructions.
