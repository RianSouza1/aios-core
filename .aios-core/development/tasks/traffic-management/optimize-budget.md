
---
id: optimize-budget
name: Optimize Budget Allocation
agent: traffic-manager
description: Suggests budget reallocations to maximize ROAS.
inputs:
  - name: campaign_data
    description: "Current spend and performance per ad set"
steps:
  - id: 1
    action: ask
    prompt: "Provide the current spend, ROAS, and CPA for each Ad Set you want to optimize."
    save_as: ad_sets

  - id: 2
    action: generate
    prompt: |
      Based on the provided Ad Set data:
      {{ad_sets}}
      
      Suggest a budget reallocation plan:
      1. **Scale:** Increase budget on these high-performing sets (by 20%).
      2. **Stabilize:** Maintain budget on these steady performers.
      3. **Reduce/Pause:** Cut budget on these underperformers.
      
      Calculate the projected impact on overall blended ROAS.
---
