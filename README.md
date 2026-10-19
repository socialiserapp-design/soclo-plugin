# Soclo for Claude

Social media creation, scheduling, analytics, and ad management for Claude — connected to your live Soclo workspace through the remote MCP server at `https://mcp.soclo.app/mcp/auth`.

## Overview

Soclo gives Claude 415 tools across eight workspace areas so you can plan, create, schedule, publish, and measure content and campaigns from a single conversation:

| Area | What Claude can do | Spending / external side effects | Confirmation required |
| :--- | :--- | :--- | :--- |
| **Brand** | Read and update your brand profile, voice, colours, logos, and connected social accounts. | Free workspace updates. | Writes require owner confirmation when replacing brand assets. |
| **Library** | Browse, search, organise, and inspect images, videos, audio tracks, and reusable creative assets. | Free reads and library organisation. | Deleting library items requires explicit confirmation (`confirm: true`). |
| **Studio** | Generate and edit images, videos, voiceovers, music, and multi-slide visuals using Soclo's creative models. | Uses Soclo workspace credits when generating or rendering media. | Every credit-spending generation tool states its credit use and requires confirmation (`confirm: true`) when applicable. |
| **Schedule** | Inspect your content calendar, find best posting times, and schedule, reschedule, or unschedule posts. | Publishes to connected social networks at the scheduled time. | Scheduling, rescheduling, or cancelling scheduled posts requires explicit confirmation (`confirm: true`). |
| **Posts** | Read published posts and drafts, save and edit drafts, and publish or delete social posts across platforms. | Publishing posts sends content live to connected social accounts. | Publishing or deleting a post requires explicit confirmation (`confirm: true`). Saving drafts is non-destructive. |
| **Agreed Plan** | Read planning guides, and save, reopen, edit, and price multi-post or advert plans written by this assistant. | Free planning and pricing estimates; does not publish or spend until executed. | Approving or deleting a saved plan requires explicit confirmation. |
| **Ads** | Inspect ad accounts, draft campaigns, preview targeting and budgets, and launch or pause paid ad campaigns. | **Spends real money** on your connected ad account (outside Soclo credits) once a campaign is confirmed and goes live. | Creating, launching, changing budgets, or pausing live ad campaigns requires explicit confirmation (`confirm: true`) after reviewing the budget. |
| **Insights** | Read post performance, audience demographics, engagement trends, and ad campaign metrics. | Read-only analytics; no credits or ad spend used. | None (read-only). |

## Installation

### Claude.ai & Claude Desktop (Directory / Remote MCP)

1. Open **Settings → Connectors** (or browse the Claude Directory) and select **Soclo**.
2. Connect using `https://mcp.soclo.app/mcp/auth` and complete the Soclo OAuth sign-in in your browser.

### Claude Code CLI

```bash
claude mcp add --transport http soclo https://mcp.soclo.app/mcp/auth
```

Or install this plugin directly from GitHub:

```bash
/plugin marketplace add socialiserapp-design/soclo-plugin
/plugin install soclo@soclo
```

## Authentication & Permissions

- **OAuth 2.0 with PKCE:** You sign in on `soclo.app` and review the exact permissions requested before granting access.
- **Safety & Confirmation Gates:** Read-only tools (`readOnlyHint: true`) never mutate your workspace. Tools that publish posts, consume Soclo Studio credits, delete items, or spend real money on connected ad accounts clearly declare their effect and require explicit confirmation before executing.

## Included Skills

- **`/soclo-brand`** — Inspect or update your brand kit, tone of voice, and connected social profiles.
- **`/soclo-studio`** — Create images, videos, audio, and social assets in Soclo Studio and save drafts.
- **`/soclo-schedule`** — Plan your content calendar, check upcoming slots, and schedule or publish approved drafts.
- **`/soclo-ads-insights`** — Review post and campaign performance, or draft and price paid ad campaigns with clear budget checks.

## Support & Privacy

- **Website:** [https://soclo.app](https://soclo.app)
- **MCP Documentation:** [https://soclo.app/mcp](https://soclo.app/mcp)
- **Privacy Policy:** [https://soclo.app/privacy](https://soclo.app/privacy)
- **Terms of Service:** [https://soclo.app/terms](https://soclo.app/terms)
- **Support:** [mailto:hello@soclo.app](mailto:hello@soclo.app)
