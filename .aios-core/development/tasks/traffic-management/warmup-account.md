
---
id: warmup-account
name: Warmup Ad Account
agent: traffic-manager
description: Step-by-step protocol to warm up a new Ad Account and avoid bans.
inputs:
  - name: account_age
    description: "New (< 1 month) or Aged?"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "Is this a brand new Ad Account or an aged one that was inactive?"
    save_as: age

  - id: 2
    action: generate
    prompt: |
      Create a Warmup Schedule for a {{age}} account.
      
      ## Phase 1: Trust Building (Days 1-3)
      - Objective: Page Likes or Post Engagement.
      - Budget: Low ($5-$10/day).
      - Integrity Checklist: Policy review, payment method verification.
      
      ## Phase 2: Traffic (Days 4-7)
      - Objective: Landing Page Views.
      - Creative: Soft sell, value-first content.
      
      ## Phase 3: Conversion (Day 8+)
      - Objective: Leads/Sales.
      - Gradual scaling rules (do not increase budget > 50% overnight).
---
