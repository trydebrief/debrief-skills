# /debrief digest

Daily or weekly summary of a specific noisy Slack channel.

## Apps
- **Slack** — read channel history and resolve user/thread links. Also check saved-for-later via `is:saved`.

## Step 1: Scope
Ask which channel and window (default: last 24h for daily, 7d for weekly). Use Slack `search_channels` to resolve the channel.

## Step 2: Summarize
Use Slack `read_channel` and `read_thread` to pull the window. Surface:
- **Decisions made** (with permalinks)
- **Questions asked** (and whether answered)
- **Notable threads** (high engagement or senior participation — look up user profiles for context)
- **Saved-for-later** — any `is:saved` items the user bookmarked in this channel
- **Noise** — count, don't enumerate

## Step 3: Present
Keep under 200 words for daily, 400 for weekly.

## Guidelines
- Preserve names — who said what matters in a digest.
- If nothing important happened, say so. Don't manufacture highlights.
