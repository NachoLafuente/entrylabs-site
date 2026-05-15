# Enricher · Agent 02

> /find anyone, from Slack.

Type `/find Sarah at Acme` in any channel. The agent checks your Attio, then waterfalls Prospeo + BetterContact + LinkedIn. Phone, email, role back in your channel within seconds.

- [Book a session](/book)
- **€2k deploy + €350/mo all-inclusive**

## What it does for the funnel

- **Waterfalls, not single-shot** — Attio first (instant, free), then Prospeo for email, BetterContact for phone, LinkedIn for role. Claude picks each step.
- **Lives in your Slack** — No new tab, no new dashboard. Type /find anywhere your reps already work. Result comes back in the same thread.
- **Capped budget per workspace** — Daily budget cap per Slack workspace, 5-turn cap per query. Predictable cost.
- **Confidence on every field** — Email at 0.93. Phone at 0.88. LinkedIn at 0.95. Reps see the score before they trust the result.

## A find is a decision, not a query

1. Rep types `/find Sarah at Acme` in any Slack channel. Slack POSTs to the agent endpoint inside your VPC.
2. Enricher checks Attio first — your CRM is the cheapest, fastest, and most accurate source. If it's there, we're done.
3. If not, Claude picks the next step: Prospeo for email, BetterContact for phone, LinkedIn lookup for role and seniority. Each call carries a confidence — Claude stops when it has enough.
4. Result replies in-thread with every field, every source, every confidence. Reps decide whether to write it back to Attio with one click.

```
 /find Sarah at Acme
   │
   ▼
 ┌──────────────────┐
 │   ENRICHER       │
 │   ▸ attio        │
 │   ▸ prospeo      │
 │   ▸ bettercontact│
 │   ▸ linkedin     │
 │   ▸ rank · gate  │
 └──────────────────┘
   │
   ▼
 ┌──────────────────┐
 │   SLACK REPLY    │
 │   sarah@acme.io  │
 │   +1 415 555-…   │
 │   VP Sales · 6y  │
 │   confidence ok  │
 └──────────────────┘
```

## The specification, plainly

- **Surface** — Slack `/find` command — works in any channel, any thread
- **Sources** — Attio (first) · Prospeo · BetterContact · LinkedIn
- **Logic** — Claude tool-use waterfall — stops at first sufficient answer
- **Latency** — ~5–10s per lookup, including waterfall steps
- **Cost** — €350/mo all-inclusive · €300/mo BYOK Anthropic · €2k one-time deploy
- **Quota** — ~100 lookups/mo included · €0.04/lookup beyond
- **Caps** — 5-turn cap per query · per-workspace daily budget cap
- **Write-back** — One-click write to Attio (record matched or new)
- **Data** — EU-hosted (Hetzner Falkenstein). Per-client VPS + Postgres.

## The other two agents

- [Autofill](/agents/autofill) — fills your fields
- [Signals](/agents/signals) — watches your accounts

## See it on your accounts

- [Book the session](/book)
- Talk to a founder: nacho@5050growth.com
