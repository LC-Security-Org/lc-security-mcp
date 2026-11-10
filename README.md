# LC Scam Intelligence for Claude

Ask Claude about the scam calls your LC Security decoy lines have answered: what is new, which campaigns are growing, who is behind a number, what to block, or have Claude write the briefing for your fraud team.

It reads exactly what your LC Security dashboard shows, scoped to your organisation, and the numbers match the screen. It is **read-only**: it cannot change, block or delete anything, and it never receives call audio.

You need an LC Security account that belongs to an organisation. Access is by invitation; ask your LC Security contact.

## Install

### Claude Code

```sh
claude plugin marketplace add LC-Security-Org/lc-security
claude plugin install lc-scam-intelligence@lc-security
```

Or inside Claude Code: `/plugin marketplace add LC-Security-Org/lc-security`, then `/plugin install lc-scam-intelligence@lc-security`.

### Claude Desktop and Claude on the web

Add the connector by its address. In Claude, open **Settings → Connectors → Add custom connector** (the name and availability of this menu depend on your Claude plan). Name it **LC Scam Intelligence** and enter:

```
https://app.lcsecurity.ai/mcp
```

## Log in

The connector signs you in **in your browser**. No password is typed into Claude or stored by it.

1. **Claude Code:** run `/mcp`, choose `lc-scam-intelligence`, then **Authenticate**. **Claude Desktop or web:** open the connector and choose **Connect**.
2. Your browser opens LC Security. If you are already signed in to LC Security in that browser, you go straight to the question; otherwise sign in first.
3. Check the name of the application asking, then choose **Allow**.
4. Go back to Claude. You are connected.

To disconnect, remove the connector in Claude. To use a different account, choose **Use another account** on the approval page.

## Use it

Name **LC Scam Intelligence** in your question, so Claude reads your data rather than answering from general knowledge. Some starting points:

- "Using LC Scam Intelligence, give me an overview of the last 7 days. What should I worry about first?"
- "Using LC Scam Intelligence, which scam campaigns are growing, and which numbers are behind the biggest one?"
- "Using LC Scam Intelligence, look into +44 20 7946 0000. Where did it appear and is it blocked?"
- "Using LC Scam Intelligence, what should we block next? Give me the top five and why."
- "Using LC Scam Intelligence, walk me through one of the scam conversations from the biggest campaign."
- "Using LC Scam Intelligence, write a one-page briefing for my fraud team."

If you belong to more than one organisation, say which: "for the acme organisation".

The connector also offers ready-made starting points. In Claude Desktop, choose **+** and look under LC Scam Intelligence; in Claude Code, type `/` and pick one under `lc-scam-intelligence`.

**In Claude Code**, the plugin adds shortcuts: `/lc-scam-intelligence:briefing` and `/lc-scam-intelligence:investigate <number or name>`, and Claude uses the LC Scam Intelligence skill on its own when you ask about your scam data.

## What it can and cannot do

| It can | It cannot |
|---|---|
| Show the overview, campaigns, conversations, numbers, accounts, URLs, wallets, tactics, alerts and blocklist | Block a number, mark an alert as read, or change anything |
| Show a conversation transcript, when your organisation has transcripts turned on | Play or return call audio, ever |
| Answer for the time range you ask for (default: the last 30 days, as on the dashboard) | See any organisation you do not belong to |

## Troubleshooting

- **"Sign in" or "expired" message:** connect again (`/mcp` in Claude Code, **Connect** in Claude Desktop).
- **Nothing shows up for my organisation:** your account may not be a member of it yet. Ask your LC Security contact.
- **Claude answers without using it:** start with "Using LC Scam Intelligence, …".
- **The browser page says the request expired:** start the connection again from Claude; the approval link works once.

## What is in this repository

- `.claude-plugin/marketplace.json`: the plugin marketplace.
- `plugins/lc-scam-intelligence/`: the plugin, which adds the connector (`.mcp.json`) and three skills.

The connector itself runs at `https://app.lcsecurity.ai/mcp`. Questions: [lcsecurity.ai](https://lcsecurity.ai). Copyright LC Security, all rights reserved; see `LICENSE`.
