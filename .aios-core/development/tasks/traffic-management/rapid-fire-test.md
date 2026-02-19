
---
id: rapid-fire-test
name: Rapid Fire Testing (MVP)
agent: traffic-manager
description: Launch a low-budget test to validate an Offer + Creative pair in 24h.
inputs:
  - name: offer_url
    description: "Direct link to Checkout or Product Page"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "What is the Offer URL?"
    save_as: url

  - id: 2
    action: generate
    prompt: |
      Create a Rapid Fire Test Structure.
      
      1. **Campaign:** ABO (Ad Budget Optimization).
      2. **Ad Sets:** 3 Broad/Interest-based sets.
      3. **Budget:** $10/day per set.
      4. **Ads:** 1 Creative Variation per set (Total 3 variations).
      5. **Rules:** 
         - Kill if Spend > $5 and 0 Clicks.
         - Kill if Spend > $15 and 0 Add-to-Carts.
         - Scale if ROAS > 2.0 within 24h.
---
