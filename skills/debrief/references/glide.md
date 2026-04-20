# /debrief glide

Walk a tracked list and flag anything stalled — "on glide path or nothing's happened."

## Apps
- **Notion** — pull the tracked initiatives list.
- **Linear** — cross-check progress with ticket activity.

## Step 1: Load the list
Pull the tracked initiatives page from Notion (or Linear projects). Ask the user which list if multiple exist.

## Step 2: Per item, classify
For each initiative, check the latest activity in both Notion (page edits, comments) and Linear (ticket movement, status changes). Then classify:
- **On glide path** — visible progress in last 7 days, on track for target
- **Slipping** — some progress, but trend is off target
- **Stalled** — no activity in 14+ days
- **At risk** — active but with a flagged blocker

Evidence each classification with a timestamped artifact (Notion page URL, Linear ticket ID).

## Step 3: Present
Group by status. Lead with stalled + at risk. End with a suggestion for which 1–2 to unblock first.

## Guidelines
- "Looks busy" isn't progress. Tie status to a concrete delivered artifact.
- Don't mark stalled without checking Slack/email for off-system activity.
