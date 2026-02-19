
---
id: write-sequence
name: Write Email Sequence
agent: email-strategist
description: Create a full email sequence for a specific goal.
inputs:
  - name: type
    description: "welcome, cart-abandonment, launch, nurture, post-purchase, win-back"
    required: true
  - name: product
    description: "Product or brand name"
    required: true
  - name: audience
    description: "Who receives these emails?"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "What type of sequence? (welcome, cart-abandonment, launch, nurture, post-purchase, win-back)"
    save_as: type

  - id: 2
    action: ask
    prompt: "What is the product/brand and who is the audience?"
    save_as: context

  - id: 3
    action: generate
    prompt: |
      Create a {{type}} email sequence for {{context}}.
      
      Rules:
      - Each email must have: Subject Line, Preview Text, Body, CTA.
      - Subject lines must feel like a DM from a friend. Never corporate.
      - Apply the Deep Persuasion Pattern: micro-moment openers, vulnerability, product appears late.
      - One email = one job. Never mix objectives.
      - Include send timing for each email.
---
