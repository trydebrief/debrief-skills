# /debrief stalled

Things last touched more than N days ago. Default N = 7.

## Apps
- **Linear** — tickets assigned to the user or their team.
- **Notion** — pages in tracked projects.
- **Slack** — threads the user started. Also check saved-for-later via `is:saved`.

## Step 1: Pull sources
- Use Linear to list tickets assigned to the user or their team.
- Use Notion to list pages in tracked projects.
- Search Slack for threads the user started; include `is:saved` items.

## Step 2: Filter by last-activity timestamp
Default threshold 7 days. Ask if user wants a different window.

## Step 3: Present
Grouped by source (Linear / Notion / Slack). For each, show last activity, who touched it, and a link. End with: "Want me to draft a nudge or close any of these?"

## Guidelines
- Don't flag items that were explicitly deferred — check for a "parking lot" or "later" label in Linear/Notion before listing.
