# /debrief weekly

Auto-draft a weekly status update from Slack, meetings, email, and shipped work.

## Apps
- **Slack** — messages sent that signal progress or blockers. Also check saved-for-later via `is:saved`.
- **Granola** — meetings attended and their outcomes.
- **Gmail** — major threads the user drove.
- **Linear** — tickets closed, in progress, blocked.

## Step 1: Gather (last 7 days)
- Search Slack for messages the user sent that signal progress or blockers; include `is:saved` items for bookmarked context.
- Use Granola to list meetings attended and their outcomes.
- Use Linear to list tickets closed, in progress, and blocked.
- Use Gmail to surface major threads the user drove.

## Step 2: Structure
- **Shipped** (concrete, linkable to the Linear ticket / PR / Slack thread)
- **In progress** (with expected completion)
- **Blocked** (with what would unblock)
- **Next week** (top 3 priorities)

## Step 3: Draft and confirm
Show the draft. Ask where to send (Slack channel, email, Notion page). Don't post or send without confirmation.

## Guidelines
- Link to artifacts — PRs, Linear tickets, docs — rather than describing them.
- Keep "blocked" honest; don't soften to protect feelings.
