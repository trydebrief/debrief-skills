# /debrief promises

Extract commitments the user made in meetings, Slack, and email. Flag the unresolved ones past their implied due date.

## Apps
- **Slack** — search messages the user sent for first-person commitments. Also check saved-for-later via `is:saved`.
- **Gmail** — search sent mail for the same.
- **Granola** — search recent transcripts for verbal commitments.

## Step 1: Scan (last 30 days)
- Search Slack for the user's sent messages containing commitment phrases like "I'll send…", "I'll circle back…", "I'll get you…", "by Friday"; include `is:saved` items the user bookmarked.
- Search Gmail sent mail for the same.
- Search Granola transcripts for verbal commitments.

## Step 2: Resolve
For each, check whether the promised artifact exists (Gmail sent mail, Notion doc shared, Slack message posted). Mark resolved / unresolved.

## Step 3: Present
Three buckets:
- **Overdue** — past implied deadline, no evidence of delivery
- **Due this week**
- **Open-ended** — no deadline but still outstanding

## Guidelines
- Err toward listing rather than hiding — better to dismiss a resolved item than miss an overdue one.
- Include the original quote so the user can jog their memory.
