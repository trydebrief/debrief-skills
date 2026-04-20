# /debrief tickets

Convert a customer or internal call into ready-to-file Linear tickets.

## Apps
- **Granola** — pull the meeting transcript.
- **Linear** — create the tickets after user confirmation.

## Step 1: Pull transcript
Use Granola to fetch the target meeting transcript.

## Step 2: Identify ticket-worthy items
Scan for: bug reports, feature requests, explicit "we should build X", commitments made to the customer. Ignore discussion that isn't actionable.

## Step 3: Draft tickets
For each, produce:
- **Title** (imperative, <80 chars)
- **Description** including the customer quote that motivated it
- **Suggested labels** (bug, feature, customer-request, etc.)
- **Suggested priority** with reasoning
- **Suggested team / project** in Linear (ask the user if ambiguous)

## Step 4: Confirm before filing
Show the full list. Ask which to create. Create in Linear one at a time after confirmation, so IDs come back cleanly.

## Guidelines
- Preserve the customer's language in the description — it's evidence.
- Don't collapse distinct requests into one ticket to save effort.
- If a request is vague, file it with a "needs-scoping" label rather than guessing the scope.
