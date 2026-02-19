
---
id: craft-offer
name: Craft Irresistible Offer
agent: offer-analyst
description: Structure a high-value offer with bonuses and guarantees.
inputs:
  - name: product
    description: "Core product name"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "What is the core product/service?"
    save_as: product

  - id: 2
    action: generate
    prompt: |
      Structure an Irresistible Offer for: {{product}}.
      
      Include:
      1. **The Transformation:** What is the "After" state?
      2. **Value Stack:** List components and assign a value to each.
      3. **Bonuses:** 3 bonuses that solve immediate next problems.
      4. **Scarcity/Urgency:** Reason to buy NOW.
      5. **Risk Reversal:** A bold guarantee.
---
