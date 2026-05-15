# Entry Labs

> Deploy three GTM agents inside the CRM your team already uses.

Entry Labs builds, deploys, and operates outbound agents — **Autofill**, **Enricher**, and **Signals** — inside your Attio, HubSpot, or Salesforce workspace. EU-hosted, one invoice, seven days to live in production.

- [Book a session](/book)
- [See the catalog](#catalog)

## Three agents, one catalog

### 01 · Autofill · €2k deploy + €300/mo

Autofill fills your CRM fields. A perfect Attio record from every sales call. Reads Granola, Fathom, Gong, Otter, Fireflies. Writes back your MEDDIC, SPIN, or custom fields — only above 90% confidence, every value cited.

- [See Autofill](/agents/autofill)

### 02 · Enricher · €2k deploy + €350/mo

Enricher answers in Slack. Type `/find Sarah at Acme` in any channel. The agent checks your Attio, then waterfalls Prospeo + BetterContact + LinkedIn. Phone, email, role back in seconds.

- [See Enricher](/agents/enricher)

### 03 · Signals · €2k deploy + €400/mo

Signals catches the moment. Watches 30+ event classes — funding, hiring, exec, product, stack — across your top 100 accounts. Claude ranks each against your ICP. Daily 9am Slack digest, top signals written back to the lead record.

- [See Signals](/agents/signals)

## Use your CRM like it's an agent

The CRM is the surface. The agent is the engine. Entry Labs treats every account as a long-running task — reading sources, ranking values, writing the cell.

- **READS** — meeting notes, Slack, webhooks
- **ENRICHES** — firmographics, stack, hiring, funding, ICP
- **LISTENS** — sub-30s extraction, 24/7
- **WRITES** — idempotent, cited, confidence-gated
- **TRACES** — every decision logged, every run replayable
- **LEARNS** — monthly correction calls, prompt overlay

## How we ship

- **7 days** — kickoff to production
- **< 30s** — p95 extraction SLA
- **1 invoice** — infra, LLM, and support bundled
- **EU-hosted** — per-client VPS + Postgres

## Any source. Any agent. All in your CRM.

One invoice, seven days to live. Every agent runs on EU-hosted infrastructure inside your VPC.

### Sources

- Granola — transcripts
- Fathom — transcripts
- Gong — transcripts + signals
- Slack — `/find`, webhooks
- PredictLeads — 30+ event classes

### Agents

- 01 · Autofill — fills CRM fields
- 02 · Enricher — answers in Slack
- 03 · Signals — ranks daily

### Destinations

- Attio — native, first-class
- HubSpot — via Composio
- Salesforce — via Composio
- Slack — 9am digest, `/replies`

## CLI, Slack, webhook, YAML — the surface you already use

Four ways to talk to every agent. Pick the one your team already lives in.

### CLI · Operator

```
$ 5050 deploy --client acme --agent autofill
▸ provisioning Hetzner cx23 (Falkenstein)…
▸ neon-postgres org_id resolved
▸ cloudflare tunnel acme.entry-labs.dev → live
▸ litellm proxy boot                ✓
▸ autofill agent                    ✓ healthy
deployed in 13m 41s · /runs/r-2204
```

### Slack · Reps

```
priya /find Sarah Chen at Acme

entrylabs
▸ search_attio  → no match
▸ prospeo       → sarah@acme.io · 0.93
▸ bettercontact → +1 415 555-0182 · 0.88
▸ linkedin      → VP Sales · 6y @ Acme

✓ Sarah Chen · VP Sales · sarah@acme.io
```

### Webhooks · Inbound

```
POST https://acme.entry-labs.dev/hooks/granola
x-signature: t=1747312…
content-type: application/json
{ "call_id": "call_8821", "company": "Acme · Q2 discovery" }

↓ within 30s p95
200 OK · 24 fields written · idempotency_key=…
```

### YAML · Founder-tunable

```
name: acme-autofill
methodology: meddic
fields:
  - stage:       # short text · ≥0.92
  - pain:        # long text · ≥0.88
  - budget:      # number EUR · ≥0.90
  - timeline:    # date span · ≥0.85
hitl:
  first_n: 200   # gated review window
  after:   auto  # or: queue · surface
```

## Need a 4th agent built?

Custom builds are €5–15k depending on scope. Same productized model — deployed, operated, on EU infrastructure. 60-minute scoping call to find out.

- [Book the session](/book)
- [Vote on agent #4](/poll)

---

Keyboard: `A` Autofill · `E` Enricher · `S` Signals · `B` Book · `H` Home · `G` Game · `T` Toggle this · `?` Cheat-sheet

Operated by [5050Growth](https://5050growth.com) · Attio Partner · Berlin
