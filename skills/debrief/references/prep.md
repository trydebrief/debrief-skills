# /debrief prep

Prepare a one-pager to get the user ready for a person, topic, or their upcoming meetings.

The user may optionally specify a **person's name**, a **topic**, or a **meeting title**. If nothing is provided, default to **preparing for the user's meetings today**.

The full arguments string is: `$ARGUMENTS`

## Resolve what to prep

- **No argument**: Check the calendar for today's meetings. Prep for each one.
- **Person name**: Prep a one-pager on that person and the user's relationship with them.
- **Topic or meeting title**: Prep a one-pager on that topic, pulling relevant context.

## Gather context

Use whatever MCP tools are available. Adapt to what's connected — don't error if something is missing, just skip it.

### For a person:

- **Email**: Recent threads with this person. What's been discussed, what's pending.
- **Slack**: Recent DMs or shared channel activity. Tone and topics.
- **Calendar**: Past meetings together. Upcoming meetings scheduled.
- **Notion / docs**: Any shared documents or pages mentioning this person.
- **Apollo / CRM**: If available, pull company info, role, LinkedIn, recent activity.

### For a meeting:

- **Calendar**: Meeting details — attendees, agenda, notes from past instances.
- **Email / Slack**: Recent threads with the attendees. Open topics between you.
- **Notion / docs**: Relevant docs, past meeting notes, project pages.

### For a topic:

- **Email / Slack / Notion**: Recent discussions, decisions, and open questions on this topic.
- **Calendar**: Related meetings coming up.

## Generate the prep

Structure the output based on what's being prepped:

### For a person:

```
# Prep: [Person name]

## Who they are
[Role, company, how you know them. Pull from CRM/Apollo if available.]

## Recent context
[Summary of your last few interactions — emails, Slack, meetings. What's been discussed.]

## Open threads
[Anything unresolved between you. Pending asks, promises made, follow-ups due.]

## Talking points
[3-5 suggested topics based on what's active between you.]
```

### For a meeting:

```
# Prep: [Meeting title]

## Meeting details
[Time, attendees, recurring or one-off, agenda if available.]

## Context per attendee
[For each attendee: last interaction, anything pending between you.]

## Key topics
[What's likely to come up based on recent threads and shared work.]

## Your prep
[What the user should review, decide, or bring. Specific and actionable.]
```

### For a topic:

```
# Prep: [Topic]

## Current state
[Summary of where things stand based on recent discussions.]

## Recent activity
[Key messages, decisions, or updates from the last 1-2 weeks.]

## Open questions
[Unresolved items or decisions pending.]

## Key people
[Who's involved and their current stance or role.]
```

## Tone

Be thorough but scannable. The user should be able to read this in 2 minutes and walk into a conversation feeling prepared. Use bullet points. Bold the important parts.

## Saving output

If the Debrief MCP server is available and the user's config has `syncEnabled`, call `save_output` with the command name `prep`, the full prep output, and `context` set to everything after `prep` in `$ARGUMENTS`.
