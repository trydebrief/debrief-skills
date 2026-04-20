# /debrief news

Named accounts only — competitor and customer news flagged to chat as news breaks.

## Apps
- **Slack** — post per-item alerts to the configured channel. Also check saved-for-later via `is:saved` for prior related items.

## Step 1: Configure
List of named competitors and named customers.

## Step 2: Pull
News mentions of each in the last 24h. Filter out low-signal sources (press releases the user doesn't care about, SEO spam).

## Step 3: Classify and route
- **Competitor product launch / pricing / leadership change** → flag high
- **Customer news (funding, layoffs, exec change, acquisition)** → flag to the account owner
- **Routine press** → skip

## Step 4: Post
Post one Slack message per item to the configured channel, with link + one-sentence "why this matters" for that named account.

## Guidelines
- Respect the "named only" constraint. Don't generalize to the category.
