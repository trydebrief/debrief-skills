# /debrief reg

Daily pull of regulatory and policy changes relevant to the user's domain, tagged low/med/high.

## Apps
- **Slack** — post the digest to a configured channel. Also check saved-for-later via `is:saved` for prior items the user bookmarked.

## Step 1: Configure scope
Jurisdictions and topics the user cares about (set once, stored in user config).

## Step 2: Pull
From configured sources (RSS, gov sites, user-specified). Last 24h.

## Step 3: Classify
- **High** — directly affects product, operations, or compliance
- **Medium** — affects industry broadly, worth tracking
- **Low** — peripheral, FYI only

## Step 4: Present
Post high + medium to the configured Slack channel. Low items: count only, with link to full list.

## Guidelines
- Don't over-classify as high. Erosion of the "high" signal is the failure mode here.
- Always link primary sources, not commentary.
