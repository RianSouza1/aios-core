
---
id: analyze-creative-fatigue
name: Analyze Creative Fatigue
agent: traffic-manager
description: Identify which creatives are dying and specifically WHY.
inputs:
  - name: campaign_data
    description: "Performance data for active ads"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "Paste the performance data for the ads you suspect are fatiguing."
    save_as: data

  - id: 2
    action: generate
    prompt: |
      Analyze the fatigue pattern for these ads: {{data}}
      
      For each flagging ad, diagnose the cause:
      1. **Click Fatigue:** High Frequency > 2.5 + CTR Dropping? -> *Needs new Visual.*
      2. **Conversion Fatigue:** CTR Stable + CPA Rising? -> *Needs new Offer/Lull in Aud.*
      3. **Blindness:** No clicks at all? -> *Needs new Hook.*
      
      **Output for Copywriter/Designer:** 
      "Ad X is suffering from [Cause]. Required Action: [Specific Instruction]."
---
