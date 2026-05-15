# Autofill · Agent 01

> Sales call → CRM fields, automatically.

Every meeting ends with the CRM record already complete. Trained on your last 90 days of calls so it knows your vocabulary from day one.

- [Book a session](/book)
- **€2k deploy + €300/mo all-inclusive**

## What it does for the funnel

- **Reads every meeting tool** — Granola, Fathom, Gong, Otter, Fireflies. We hook the webhook your team already uses.
- **Writes back to your CRM** — Attio first-class. HubSpot, Salesforce, Pipedrive on request. Idempotency keys mean replays never duplicate.
- **Confidence, not guesses** — Every field carries a 0–1 confidence and a citation to the call. Below 0.9 and we suppress.
- **€300/mo, all-inclusive** — Anthropic, Hetzner, Neon, support — one invoice. BYOK Anthropic and save €50/mo.

## A field is more than a string

1. Rep finishes a call. Notes land in Granola, Fathom, Gong, Otter, or Fireflies. Attio's webhook fires the moment the note attaches to a company or deal.
2. Autofill reads the note and pulls per-company RAG — your last 90 days of calls — so it extracts in your team's vocabulary, not a generic schema.
3. Claude extracts your methodology fields. MEDDIC, SPIN, BANT, or whatever you call them. Each value carries a 0–1 confidence and a citation back to the call.
4. Fields land in Attio with idempotency keys. End-to-end p95 under 30 seconds. Day-15 correction call locks the prompt to your business; monthly reviews keep it sharp.

```
call ends
   │
   ▼
 ┌──────────────────┐
 │   AUTOFILL       │
 │   ▸ read note    │
 │   ▸ rag context  │
 │   ▸ extract      │
 │   ▸ score        │
 │   ▸ gate ≥ 0.9   │
 │   ▸ write attio  │
 └──────────────────┘
         │
         ▼
   24+ fields
   cited to call
   replayable
```

## The specification, plainly

- **Input** — Granola, Fathom, Gong, Otter, Fireflies (one or all)
- **Output** — MEDDIC, SPIN, BANT, or custom — your methodology, your field names
- **Latency** — < 30s p95 (call note in → fields written)
- **Accuracy** — Confidence-gated — only ≥ 0.9 writes to your CRM
- **Cost** — €300/mo all-inclusive · €250/mo BYOK Anthropic · €2k one-time deploy
- **Writes to** — Attio (native) · HubSpot · Salesforce · Pipedrive · Postgres
- **HITL** — First 200 writes gated for review; configurable thereafter
- **Backfill** — 90 days of prior calls processed on day one
- **Data** — EU-hosted (Hetzner Falkenstein). Per-client VPS + Postgres. Never trained on.
- **Ops** — Day-1 glossary call · Day-15 correction call · Monthly review

## The other two agents

- [Enricher](/agents/enricher) — answers in Slack
- [Signals](/agents/signals) — watches your accounts

## See it on your accounts

60-minute working session. We'll walk through your CRM and your meeting-tool stack, tell you which agent fits, and quote a fixed price before you log off.

- [Book the session](/book)
- Talk to a founder: nacho@5050growth.com
