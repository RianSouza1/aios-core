
---
id: refresh-angle
name: Refresh Ad Angle
agent: copywriter
description: Rewrite an ad angle based on specific fatigue feedback.
inputs:
  - name: feedback
    description: "The diagnosis from Traffic Manager"
    required: true
  - name: original_ad
    description: "The text of the dying ad"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "What was the feedback from the Traffic Manager? (e.g., Click Fatigue, Blindness)"
    save_as: feedback

  - id: 2
    action: ask
    prompt: "Paste the original ad copy here."
    save_as: original

  - id: 3
    action: generate
    prompt: |
      Based on the feedback "{{feedback}}", refresh this ad:
      
      Original:
      {{original}}
      
      **Strategy:**
      - If "Blindness": Write 3 completely new, shocking hooks locally relevant.
      - If "Click Fatigue": Keep the hook but change the body/story to a new angle.
      - If "Conversion Fatigue": Sharpen the CTA and add a new scarcity element.
---
