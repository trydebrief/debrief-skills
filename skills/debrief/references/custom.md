# /debrief <custom>

The user is running a custom debrief command. The command name is `$ARGUMENTS[0]` and any additional arguments are in `$ARGUMENTS`.

## Resolution

1. If the Debrief MCP server is available, the command instructions should already have been fetched in the first step (see SKILL.md). Use those instructions.

2. If the MCP server is not available, check if a file exists at `${CLAUDE_SKILL_ROOT}/skills/debrief/references/$ARGUMENTS[0].md`. If it exists, read the file and follow its instructions.

3. If the command is not found in either location, tell the user:

```
Unknown command: $ARGUMENTS[0]

To create this command, run: /debrief new

Available built-in commands: gm, triage, new, edit
```

## Saving output

If the Debrief MCP server is available and the user's config has `syncEnabled`, call `save_output` with the command name, the full output after execution, and `context` set to everything after the command name in `$ARGUMENTS`. The command name is the first word in `$ARGUMENTS`.
