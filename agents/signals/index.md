# Signals · Agent 03

> Catches the moment to reach out.

Continuous ICP-weighted scoring across funding, hiring, exec, product, and stack events. Daily 9am Slack digest. Top signals written back to the lead's Attio record.

- [Book a session](/book)
- **€2k deploy + €400/mo (100 leads tracked)**

## What it does for the funnel

- **Thirty event classes, watched** — Funding, hiring, exec, product, tech-stack, partnership, M&A, patents, domain change. PredictLeads under the hood; ICP weighting on top.
- **ICP-weighted scoring** — Score = signal × ICP fit. Day-1 glossary call captures your ICP. Weights are versioned; suppression rules are first-class.
- **9am Slack digest, not noise** — Top signals ≥7 arrive every morning with a one-sentence "why this matters for you". Below the threshold, we suppress.
- **Written back to Attio** — Top 5 ranked signals per account land on the company record. Reps see them next time they open the deal — no Slack scrollback.

## A signal is a window, not an alert

1. Day-1 glossary call captures your ICP definition, your buying criteria, your suppression rules. We freeze it into the prompt and version every change.
2. Signals watches PredictLeads + custom sources for the 30+ event classes that matter. Cadence is continuous — events show up within minutes of their public source.
3. Claude scores every event 0–10 against your ICP. Above 7 we raise a hand, with reason and remaining "window of relevance" attached.
4. Top signals land in your 9am Slack digest, ranked by score. The top 5 per account get written back to Attio so reps see them on the record.

```
 events
   │
   ▼
 ┌──────────────────┐
 │   SIGNALS        │
 │   ▸ predictleads │
 │   ▸ score ICP    │
 │   ▸ suppress     │
 │   ▸ rank         │
 │   ▸ window       │
 └──────────────────┘
   │
   ▼
 ┌──────────────────┐
 │   9AM DIGEST     │
 │   acme.io · 91   │
 │   reason: $14M   │
 │   window: 8d     │
 └──────────────────┘
   │
   ▼
   attio company.signals.5
```

## The specification, plainly

- **Watches** — Funding · hiring · exec · stack · product · M&A · patents · domain · 22 more
- **Coverage** — Starter 100 / Growth 300 / Scale 500 leads (€50/mo per +100 beyond)
- **Cadence** — Continuous — sub-30-minute event → trigger
- **Scoring** — Claude scores 0–10 against your ICP · versioned weights
- **Threshold** — Default ≥ 7 surfaces · configurable per motion
- **Surface** — 9am Slack digest + top-5 written to Attio company record
- **Cost** — €400/mo (Starter) · €550/mo (Growth) · €700/mo (Scale) · €2k one-time deploy
- **Sources** — PredictLeads PAYG (included) · custom rules · your own webhooks
- **Data** — EU-hosted (Hetzner Falkenstein). Per-client VPS + Postgres.

## The other two agents

- [Autofill](/agents/autofill) — fills your fields
- [Enricher](/agents/enricher) — answers in Slack

## See it on your accounts

- [Book the session](/book)
- Talk to a founder: nacho@5050growth.com
