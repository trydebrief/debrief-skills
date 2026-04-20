# /debrief clientlog

Maintain one running log per client to avoid context bleed across accounts.

## Apps
- **Granola** — pull the meeting transcript.
- **Notion** — find/create the client's page and append the dated entry.

## Step 1: Identify client
Ask which client, or infer from the most recent meeting's attendees. Search Notion for that client's page; create it in Notion if missing.

## Step 2: Append, don't overwrite
Pull the target meeting from Granola. Append a new dated section to the client's Notion page with: attendees, decisions, action items, open threads.

## Step 3: Cross-reference
At the top of the Notion page, maintain a rolling "open threads" list. Close threads when a later meeting resolves them. Surface stale threads (>14 days untouched) at the top of the log.

## Guidelines
- Never mix clients in a single log entry.
- Preserve prior entries — this is an audit trail, not a dashboard.
