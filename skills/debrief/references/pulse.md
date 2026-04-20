# /debrief pulse

Weekly rollup: what shipped, what's blocked, what's new across Slack, Linear, and GitHub.

## Apps
- **Slack** — channel activity, announcements, blocked language. Also check saved-for-later via `is:saved`.
- **Linear** — tickets shipped, in progress, blocked.
- **GitHub** — merged PRs, open PRs, releases.

## Step 1: Window
Default to last 7 days. Confirm with user.

## Step 2: Aggregate
- **Shipped**: use GitHub for merged PRs and releases; use Linear for closed tickets marked done.
- **In flight**: use GitHub for open PRs with recent activity; use Linear for tickets in progress.
- **Blocked**: use Linear for tickets with "blocked" label; search Slack for threads with blocking language (include `is:saved`).
- **New**: search Slack for initiative announcements; use Linear for new projects.

## Step 3: Present
Keep it skimmable. Link everything (PR URLs, Linear ticket IDs, Slack permalinks). Lead with shipped. End with blocked.

## Guidelines
- No narrative filler. Bullets with links.
- If a team had no activity, say so — silence is signal.
