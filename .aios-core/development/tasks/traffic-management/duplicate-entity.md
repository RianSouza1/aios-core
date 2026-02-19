
---
id: duplicate-entity
name: Duplicate for Scaling
agent: traffic-manager
description: Scale campaigns by duplicating high-performing Ad Sets or Ads.
inputs:
  - name: entity_type
    description: "Campaign, Ad Set, or Ad"
    required: true
  - name: source_id
    description: "ID or Name of the entity to duplicate"
    required: true
  - name: strategy
    description: "Horizontal (New Audiences) or Vertical (Budget Increase)"
steps:
  - id: 1
    action: ask
    prompt: "What do you want to duplicate? (Campaign, Ad Set, or Ad) and what is its ID/Name?"
    save_as: source

  - id: 2
    action: ask
    prompt: "Is this for Horizontal Scaling (testing new audiences) or Vertical Scaling (same audience, higher budget)?"
    save_as: strategy

  - id: 3
    action: generate
    prompt: |
      Create a duplication plan for {{source}} using {{strategy}} strategy.
      
      1. **New Name Structure:** Define how the new entity should be named (e.g., "Original Name - Copy - [Date]").
      2. **Changes:** 
         - If Horizontal: Suggest 3 new interests/lookalikes to target.
         - If Vertical: Suggest the new budget (e.g., +20%).
      3. **Maintenance:** Rules for monitoring the new duplicate (e.g., "Kill if CPL > $X in 24h").
---
