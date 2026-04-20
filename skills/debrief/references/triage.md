# /debrief triage

A prioritized triage across Gmail, Slack, and Notion with draft responses ready to send.

## Apps
- **Gmail** — unread email and draft creation.
- **Slack** — unread DMs, mentions, important channels; draft creation. Also check saved-for-later via `is:saved`.
- **Notion** — comments and mentions directed at the user.

## Step 1: Gather messages
- Use Gmail for unread, especially from people (not automated).
- Use Slack for unread DMs, @mentions, and messages in important channels; include `is:saved` items the user bookmarked.
- Use Notion for comments and mentions directed at the user.

## Step 2: Triage and rank

| Tier | Criteria |
|------|----------|
| **🔴 Urgent** | Blocks someone, time-sensitive, or directly tied to a top priority |
| **🟡 Today** | Should be handled today but not immediately |
| **🟢 This week** | Can wait but shouldn't be forgotten |
| **⚪ Skip** | Matches the user's deprioritize list, or truly doesn't need a response |

## Step 3: Output format

For each item (skip the ⚪ tier unless there are fewer than 5 total items):

```
### 🔴 [Source] Subject or summary
**From:** Name
**Received:** Time
**Why it matters:** One sentence connecting to priorities
**Draft reply:**
> [A ready-to-send reply the user can copy, edit, or approve. Match the formality of the source — casual for Slack, professional for email.]
```

Save Gmail drafts via `create_draft` and Slack drafts via `send_message_draft`. Group items by tier; within each tier, sort by most urgent.

## Step 4: Summary

```
---
**Triage summary:** X urgent, Y today, Z this week, W skipped
**Estimated time to clear:** ~N minutes
```
