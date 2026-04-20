# /debrief followup

An accountability check across Gmail, Slack, Notion, and Calendar action items. Surface what fell through the cracks, what got resolved badly, and what still needs pushing.

The user may add scope after the command to narrow the focus (e.g. `followup hiring`, `followup with Sarah`, `followup funding round`, `followup slack only`). If scope is provided, filter to only matching items. If no scope is given, check everything.

The full arguments string is: `$ARGUMENTS`

This is not an inbox scan. This is an accountability check. The user wants to know: **what fell through the cracks, what got resolved badly, and what still needs pushing.**

## Apps
- **Gmail** — threads with no resolution; sent messages awaiting reply.
- **Slack** — DMs and threads still active or gone silent. Check saved-for-later via `is:saved` (critical — these are the items the user told themselves to come back to).
- **Notion** — tasks assigned to the user; open items the user owns.
- **Google Calendar** — action items from recent meeting notes.

## Step 1: Gather (last two weeks)
- Use Gmail for threads with no resolution and sent messages awaiting reply (also starred/snoozed/flagged).
- Use Slack for DMs and threads still active or gone silent; search `is:saved` for Saved-for-Later items.
- Use Notion for tasks assigned to the user and open items mentioned.
- Use Google Calendar to find recent meetings; check linked notes for unresolved action items.

Focus on items where **something should have happened by now but hasn't**, or where **something happened but the outcome is unclear or unsatisfying**.

## Step 2: Analyze each item

For every item, work through this:

1. **What is this about?** The substance — not "email from Sarah" but what Sarah is asking about and why it matters.
2. **Why are we tracking this?** Connect it to the user's priorities, a deadline, a dependency, or a commitment they made.
3. **Timelines:** Any deadlines, expected response windows, or dependencies. If someone said "by end of week" two weeks ago, flag that.
4. **Status and resolution:** What happened since the user last engaged? If it was resolved, was the resolution actually good enough?
5. **Who needs to do what next?** Name the person and the specific action. If it's the user, draft a Gmail / Slack message.

## Step 3: Output format

```
# Follow-ups

**X need your action, Y waiting on others, Z cleared**

## You need to act

| # | Source | Item | Status | Next step |
|---|--------|------|--------|-----------|
| 1 | Slack | [Descriptive title — the topic, not the person] | [What happened or didn't, in one line] | [Specific action] |
| 2 | Gmail | ... | ... | ... |

**Drafts** (use Gmail `create_draft` or Slack `send_message_draft`)

**1 — [Title]:** [Ready-to-send message in the user's voice. Match the channel. Reference specifics — no generic nudges.]

**2 — [Title]:** ...

## Waiting on others

| # | Source | Item | Who | Since | Next step |
|---|--------|------|-----|-------|-----------|
| 1 | Slack | [Title] | [Person] | [Date or "2 weeks"] | Wait / Nudge / Escalate |

Include a draft nudge below the table only for overdue or stale items.

## Cleared

| Source | Item | Resolution |
|--------|------|------------|
| Gmail | [Title] | [One line — what happened and whether it was sufficient] |
```

Rules:
- Every item gets exactly one row. No multi-paragraph entries.
- The "Item" column describes the substance, not "email from Sarah" — what Sarah is asking about.
- Draft messages go below their table, not inline. Only include drafts for items that need action.
- If there are no items in a section, omit that section entirely.

## Tone
Be a Chief of Staff, not an assistant. If something is overdue, say it plainly. If a resolution was weak, say why. If the user dropped the ball, tell them. The goal is accountability and clarity.

When drafting messages, write in the user's voice — match how they actually communicate on that channel. Be specific to the actual conversation, not generic.
