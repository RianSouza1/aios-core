
---
id: create-campaign
name: Create Meta Ads Campaign
agent: traffic-manager
description: Guided workflow to plan and structure a new Facebook/Instagram ad campaign.
inputs:
  - name: goal
    description: "Objective (e.g., Sales, Leads, Traffic)"
    required: true
  - name: budget
    description: "Daily or Lifetime budget"
    required: false
steps:
  - id: 1
    action: ask
    prompt: "What is the primary objective of this campaign? (e.g., Sales, Leads, Traffic, Awareness)"
    save_as: objective

  - id: 2
    action: ask
    prompt: "Who is your target audience? Describe demographics, interests, or behaviors."
    save_as: audience

  - id: 3
    action: ask
    prompt: "What is your daily or lifetime budget for this campaign?"
    save_as: budget

  - id: 4
    action: generate
    prompt: |
      Based on the following inputs:
      - Objective: {{objective}}
      - Audience: {{audience}}
      - Budget: {{budget}}
      
      Create a detailed campaign structure including:
      1. **Campaign Level:** Objective and Budget Optimization strategy (CBO/ABO).
      2. **Ad Set Level:** Audience definition, Placements (Automatic vs. Manual), and Optimization Goal.
      3. **Ad Level:** Suggest 3 ad angles (Hooks + Creative ideas + Copy outline).
      
      Format the output as a structured plan ready for implementation in Ads Manager.
---
