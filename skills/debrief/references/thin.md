# /debrief thin

Flag closed items where the resolution looks thin: closed tickets without a fix commit, email threads marked done without a confirmation from the other side, decisions recorded without a followup artifact.

## Apps
- **Linear** — recently closed tickets and their linked PRs.
- **Gmail** — recently archived threads.
- **Slack** — recent meeting/decision threads marked resolved. Also check saved-for-later via `is:saved`.

## Step 1: Pull recently closed (last 14 days)
- Use Linear to list tickets closed in last 14 days.
- Use Gmail to list threads archived recently.
- Search Slack for decision threads in the same window; include `is:saved` items to catch ones the user bookmarked.

## Step 2: Quality check
For each:
- **Linear**: is there a linked PR / commit on the ticket?
- **Gmail**: did the counterparty acknowledge in the thread?
- **Slack**: did the followup action item actually happen (cross-check Linear / Notion)?

## Step 3: Surface the thin ones
Present with the specific gap and a link to the source. Do not reopen anything — this is a review, not an action.

## Guidelines
- Be charitable. Many items are legitimately closed without ceremony. Only flag where the gap is real.
