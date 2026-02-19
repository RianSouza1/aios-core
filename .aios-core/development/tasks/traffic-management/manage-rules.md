
---
id: manage-rules
name: Setup Automated Rules
agent: traffic-manager
description: Create logic for automated budget optimization and safeguards.
inputs:
  - name: risk_level
    description: "Conservative, Balanced, or Aggressive"
    required: false
steps:
  - id: 1
    action: ask
    prompt: "What is your risk tolerance for these rules? (Conservative, Balanced, Aggressive)"
    save_as: risk

  - id: 2
    action: generate
    prompt: |
      Generate a set of Automated Rules for Meta Ads based on {{risk}} profile.
      
      Include:
      1. **Stop Loss (Safety):** specific condition to pause ads (e.g., "Spend > 2x CPA and 0 Conversions").
      2. **Scale Up (Winners):** condition to increase budget (e.g., "ROAS > 3.0, increase by 20%").
      3. **Revive/Re-test:** conditions for delayed attribution (optional).
      
      Format as a table: Rule Name | Condition | Action | Timeframe.
---
