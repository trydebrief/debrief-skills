# /debrief new

The user wants to create a new custom debrief command. Walk them through it interactively, one question at a time.

**Presenting choices:** If you have an interactive selection tool (e.g. `AskUserQuestion`), use it to present options as a selectable UI. Otherwise, present a clean numbered list and let the user reply with a number or their own text.

## Step 1: Command name

Ask the user what they want to call their command — what should they type after `/debrief` to run it?

Present a single-select choice with common starting points:

Options:
1. **standup** — Daily standup summary
2. **weekly** — Weekly recap or review
3. **followups** — Track pending follow-ups
4. **focus** — Deep work planning session

The user can type their own name instead. Wait for their answer before continuing.

## Step 2: What should it do?

Based on the command name, propose 3-4 suggestions for what the command could do. Each suggestion should describe a different take — what data it gathers, what output it produces, and which MCP tools it would use.

Present these as a single-select choice. The user can pick one, combine ideas, or describe something completely different. Wait for their answer before continuing.

## Step 3: Any tweaks?

Based on their answer, propose the command's tone, formatting, and focus as a short summary. Ask if they want to tweak anything or if it looks good.

Wait for their answer before continuing.

## Step 4: Generate the command prompt

Write a markdown prompt based on their answers. The prompt should:

- Start with a heading: `# /debrief <command-name>`
- Include clear instructions that Debrief will follow when the command is invoked
- Use any MCP tools that are appropriate for what the command needs to do
- Be written as direct instructions (imperative mood), matching the style of other debrief commands

## Step 5: Preview the command

Show the user the full generated prompt and ask:

```
Here's what your command will do — take a look and let me know if you'd like to tweak anything before I save it.
```

If they request changes, revise and preview again. Once they're happy, move on.

## Step 6: Save the command

Save the command using the MCP `add_or_update_command` tool if the Debrief MCP server is available. Pass the command `name` and the full markdown prompt as `instructions`.

If the MCP server is not available, save the file to `${CLAUDE_SKILL_ROOT}/skills/debrief/references/<command-name>.md`.

Never overwrite built-in commands (`gm`, `triage`, `new`, `edit`, `custom`, `SKILL`).

## Step 7: Confirm

Tell the user the command is ready and show them how to run it:

```
Command created: /debrief <command-name>

Run it now with: /debrief <command-name>
Edit it later with: /debrief edit <command-name>
```

## Saving output

If the Debrief MCP server is available and the user's config has `syncEnabled`, call `save_output` with the command name `new`, a summary of what was created (command name, description of what it does), and `context` set to everything after `new` in `$ARGUMENTS`.
