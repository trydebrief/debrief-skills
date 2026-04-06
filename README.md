# Debrief

Your local Chief of Staff. Morning briefings, prioritized triage, and custom commands — all your data stays on your device. Works with any agent that supports MCP and skills.

## Skills

- **[Debrief](skills/debrief/)** (`debrief`) — morning briefings, prioritized triage across email/Slack/calendar, custom commands, and interactive setup. Works fully offline with optional cloud sync.

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

### Claude.ai

1. Download this repository as a `.zip`.
2. Go to [https://claude.ai/customize/skills](https://claude.ai/customize/skills)
3. Click "+" > Create skill > Upload a skill
4. Select the `.zip` and you're done.

### Cursor / Windsurf

Add to your project's `.cursor/settings.json` or use the same skill format.

### Codex / Gemini CLI

Point your agent to `agents/AGENTS.md` which contains skill descriptions and paths.

### Other AI tools

Any AI tool that supports Markdown context can use the skills by pointing to:

- `agents/AGENTS.md` — skill index
- `skills/*/SKILL.md` — individual skill documentation

## Customization

For custom commands, cross-device config, and optional history sync, add the MCP server:

```bash
https://www.trydebrief.com/mcp
```

## Commands

| Command               | Description                                                 |
| --------------------- | ----------------------------------------------------------- |
| `/debrief gm`         | Morning briefing on what matters today                      |
| `/debrief triage`     | Prioritized messages across all channels with draft replies |
| `/debrief init`       | Set up or update your preferences                           |
| `/debrief new`        | Create a custom command                                     |
| `/debrief edit <cmd>` | Edit an existing command                                    |
| `/debrief <custom>`   | Run a custom command                                        |

## Optional: Connect your account

Debrief works fully offline. To customize commands and optionally keep history/sync across devices, connect a free account:

1. Sign up at [trydebrief.com](https://trydebrief.com)
2. Add the MCP server to your agent and authenticate: `https://www.trydebrief.com/mcp`

## Support

- [trydebrief.com](https://trydebrief.com)
- [GitHub Issues](https://github.com/trydebrief/debrief-skills/issues)

## License

[Apache-2.0](LICENSE)
