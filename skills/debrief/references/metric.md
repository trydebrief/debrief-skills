# /debrief metric

Ping when a number crosses a threshold.

## Apps
- **Slack** — post threshold alerts to the configured channel. Also check saved-for-later via `is:saved` for prior breach notifications.

## Step 1: Configure
User defines metric, source, and threshold (e.g., "daily signups < 50" or "error rate > 2%").

## Step 2: Check
On schedule or on-demand, pull current value from the source.

## Step 3: Alert
If threshold crossed, post to the configured Slack channel with:
- Current value
- Threshold
- Direction of move
- Link to dashboard for investigation

## Guidelines
- Include some historical context ("down from 80 yesterday") — a single number without trend is hard to act on.
- Respect cooldowns — don't re-alert on the same breach every run.
