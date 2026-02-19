
---
id: subject-lines
name: Generate Subject Lines
agent: email-strategist
description: Generate subject line variations for A/B testing.
inputs:
  - name: context
    description: "What is the email about?"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "Describe the email content and objective."
    save_as: context

  - id: 2
    action: generate
    prompt: |
      Generate 10 subject lines for: {{context}}
      
      Categories (at least 2 per category):
      1. **Curiosity:** Makes them NEED to open ("você viu o que aconteceu?")
      2. **Personal:** Feels like a friend texting ("preciso te contar uma coisa")
      3. **Shock:** Pattern interrupt ("para tudo.")
      4. **Question:** Asks something they can't ignore ("isso tá acontecendo com você também?")
      5. **Story:** Opens a narrative loop ("eu não acreditei quando vi...")
      
      Rules:
      - Lowercase preferred (feels casual).
      - Max 50 characters.
      - NEVER use: "🔥", "URGENTE", "IMPERDÍVEL", "EXCLUSIVO".
      - Must pass the "friend test": would a friend send this subject?
---
