# /debrief sales

Stalled-deal alerts, post-call CRM updates, trigger-based outreach.

## Apps
- **HubSpot** — deal pipeline, stalled deals, account activity.
- **Granola** — recent sales call transcripts.
- **Gmail** — outreach drafts and prior threads with named accounts.

## Step 1: Stalled deals
Use HubSpot to pull deals with no activity in 14+ days. Group by stage. Flag any with close dates in the next 30 days.

## Step 2: Post-call updates
Use Granola to find meetings in the last 24h with external contacts. For each that doesn't yet have a HubSpot note, run the `/debrief crm` flow.

## Step 3: Trigger-based outreach
Scan named-account news (if a source is configured). For each trigger, use Gmail to draft an outreach note referencing it (save, never send).

## Step 4: Present
One list per section. Link everything (HubSpot deal URL, Gmail draft).

## Guidelines
- Don't send outreach automatically. All Gmail drafts.
- Stalled ≠ dead. Include a suggested next step, not just a flag.
