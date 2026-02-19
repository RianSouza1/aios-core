
---
id: generate-report
name: Analyze Campaign Performance
agent: traffic-manager
description: Generates a performance analysis report based on provided metrics.
inputs:
  - name: time_period
    description: "Period to analyze (e.g., Last 7 days, This Month)"
  - name: metrics_data
    description: "Raw data or key metrics (Paste CSV or type summary)"
steps:
  - id: 1
    action: ask
    prompt: "Please paste the campaign performance data (or describe key metrics like Spend, Impressions, Clicks, conversions, ROAS) for the period: {{time_period}}."
    save_as: data

  - id: 2
    action: generate
    prompt: |
      Analyze the following campaign data:
      {{data}}
      
      Provide a report covering:
      1. **Executive Summary:** Key wins and losses.
      2. **Metric Deep Dive:** CPM trends, CTR analysis, CPA vs Target.
      3. **Creative Performance:** Which ads are winning/losing?
      4. **Recommendations:** Actionable steps to improve performance (Scale, Kill, or Revive).
---
