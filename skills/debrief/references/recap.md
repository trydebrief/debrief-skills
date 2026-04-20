# /debrief recap

A written status update covering everything within a time range across Calendar, Gmail, Slack, Linear, and GitHub. Shareable — paste into Slack, an email, or a standup doc.

The user may specify a **time range** (e.g. `this week`, `yesterday`, `last 3 days`, `april`) and/or a **scope** (e.g. a project name, team, or area). If no time range is given, default to **this week**. If a scope is given, filter to only that area.

The full arguments string is: `$ARGUMENTS`

## Apps
- **Google Calendar** — meetings attended in the time range.
- **Gmail** — sent threads (signal of what the user acted on).
- **Slack** — messages sent and threads participated in. Also check saved-for-later via `is:saved`.
- **Linear** — tickets closed.
- **GitHub** — PRs merged.

## Step 1: Gather activity
Focus on **what the user did**, not what happened to them. Sent > received. Actions > notifications.
- Use Google Calendar for meetings attended and key decisions.
- Use Gmail for sent threads (summarize threads, not messages).
- Use Slack for messages sent and active threads; include `is:saved` items the user flagged as important.
- Use Linear for tickets closed in the range.
- Use GitHub for merged PRs in the range.

## Step 2: Generate the recap

```
# Recap: [time range]

## Highlights
[3-5 bullet points of the most significant things accomplished. Lead with impact, not activity.]

## By area
[Group work by project, team, or theme. Each area gets a heading with bullet points underneath.]

### [Area name]
- [What was done] — [source: Slack thread / PR #123 / Gmail to X / Linear ticket]
- ...

## Key decisions
[Any decisions made during this period that others should know about. Include who was involved.]

## Open threads
[Things started but not finished. Handoffs pending. Anything that carries into next period.]
```

## Tone
Write like you're briefing a peer or manager — clear, factual, no fluff. Use past tense. Include sources so the reader can dig deeper if needed.
