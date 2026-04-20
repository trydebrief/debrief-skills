# /debrief slacktri

Unread across Slack channels and DMs, ranked by who/what matters.

## Apps
- **Slack** — read unread messages across channels and DMs; identify VIPs via user profile lookups. Also surface saved-for-later via `is:saved`.

## Step 1: Pull unread
List unread Slack messages across all channels and DMs the user is in. Include threads they're participating in. Surface `is:saved` items the user bookmarked.

## Step 2: Rank
Priority order:
1. DMs from key people (user's manager, direct reports, known VIPs — look them up via Slack user search)
2. @mentions
3. Threads the user started or recently participated in
4. Channel messages in channels tagged "important" in user config
5. Saved-for-later (`is:saved`) items
6. Everything else (summarize, don't enumerate)

## Step 3: Present
For top items: who, what (one line), and a suggested action (reply, acknowledge, ignore). Offer to draft replies in batch via Slack `send_message_draft`.

## Guidelines
- Don't list every unread. Most Slack noise is skippable.
- Flag anything with a time-sensitive ask explicitly.
