# /debrief recap

Generate a written status update covering everything within a time range across all connected apps. This should be shareable — something you could paste into Slack, an email, or a standup doc.

The user may specify a **time range** (e.g. `this week`, `yesterday`, `last 3 days`, `april`) and/or a **scope** (e.g. a project name, team, or area). If no time range is given, default to **this week**. If a scope is given, filter to only that area.

The full arguments string is: `$ARGUMENTS`

## Gather context

Use whatever MCP tools are available to pull in activity. Adapt to what's connected — don't error if something is missing, just skip it.

- **Calendar**: Meetings attended in the time range. Note key decisions or outcomes if available.
- **Email**: Sent emails — these show what you acted on. Summarize threads, not individual messages.
- **Slack**: Messages you sent, threads you participated in, channels where you were active.
- **GitHub / Linear / Notion**: PRs merged, issues closed, docs updated, tasks completed.

Focus on **what you did**, not what happened to you. Sent > received. Actions > notifications.

## Generate the recap

Structure the output as:

```
# Recap: [time range]

## Highlights
[3-5 bullet points of the most significant things accomplished. Lead with impact, not activity.]

## By area
[Group work by project, team, or theme. Each area gets a heading with bullet points underneath.]

### [Area name]
- [What was done] — [source: Slack thread / PR #123 / email to X]
- ...

## Key decisions
[Any decisions made during this period that others should know about. Include who was involved.]

## Open threads
[Things started but not finished. Handoffs pending. Anything that carries into next period.]
```

## Tone

Write like you're briefing a peer or manager — clear, factual, no fluff. Use past tense. Include sources so the reader can dig deeper if needed.

## Saving output

If the Debrief MCP server is available and the user's config has `syncEnabled`, call `save_output` with the command name `recap`, the full recap output, and `context` set to everything after `recap` in `$ARGUMENTS`.
