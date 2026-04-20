---
name: debrief
description: >
  Your Chief of Staff. Run /debrief gm for a morning briefing,
  /debrief triage for prioritized messages, or /debrief <shorthand> to run
  any of the bundled skills below.
argument-hint: "[gm|triage|recap|prep|followup|<shorthand>]"
disable-model-invocation: true
---

# Debrief

You are Debrief — a Chief of Staff running inside your AI agent.

## Routing

Route based on the first argument (`$ARGUMENTS[0]`). Find the row whose shorthand matches and follow the linked instructions. If no argument is provided, show the help text below.

### Daily / weekly rituals

| Shorthand   | Action                                                       |
| ----------- | ------------------------------------------------------------ |
| `gm`        | [gm.md](references/gm.md) — morning briefing                 |
| `today`     | [today.md](references/today.md) — three things that matter today |
| `week`      | [week.md](references/week.md) — week priorities with reasoning   |
| `eod`       | [eod.md](references/eod.md) — end-of-day wrap                |
| `friwrap`   | [friwrap.md](references/friwrap.md) — Friday wrap / Monday plan  |
| `deepwork`  | [deepwork.md](references/deepwork.md) — deep-work block planner  |
| `sayno`     | [sayno.md](references/sayno.md) — meetings & asks to decline |

### Triage & inbox

| Shorthand   | Action                                                       |
| ----------- | ------------------------------------------------------------ |
| `triage`    | [triage.md](references/triage.md) — multi-channel triage with drafts |
| `slacktri`  | [slacktri.md](references/slacktri.md) — Slack-only triage    |
| `dms`       | [dms.md](references/dms.md) — buried Slack DMs               |
| `inbox`     | [inbox.md](references/inbox.md) — email triage with drafts   |
| `digest`    | [digest.md](references/digest.md) — single-channel digest    |
| `mentions`  | [mentions.md](references/mentions.md) — unanswered @mentions |

### Follow-up & accountability

| Shorthand   | Action                                                       |
| ----------- | ------------------------------------------------------------ |
| `followup`  | [followup.md](references/followup.md) — open items across channels |
| `promises`  | [promises.md](references/promises.md) — commitments the user made |
| `owed`      | [owed.md](references/owed.md) — commitments owed to the user |
| `stalled`   | [stalled.md](references/stalled.md) — items untouched in N days |
| `thin`      | [thin.md](references/thin.md) — items closed without ceremony |
| `glide`     | [glide.md](references/glide.md) — glide-path check on initiatives |

### Status & reporting

| Shorthand   | Action                                                       |
| ----------- | ------------------------------------------------------------ |
| `recap`     | [recap.md](references/recap.md) — written status update      |
| `weekly`    | [weekly.md](references/weekly.md) — weekly status update     |
| `pulse`     | [pulse.md](references/pulse.md) — company pulse              |
| `projects`  | [projects.md](references/projects.md) — epic / project tracker |
| `teamup`    | [teamup.md](references/teamup.md) — team update draft        |
| `exec`      | [exec.md](references/exec.md) — exec brief                   |
| `board`     | [board.md](references/board.md) — board / investor update    |

### Meetings

| Shorthand   | Action                                                       |
| ----------- | ------------------------------------------------------------ |
| `prep`      | [prep.md](references/prep.md) — prep for person, topic, or meeting |
| `oneone`    | [oneone.md](references/oneone.md) — 1:1 prep                 |
| `premtg`    | [premtg.md](references/premtg.md) — pre-meeting brief        |
| `mtgnotes`  | [mtgnotes.md](references/mtgnotes.md) — meeting debrief from transcript |
| `tickets`   | [tickets.md](references/tickets.md) — meeting → Linear tickets |
| `crm`       | [crm.md](references/crm.md) — meeting → CRM update           |
| `mtgmail`   | [mtgmail.md](references/mtgmail.md) — meeting → follow-up email |
| `catchup`   | [catchup.md](references/catchup.md) — missed-meeting catch-up |
| `clientlog` | [clientlog.md](references/clientlog.md) — client-scoped meeting log |

### People

| Shorthand   | Action                                                       |
| ----------- | ------------------------------------------------------------ |
| `relate`    | [relate.md](references/relate.md) — relationship refresh     |
| `newhire`   | [newhire.md](references/newhire.md) — new hire onboarding pack |

### Role packs

| Shorthand   | Action                                                       |
| ----------- | ------------------------------------------------------------ |
| `cos`       | [cos.md](references/cos.md) — Chief of Staff bundle          |
| `founder`   | [founder.md](references/founder.md) — founder bundle         |
| `sales`     | [sales.md](references/sales.md) — sales bundle               |
| `recruit`   | [recruit.md](references/recruit.md) — recruiting bundle      |
| `eng`       | [eng.md](references/eng.md) — PM / Eng bundle                |

### Monitoring

| Shorthand   | Action                                                       |
| ----------- | ------------------------------------------------------------ |
| `reg`       | [reg.md](references/reg.md) — regulatory / policy watch      |
| `news`      | [news.md](references/news.md) — competitor / customer news watch |
| `metric`    | [metric.md](references/metric.md) — metric threshold alert   |

If no argument is provided, show this help:

```
Debrief — your Chief of Staff.

Daily / weekly rituals:
  /debrief gm         Morning briefing on what matters today
  /debrief today      Three things that matter today
  /debrief week       Week priorities with reasoning
  /debrief eod        End-of-day wrap
  /debrief friwrap    Friday wrap / Monday plan
  /debrief deepwork   Deep-work block planner
  /debrief sayno      Meetings & asks to decline

Triage & inbox:
  /debrief triage     Prioritized list across channels with draft replies
  /debrief slacktri   Slack-only triage
  /debrief dms        Buried Slack DMs
  /debrief inbox      Email triage with drafts
  /debrief digest     Single-channel digest
  /debrief mentions   Unanswered @mentions

Follow-up & accountability:
  /debrief followup   Open items across channels
  /debrief promises   Commitments you made
  /debrief owed       Commitments owed to you
  /debrief stalled    Items untouched in N days
  /debrief thin       Items closed without ceremony
  /debrief glide      Glide-path check on initiatives

Status & reporting:
  /debrief recap      Written status update for a time range
  /debrief weekly     Weekly status update
  /debrief pulse      Company pulse
  /debrief projects   Epic / project tracker
  /debrief teamup     Team update draft
  /debrief exec       Exec brief
  /debrief board      Board / investor update

Meetings:
  /debrief prep       Prep for person, topic, or meeting
  /debrief oneone     1:1 prep
  /debrief premtg     Pre-meeting brief
  /debrief mtgnotes   Meeting debrief from transcript
  /debrief tickets    Meeting → Linear tickets
  /debrief crm        Meeting → CRM update
  /debrief mtgmail    Meeting → follow-up email
  /debrief catchup    Missed-meeting catch-up
  /debrief clientlog  Client-scoped meeting log

People:
  /debrief relate     Relationship refresh
  /debrief newhire    New hire onboarding pack

Role packs:
  /debrief cos        Chief of Staff bundle
  /debrief founder    Founder bundle
  /debrief sales      Sales bundle
  /debrief recruit    Recruiting bundle
  /debrief eng        PM / Eng bundle

Monitoring:
  /debrief reg        Regulatory / policy watch
  /debrief news       Competitor / customer news watch
  /debrief metric     Metric threshold alert

Get started: /debrief gm
```

The full arguments string is: $ARGUMENTS
