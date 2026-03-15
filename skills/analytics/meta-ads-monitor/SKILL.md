---
name: meta-ads-monitor
description: Analyze Meta Ads campaign performance and classify creatives/adsets into winner, test, or loser; recommend scale/pause/iterate actions. Use when reviewing CTR/CPC/CPA/frequency/spend data or deciding campaign actions.
---

# Meta Ads Monitor

## Inputs

- `campaign_data` (JSON/table with ad/adset metrics)
- `date_range`
- `geo` (optional)
- `objective` (optional)

## Process

1. Read key metrics for each ad/adset:
   - CTR
   - CPC
   - CPA
   - frequency
   - spend
2. Detect patterns:
   - high CTR + healthy CPA
   - rising frequency with falling CTR (fatigue)
   - high spend with weak conversion
3. Classify each line:
   - **WINNER**: CPA below target + CTR above baseline
   - **TEST**: mixed/unstable performance
   - **LOSER**: CPA above target + CTR below baseline
4. Recommend action:
   - `scale`
   - `test_more_creatives`
   - `pause`

## Output

Return a concise report with:

- top winners
- fatigued creatives
- losers to pause
- recommended next actions (with thresholds used)
