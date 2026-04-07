# /debrief followup

Review the user's pending threads and saved-for-later items. For each one, give a status update, say what needs to happen next, and draft a reply if the user needs to act.

## Gather context

Use whatever MCP tools are available. Adapt to what's connected — don't error if something is missing, just skip it.

- **Email**: Threads the user started or replied to that don't have a resolution. Sent messages awaiting a response. Starred or snoozed items.
- **Slack**: Saved messages, bookmarked items, threads the user participated in that are still active. DMs waiting on a response (from either side).
- **Notion / docs**: Tasks assigned to the user. Comments the user was mentioned in.
- **Calendar**: Action items from recent meetings that may need follow-up.

Focus on threads where the **ball is in someone's court** (the user's or someone else's).

## Analyze and categorize

For each item, determine:
1. **Status**: What happened since the user last engaged? Did someone reply? Did it go quiet?
2. **Who's on the hook**: Is the user waiting on someone, or is someone waiting on the user?
3. **What needs to happen**: Specific next action.

## Output format

Group items by urgency:

```
# Follow-ups

## You need to respond
[Items where someone is waiting on the user.]

### [Source] Subject or summary
**Thread with:** [Person/people]
**Last activity:** [When and what happened]
**Status:** [What's changed since you last looked]
**Action needed:** [What to do]
**Draft reply:**
> [A ready-to-send reply. Match the tone of the source — casual for Slack, professional for email.]

## Waiting on others
[Items where the user is waiting on someone else.]

### [Source] Subject or summary
**Waiting on:** [Person]
**You last wrote:** [When and what you said]
**Status:** [Still no reply / they replied but didn't address X / etc.]
**Suggested nudge:**
> [A gentle follow-up the user can send if needed.]

## Resolved or stale
[Items that appear to be done or no longer relevant.]

### [Source] Subject or summary
**Resolution:** [What happened or why it's stale]
```

End with a summary:

```
---
**Follow-up summary:** X need your response, Y waiting on others, Z resolved/stale
```

## Tone

Be direct. Don't sugarcoat — if the user dropped the ball, say so plainly. If someone else is ghosting, flag it. The goal is to clear the backlog, not describe it politely.

## Saving output

If the Debrief MCP server is available and the user's config has `syncEnabled`, call `save_output` with the command name `followup` and the full follow-up output.
