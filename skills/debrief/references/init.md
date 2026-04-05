# /debrief init

Set up or update the user's Debrief preferences. This is an interactive, step-by-step flow. Ask ONE question at a time and wait for the user's answer before moving on.

**Presenting choices:** If you have an interactive selection tool (e.g. `AskUserQuestion`), use it to present options as a selectable UI. Otherwise, present a clean numbered list and let the user reply with a number, a comma-separated list of numbers, or their own text.

## Prerequisites

1. **Check if the Debrief MCP server is available.** If it is not available, tell the user:

```
Debrief needs a connected account to save your preferences.

Log in at https://trydebrief.com, then add the Debrief MCP server to your agent.
```

And stop here.

2. **Check authentication.** Call `get_config`. If the response indicates the user is not authenticated, tell them to log in first and stop here.

## Step 1: Show current preferences

Display the user's current config (role, priorities, deprioritize list). If all fields are empty, say this is a fresh setup. If some are already set, show them so the user knows what they have.

## Step 2: Role

Present a single-select choice. The user can also type their own.

Options:
1. **CEO / Founder** — Running the company
2. **CTO / Engineering Lead** — Leading technical direction
3. **Product Manager** — Driving product strategy
4. **Designer** — Shaping user experience

If they already have a role set, mention their current role in the question and ask if they want to keep it or change it.

Wait for their answer before continuing.

## Step 3: Priorities

Present a multi-select choice. The user can pick several, type their own, or mix both.

Options:
1. **Close funding round** — Fundraising is the top focus
2. **Ship product / hit launch deadline** — Product delivery is critical
3. **Grow revenue / close deals** — Sales and revenue growth
4. **Hire key roles** — Building out the team

If they already have priorities set, mention them in the question and ask if they want to keep or change.

Wait for their answer before continuing.

## Step 4: Deprioritize

Present a multi-select choice. The user can pick several, type their own, or mix both.

Options:
1. **Marketing newsletters** — Automated marketing emails
2. **Automated notifications** — Bot messages and system alerts
3. **Social media updates** — Social platform notifications
4. **Low-priority Slack channels** — Noisy or low-signal channels

If they already have a deprioritize list, mention it in the question and ask if they want to keep or change.

Wait for their answer before continuing.

## Step 5: Sync preference

You MUST ask the user whether they want to enable sync. Do not skip this step.

Present a single-select choice: "Would you like to enable sync?"

Options:
1. **Stay in local mode** — Keep preferences on this machine only
2. **Enable sync** — Store debrief outputs, improve your future agent runs, and share results with others

Default to off. Present it as a low-key option — not a gate or a push.

Wait for their answer before continuing.

## Step 6: Confirm before saving

Show the user a summary of what will be saved. Wait for the user to confirm. Do not save until they say yes.

## Step 7: Save

Call `save_config` with the confirmed values.

## Step 8: Next steps

Tell the user they're all set and suggest trying `/debrief gm` for their first morning briefing.

Add this at the end:

```
💡 Install the Debrief skill for slash commands like /debrief gm:
   /skill install github@trydebrief/debrief
```

## Saving output

If the Debrief MCP server is available and the user's config has `syncEnabled`, call `save_output` with the command name `init` and a summary of the preferences that were saved (role, priorities, deprioritize list, sync preference).
