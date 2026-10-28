# Findings — synthetic demonstration only

## Dataset and methodology
- 150 generated lap records; 140 valid laps after excluding pit-out laps and implausible durations.
- Comparison uses within-session descriptive statistics; bootstrap 95% confidence intervals resample observed laps (5,000 replicates).
- Laps within a driver are serially correlated; naive bootstrap intervals are illustrative, not rigorous inference for race performance.

## Results
- Lowest average lap time: **Driver 01** (92.47 seconds); this is an outcome of the simulation parameters, not a real F1 result.
- Highest average lap time: **Driver 81** (93.63 seconds).
- Synthetic correlation of sector 2 time with full lap time: **0.96** (part-whole relationship, not a causal estimate).

## Limitations
- Synthetic drivers/teams; no results from an actual Grand Prix are asserted.
- Sector duration is arithmetically related to total lap time, so sector correlations are descriptive only.
- Track evolution, fuel load, traffic, tyre compounds, weather and session context are not controlled.
- Comparisons should not be interpreted as driver skill rankings.

## Next analysis using real OpenF1 data
- Fetch a historical session and verify field coverage and quality before comparing drivers.
- Match comparable stints or conditions, screen in/out laps and report sample sizes.
- Add robust time-series treatment or block bootstrap when producing inferential uncertainty.
