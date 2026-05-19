# Power BI Dashboard Design Brief

## The Dashboard's Job (one sentence)

A VP of Commercial at Novo Nordisk uses this dashboard to monitor where Mounjaro is gaining Decile 10 share fastest by state, so they can adjust monthly field force investment across the three geographic tiers (Stronghold Defense, Southern Battleground, and Withdrawn states).

## Key Decisions This Sentence Implies

- **Primary user:** VP of Commercial at Novo (or VP of Field Force Strategy)
- **Decision frequency:** Monthly field force review and quarterly strategic reallocation
- **Trigger for use:** Either a scheduled review, or an alert when share-shift in a priority state crosses a threshold
- **Action it drives:** Reallocate rep effort and KOL investment between geographies

## What This Dashboard Must Show

To support the decision, the dashboard must include:

1. State-level map of Decile 10 share dynamics (Novo vs Lilly)
2. State-level Mounjaro YoY growth in Decile 10
3. Tier classification for each state (Tier 1 / 2 / 3)
4. Drill-down: within each state, top-decile prescribers and their brand preferences
5. Trend view: month-over-month share-shift in priority states (when more granular data becomes available)

## What This Dashboard Will NOT Show

- Lower-decile (Decile 1-7) prescriber detail (these are not the strategic focus)
- Patient-level analysis (out of scope for CMS data)
- Specialty breakdowns at the headline level (the volume-driven finding makes specialty secondary)
- Overall market share dashboards (this is a defensive monitoring tool, not a market reporting tool)

## Connection to Strategic Recommendation

This dashboard operationalizes the three-tier geographic framework introduced in the strategic recommendation. Tier 1 states (Texas, California, Florida, New York) are where Novo defends strongholds; Tier 2 states (Tennessee, Georgia, Indiana, Alabama, Louisiana) are where Mounjaro is growing fastest and Novo must intervene; Tier 3 states (Massachusetts, Ohio, Michigan) are where Lilly has won and incremental investment is no longer ROI-positive. The dashboard's primary function is to track whether each state is staying in its tier or shifting between tiers — which would trigger reallocation decisions.
