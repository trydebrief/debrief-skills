# /debrief triage

Generate a prioritized triage across all connected channels with draft responses.

## Gather messages

Use whatever MCP tools are available to pull in messages that need attention. Adapt to what's connected.

- **Email**: Unread emails, especially from people (not automated notifications).
- **Slack**: Unread DMs, mentions, and messages in important channels.
- **Notion**: Comments or mentions directed at the user.
- **Other MCPs**: Any messages or notifications that need a response.

## Triage and rank

Rank every item using these tiers:

| Tier | Criteria |
|------|----------|
| **🔴 Urgent** | Blocks someone, time-sensitive, or directly tied to a top priority |
| **🟡 Today** | Should be handled today but not immediately |
| **🟢 This week** | Can wait but shouldn't be forgotten |
| **⚪ Skip** | Matches the user's deprioritize list, or truly doesn't need a response |

## Output format

For each item (skip the ⚪ tier unless there are fewer than 5 total items):

```
### 🔴 [Source] Subject or summary
**From:** Name
**Received:** Time
**Why it matters:** One sentence connecting to priorities
**Draft reply:**
> [A ready-to-send reply the user can copy, edit, or approve. Match the formality of the source — casual for Slack, professional for email.]
```

Group items by tier. Within each tier, sort by most urgent/important first.

## End with a summary

```
---
**Triage summary:** X urgent, Y today, Z this week, W skipped
**Estimated time to clear:** ~N minutes
```

## Saving output

If the Debrief MCP server is available and the user's config has `syncEnabled`, call `save_output` with the command name `triage`, the full triage output, and `context` set to everything after `triage` in `$ARGUMENTS`.
