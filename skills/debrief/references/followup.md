# /debrief followup

Track the user's open items across every connected channel. For each one, explain what's going on, whether it's resolved, and what the user should do — then draft a message if they need to act.

The user may add scope after the command to narrow the focus (e.g. `followup hiring`, `followup with Sarah`, `followup funding round`, `followup slack only`). If scope is provided, filter to only matching items. If no scope is given, check everything.

The full arguments string is: `$ARGUMENTS`

This is not an inbox scan. This is an accountability check. The user wants to know: **what fell through the cracks, what got resolved badly, and what still needs pushing.**

## Gather context

Use whatever MCP tools are available. Adapt to what's connected — don't error if something is missing, just skip it.

Look at items from the **last two weeks**:

- **Email**: Threads the user sent or replied to that have no resolution. Sent messages still awaiting a response. Starred, snoozed, or flagged threads.
- **Slack**: DMs and threads the user participated in that are still active or went silent. Messages waiting on a response from either side. Also check `is:saved` across both public and private channels to catch Saved for Later items.
- **Notion / docs**: Tasks assigned to the user. Open items the user created or was mentioned on.
- **Calendar**: Action items from recent meetings (check meeting notes if available).

Focus on items where **something should have happened by now but hasn't**, or where **something happened but the outcome is unclear or unsatisfying**.

## Analyze each item

For every item, work through this:

1. **What is this about?** The substance — not "email from Sarah" but what Sarah is asking about and why it matters. Give enough context that the user doesn't need to go read the thread.

2. **Why are we tracking this?** Connect it to the user's priorities, a deadline, a dependency, or a commitment they made. If you can't figure out why it matters, say so.

3. **Timelines:** Any deadlines, expected response windows, or dependencies. If someone said "by end of week" two weeks ago, flag that.

4. **Status and resolution:** What happened since the user last engaged? Did someone reply, go quiet, or close it out? If it was resolved, was the resolution actually good enough?

5. **Who needs to do what next?** Name the person and the specific action. If it's the user, draft a message. If it's someone else and they're overdue, draft a nudge. If it's done, say so.

## Output format

Present everything in tables. People scan, they don't read — keep it tight.

```
# Follow-ups

**X need your action, Y waiting on others, Z cleared**

## You need to act

| # | Source | Item | Status | Next step |
|---|--------|------|--------|-----------|
| 1 | Slack | [Descriptive title — the topic, not the person] | [What happened or didn't, in one line] | [Specific action] |
| 2 | Email | ... | ... | ... |

**Drafts**

**1 — [Title]:** [Ready-to-send message in the user's voice. Match the channel. Reference specifics — no generic nudges.]

**2 — [Title]:** ...

## Waiting on others

| # | Source | Item | Who | Since | Next step |
|---|--------|------|-----|-------|-----------|
| 1 | Slack | [Title] | [Person] | [Date or "2 weeks"] | Wait / Nudge / Escalate |

Include a draft nudge below the table only for overdue or stale items, same format as above.

## Cleared

| Source | Item | Resolution |
|--------|------|------------|
| Email | [Title] | [One line — what happened and whether it was sufficient] |
```

Rules:
- Every item gets exactly one row. No multi-paragraph entries.
- The "Item" column describes the substance, not "email from Sarah" — what Sarah is asking about.
- Draft messages go below their table, not inline. Only include drafts for items that need action.
- If there are no items in a section, omit that section entirely.

## Tone

Be a Chief of Staff, not an assistant. If something is overdue, say it plainly. If a resolution was weak, say why. If the user dropped the ball, tell them. The goal is accountability and clarity — the user should walk away knowing exactly what's unresolved and what to do about it.

When drafting messages, write in the user's voice — match how they actually communicate on that channel. Be specific to the actual conversation, not generic.

## Saving output

If the Debrief MCP server is available and the user's config has `syncEnabled`, call `save_output` with the command name `followup`, the full follow-up output, and `context` set to everything after `followup` in `$ARGUMENTS`.
