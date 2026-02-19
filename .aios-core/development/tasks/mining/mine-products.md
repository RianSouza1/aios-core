
---
id: mine-products
name: Mine Winning Products
agent: miner
description: Find potential winning products or trends.
inputs:
  - name: niche
    description: "Health, Gadgets, Home, etc."
    required: true
steps:
  - id: 1
    action: ask
    prompt: "What niche or market are we hunting in?"
    save_as: niche

  - id: 2
    action: generate
    prompt: |
      Identify 3 Potential Winners in the {{niche}} niche.
      
      For each:
      1. **The Product:** Description / Name.
      2. **The Wow Factor:** Why does it stop the scroll?
      3. **Evidence:** Why do you think it's trending? (e.g., TikTok volume, Problem/Solution fit).
      4. **Angle:** How would we sell it?
---
