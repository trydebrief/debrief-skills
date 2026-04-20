# /debrief prep

A one-pager that gets the user ready for a person, topic, or upcoming meeting in two minutes.

The user may optionally specify a **person's name**, a **topic**, or a **meeting title**. If nothing is provided, default to **preparing for the user's meetings today**.

The full arguments string is: `$ARGUMENTS`

## Apps
- **Google Calendar** — meeting details, attendees, past instances.
- **Gmail** — recent threads with the person/attendees.
- **Slack** — recent shared threads or DMs. Also check saved-for-later via `is:saved`.
- **Notion** — shared docs, past meeting notes, project pages.

## Resolve what to prep
- **No argument**: Use Google Calendar to list today's meetings. Prep each.
- **Person name**: Prep a one-pager on that person and the user's relationship with them.
- **Topic or meeting title**: Prep a one-pager on that topic, pulling relevant context.

## Gather context

### For a person:
- Use Gmail for recent threads with this person.
- Use Slack for recent DMs or shared channel activity; include `is:saved` items that reference them.
- Use Google Calendar for past meetings together and upcoming meetings scheduled.
- Use Notion for any shared documents or pages mentioning this person.

### For a meeting:
- Use Google Calendar for invite details — attendees, agenda, notes from past instances.
- Use Gmail and Slack for recent threads with the attendees (include Slack `is:saved`).
- Use Notion for relevant docs, past meeting notes, project pages.

### For a topic:
- Use Gmail, Slack, and Notion for recent discussions, decisions, and open questions.
- Use Google Calendar for related meetings coming up.

## Generate the prep

### For a person:

```
# Prep: [Person name]

## Who they are
[Role, company, how you know them.]

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
