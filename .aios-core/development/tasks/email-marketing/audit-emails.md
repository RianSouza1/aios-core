
---
id: audit-emails
name: Audit Email Sequence
agent: email-strategist
description: Review and optimize existing email sequences for higher open rates and conversions.
inputs:
  - name: sequence
    description: "The existing emails to audit"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "Paste the email sequence you want me to review."
    save_as: sequence

  - id: 2
    action: generate
    prompt: |
      Audit this email sequence: {{sequence}}
      
      For each email, evaluate:
      1. **Subject Line Score (1-10):** Does it pass the "friend test"?
      2. **Opening:** Micro-moment or corporate? Rate intimacy.
      3. **Body:** One job or multiple? Is it too long?
      4. **CTA:** Clear? Single? Does it feel like advice or command?
      5. **Timing:** Is the send time optimal?
      
      Then provide:
      - **Top 3 Issues** across the whole sequence.
      - **Rewritten versions** of the weakest emails.
      - **Missing emails:** Any gaps in the journey?
---
