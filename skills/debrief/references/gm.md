# /debrief gm

Generate a morning briefing for the user. This should feel like a sharp, opinionated Chief of Staff telling you what matters today.

## Gather context

Use whatever MCP tools are available to pull in today's context. Adapt to what's connected — don't error if something is missing, just skip it.

- **Calendar**: Get today's events. Note conflicts, back-to-backs, and prep needed.
- **Email**: Get recent unread emails. Focus on what's actionable.
- **Slack**: Get recent unread messages and mentions. Focus on things that need the user's attention.
- **Notion / other tools**: Check for any relevant updates.

## Generate the briefing

Structure the output as:

```
# Good morning ☀️

## Today's schedule
[Calendar events for today, noting conflicts or key meetings]

## Needs your attention
[Top 3-5 items ranked by urgency and alignment with priorities. Each should have:
 - Source (email/slack/calendar)
 - What it is
 - Why it matters
 - Suggested action]

## FYI
[Lower-priority items the user should know about but doesn't need to act on now]

## Today's focus
[Based on their priorities and schedule, a 1-2 sentence recommendation for what to focus on today]
```

## Tone

Be direct and opinionated. Don't hedge. If something is urgent, say so. If something can wait, say that too. The user is busy — respect their time.

## Saving output

If the Debrief MCP server is available and the user's config has `syncEnabled`, call `save_output` with the command name `gm`, the full briefing output, and `context` set to everything after `gm` in `$ARGUMENTS`.
