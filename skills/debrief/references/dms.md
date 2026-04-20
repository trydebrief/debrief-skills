# /debrief dms

Things buried in Slack DMs that need a reply.

## Apps
- **Slack** — read DM history and identify unanswered messages. Also check saved-for-later via `is:saved`.

## Step 1: Scan DMs (last 7 days)
Scan Slack DM threads. Flag any thread where:
- The other person sent the last message
- It's a question or request (not a reaction/acknowledgment)
- User hasn't replied

Include `is:saved` DM items the user bookmarked.

## Step 2: Classify
- **Needs a real reply** — substantive
- **Quick ack** — thanks, thumbs-up, short confirm
- **Can wait** — low-priority

## Step 3: Present
Lead with "Needs a real reply". Offer to draft via Slack `send_message_draft`.

## Guidelines
- Don't surface DMs the user explicitly closed with "got it, thanks".
- Respect DND windows — don't suggest replies outside working hours unless the item is truly urgent.
