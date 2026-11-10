---
name: briefing
description: Write a one-page briefing for a fraud team from LC Scam Intelligence data: top threats with numbers, what changed, open decisions and recommended actions. Use when asked for a briefing, weekly summary, or "what should I worry about".
---

# Briefing from LC Scam Intelligence

Follow the `lc-scam-intelligence` skill for how to use the tools and what to say about limits.

1. Call `get_overview` for the period (default 7 days for a weekly briefing), then `list_campaigns`, `list_alerts` and `get_blocklist`.
2. Write one page with these parts, in this order:
   - **Top three threats**: each with its numbers and what the callers are trying to get.
   - **What changed** against the previous period.
   - **Waiting on a decision**: alerts and blocklist entries that still need one.
   - **Recommended actions**: three, each tied to something in the data.
3. Quote ids as returned. Report any `notice` from the data. You cannot block anything yourself; say that actions happen on the dashboard.
