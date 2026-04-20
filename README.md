# Debrief

Debrief is a skillset for operators. Run `/debrief <shorthand>` to use within any agent.

Morning briefings, prioritized triage across email/Slack/calendar, meeting prep, status updates, and more — all your data stays on your device and between you and your agent.

Works with any agent that supports skills.

You can use Debrief from any device, on any schedule from [trydebrief.com](https://trydebrief.com).

## Installation

```bash
npx skills add trydebrief/debrief-skills
```

### Claude Code

```bash
# Add the marketplace
/plugin marketplace add https://github.com/trydebrief/debrief-skills

# Install the skill
/plugin install debrief@debrief-skills
```

### Claude Desktop / Claude Cowork

1. Download this repository as a `.zip`.
2. Customize > Add Plugin > Create Plugin > Upload Plugin

### Claude.ai

1. Go to [Releases](https://github.com/trydebrief/debrief-skills/releases/latest)
2. Download `debrief-skill.zip`
3. Go to https://claude.ai/customize/skills
4. Click "+" → Create skill → Upload a skill
5. Select the ZIP and you're done

### Cursor / Windsurf

Add to your project's `.cursor/settings.json` or use the same skill format.

### Codex / Gemini CLI

Point your agent to `agents/AGENTS.md` which contains skill descriptions and paths.

### Other AI tools

Any AI tool that supports Markdown context can use the skills by pointing to:

- `agents/AGENTS.md` — skill index
- `skills/*/SKILL.md` — individual skill documentation

## Commands

Run any of these with `/debrief <shorthand>`.

### Daily / weekly rituals

| Shorthand  | Description                               |
| ---------- | ----------------------------------------- |
| `gm`       | Morning briefing on what matters today    |
| `today`    | Three things that matter today            |
| `week`     | Week priorities with reasoning            |
| `eod`      | End-of-day wrap                           |
| `friwrap`  | Friday wrap / Monday plan                 |
| `deepwork` | Deep-work block planner                   |
| `sayno`    | Meetings & asks to decline                |

### Triage & inbox

| Shorthand  | Description                                       |
| ---------- | ------------------------------------------------- |
| `triage`   | Prioritized list across channels with draft replies |
| `slacktri` | Slack-only triage                                 |
| `dms`      | Buried Slack DMs                                  |
| `inbox`    | Email triage with drafts                          |
| `digest`   | Single-channel digest                             |
| `mentions` | Unanswered @mentions                              |

### Follow-up & accountability

| Shorthand  | Description                              |
| ---------- | ---------------------------------------- |
| `followup` | Open items across channels               |
| `promises` | Commitments you made                     |
| `owed`     | Commitments owed to you                  |
| `stalled`  | Items untouched in N days                |
| `thin`     | Items closed without ceremony            |
| `glide`    | Glide-path check on initiatives          |

### Status & reporting

| Shorthand  | Description                              |
| ---------- | ---------------------------------------- |
| `recap`    | Written status update for a time range   |
| `weekly`   | Weekly status update                     |
| `pulse`    | Company pulse                            |
| `projects` | Epic / project tracker                   |
| `teamup`   | Team update draft                        |
| `exec`     | Exec brief                               |
| `board`    | Board / investor update                  |

### Meetings

| Shorthand   | Description                              |
| ----------- | ---------------------------------------- |
| `prep`      | Prep for person, topic, or meeting       |
| `oneone`    | 1:1 prep                                 |
| `premtg`    | Pre-meeting brief                        |
| `mtgnotes`  | Meeting debrief from transcript          |
| `tickets`   | Meeting → Linear tickets                 |
| `crm`       | Meeting → CRM update                     |
| `mtgmail`   | Meeting → follow-up email                |
| `catchup`   | Missed-meeting catch-up                  |
| `clientlog` | Client-scoped meeting log                |

### People

| Shorthand | Description                  |
| --------- | ---------------------------- |
| `relate`  | Relationship refresh         |
| `newhire` | New hire onboarding pack     |

### Role packs

| Shorthand | Description              |
| --------- | ------------------------ |
| `cos`     | Chief of Staff bundle    |
| `founder` | Founder bundle           |
| `sales`   | Sales bundle             |
| `recruit` | Recruiting bundle        |
| `eng`     | PM / Eng bundle          |

### Monitoring

| Shorthand | Description                        |
| --------- | ---------------------------------- |
| `reg`     | Regulatory / policy watch          |
| `news`    | Competitor / customer news watch   |
| `metric`  | Metric threshold alert             |

### Setup & custom commands

| Shorthand       | Description                         |
| --------------- | ----------------------------------- |
| `init`          | Set up or update your preferences   |
| `new`           | Create a custom command             |
| `edit <cmd>`    | Edit an existing command            |
| `<custom>`      | Run a custom command                |

## Support

- [trydebrief.com](https://trydebrief.com)
- [GitHub Issues](https://github.com/trydebrief/debrief-skills/issues)

## License

[Apache-2.0](LICENSE)
