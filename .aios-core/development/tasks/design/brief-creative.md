
---
id: brief-creative
name: Create Design Brief
agent: designer
description: Generate a structured brief for a visual creative.
inputs:
  - name: concept
    description: "Core idea or hook"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "Describe the core concept or hook for this creative."
    save_as: concept

  - id: 2
    action: generate
    prompt: |
      Create a Design Brief for: {{concept}}.
      
      Include:
      1. **Visual Headline:** Text overlay on the image/video.
      2. **Main Visual:** What should be the focal point? (Person, Product, Abstract).
      3. **Colors/Vibe:** e.g., "Urgent Red" or "Trustworthy Blue".
      4. **Format:** Stories (9:16) or Feed (4:5).
---
