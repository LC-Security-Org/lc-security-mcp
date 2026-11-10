---
name: lc-scam-intelligence
description: Use whenever the person asks about their LC Security data, the scam calls their decoy lines answered, scam campaigns, scammer phone numbers, accounts, URLs or wallets, tactics, alerts, or the blocklist. Always reads the LC Scam Intelligence tools, never general knowledge.
---

# LC Scam Intelligence

LC Scam Intelligence is the customer's own scam-call data from their LC Security dashboard: the scam calls LC's AI decoy phone lines answered and what the scammers revealed. The `lc-scam-intelligence` connector reads the same data as the dashboard, scoped to the person's organisation, and the numbers match the screen. It is separate from any other LC tool.

## How to work

1. If you do not know the organisation, call `list_organisations`. If the account belongs to more than one, pass `org` (the slug) on every call.
2. Pick the tool that matches the question: `get_overview` (Command Center), `list_campaigns` and `get_campaign` (Active Threats), `list_conversations` and `get_conversation`, `list_entities`, `get_entity` and `list_callers`, `list_alerts`, `get_blocklist`, `list_tactics`, `search` for anything by name or number.
3. Default range is the last 30 days, as on the dashboard. Use `24h`, `7d`, `90d` or `all` when the question says so.
4. Quote ids exactly as returned, so the person can find the same item on the dashboard. Never guess an id: search or list first.
5. If a result carries a `notice`, say what it says when you present the data.

## Limits to state plainly

- Read-only. You cannot block a number, mark an alert as read or change anything. Point to the dashboard for the action.
- There is no call audio. A transcript appears only when the organisation has transcripts turned on.
- Report only what the tools return. If the data does not answer the question, say so rather than filling the gap.
