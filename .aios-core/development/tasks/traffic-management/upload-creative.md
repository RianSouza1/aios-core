
---
id: upload-creative
name: Manage Creatives
agent: traffic-manager
description: Upload creatives via Post ID (Dark Posts) or generate variations.
inputs:
  - name: action_type
    description: "Upload via ID or Generate Variations"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "Do you want to (1) Use an existing Post ID (Dark Post) or (2) Create variations of a winning creative?"
    save_as: user_choice

  - id: 2
    action: generate
    prompt: |
      Based on choice {{user_choice}}:
      
      **If (1) Post ID:**
      - Ask for the Post IDs.
      - Generate a plan to map these IDs to specific Ad Sets.
      
      **If (2) Variations:**
      - Ask for the details of the winning creative (Headline, Visual, Hook).
      - Suggest 3 variations:
        - Variation A: Change the Hook (first 3 seconds/text).
        - Variation B: Change the Format (e.g., Carousel vs Single Image).
        - Variation C: Change the Call to Action (CTA).
---
