# The Alliance Marketing — Claude plugin

Product marketing guidance from [The Alliance](https://www.productmarketingalliance.com/),
grounded in a curated library of practitioner content: positioning, messaging,
differentiation, pricing, launches, go-to-market, ICP and sales enablement.

This repo is the distribution channel only. It carries the plugin manifest, the
remote server address and the router skill — the server itself is hosted at
`https://mcp.allianceteam.io/mcp`.

## Install

In Claude Code:

```
/plugin marketplace add hernie-0x0/MCP-Plugin
/plugin install alliance-marketing@the-alliance
```

On claude.ai: **Directory → Plugins → Add marketplace → `hernie-0x0/MCP-Plugin`**, then install
**The Alliance Marketing**.

Claude will prompt you to authenticate the `marketing` server on first use —
sign in with the Google account attached to your Alliance membership. `/mcp`
shows connection status. An active membership is required; sign-in fails for
accounts without one.

## What you get

| Component | What it does |
|-----------|--------------|
| `plugin/.mcp.json` | Connects Claude to the hosted MCP server. OAuth is negotiated by the client — no keys or secrets to paste. |
| `plugin/skills/alliance-mcp-governor/` | A router skill that is active *before* tool discovery, so product marketing questions get routed into the connector instead of answered from general knowledge. |

Ask a product marketing question the way you normally would — "how do I explain
what we do to a technical buyer", "what makes us different from X", "who is this
actually for" — and Claude will pull from the library and cite the practitioners
it drew on.

## Updating

```
/plugin update alliance-marketing@the-alliance
```

Most improvements — tool behaviour, workflow, output format, the content index —
live server-side and reach you with no update needed. An update is only required
when the plugin's `version` changes, which happens when the server address or the
router skill changes.

## Support

- Docs and connection help: <https://mcp.allianceteam.io/docs>
- Membership and account questions: The Alliance member support

Issues with the plugin itself can be filed on this repo.
