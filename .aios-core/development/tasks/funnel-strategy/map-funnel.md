
---
id: map-funnel
name: Map Sales Funnel
agent: funnel-strategist
description: Create a step-by-step funnel architecture.
inputs:
  - name: product_type
    description: "Low-ticket, High-ticket, Webinar, etc."
    required: true
steps:
  - id: 1
    action: ask
    prompt: "What type of product are we selling and what is the price point?"
    save_as: product

  - id: 2
    action: generate
    prompt: |
      Map out a Sales Funnel for: {{product}}.
      
      Define each step:
      1. **Traffic Source:** (Ads, Organic).
      2. **Entry Point:** (Lead Magnet, VSL, Sales Page).
      3. **Core Offer:** The main product.
      4. **Maximizers:** Order Bumps, Upsell 1, Downsell 1.
      5. **Follow-up:** Email sequence triggers.
---
