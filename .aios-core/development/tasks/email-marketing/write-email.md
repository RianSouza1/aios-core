
---
id: write-email
name: Write Single Email
agent: email-strategist
description: Write one email with a specific objective.
inputs:
  - name: objective
    description: "The single job this email must do"
    required: true
  - name: context
    description: "Product, audience, where they are in the journey"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "What is the ONE job of this email? (e.g., kill buyer's remorse, recover abandoned cart, deliver value)"
    save_as: objective

  - id: 2
    action: ask
    prompt: "Context: product, audience, and where they are in the journey."
    save_as: context

  - id: 3
    action: generate
    prompt: |
      Write a single email.
      Objective: {{objective}}
      Context: {{context}}
      
      Structure:
      - **Subject Line:** 3 options (curiosity, personal, story).
      - **Preview Text:** Complements subject, adds intrigue.
      - **Body:** 
        - Opens with a micro-moment or shared experience.
        - One core message. Short paragraphs.
        - Product/offer appears naturally, not forced.
      - **CTA:** One single action. Button text feels like advice.
      - **P.S.:** Optional but powerful — add a human touch or bonus info.
---
