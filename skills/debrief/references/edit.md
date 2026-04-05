# /debrief edit

The user wants to edit an existing debrief command. The command name is `$ARGUMENTS[1]`.

**Presenting choices:** If you have an interactive selection tool (e.g. `AskUserQuestion` in Claude Code), use it to present options as a selectable UI. Otherwise, present a clean numbered list and let the user reply with a number or their own text.

## Step 1: Resolve the command

If no command name was provided (`$ARGUMENTS[1]` is empty):

- If the Debrief MCP server is available, call `get_commands` to list all commands.
- If the MCP server is not available, list custom command files in `${CLAUDE_SKILL_ROOT}/skills/debrief/references/`.

Exclude built-in commands: `gm`, `triage`, `new`, `edit`, `custom`, `SKILL`.

Present the remaining commands as a single-select choice. Each option label should be the command name, with its first line of instructions as the description. Wait for the user's answer before continuing.

If a command name was provided, look it up via `get_commands` (MCP) or check for the local file.

## Step 2: Show and discuss

Show the user the current command instructions and ask what they'd like to change.

## Step 3: Update

Edit the command based on the user's feedback. Preserve the overall structure (heading, imperative instructions) and keep it consistent with other debrief commands.

Save the updated command using the MCP `add_or_update_command` tool if available. Otherwise, edit the local file.

## Step 4: Confirm

Tell the user the command has been updated and show them how to run it:

```
Updated: /debrief <command-name>

Run it with: /debrief <command-name>
```

## Saving output

If the Debrief MCP server is available and the user's config has `syncEnabled`, call `save_output` with the command name `edit` and a summary of what was changed (command name, what was modified).
