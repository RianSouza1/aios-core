
---
id: write-ad
name: Write Ad Copy
agent: copywriter
description: Write high-converting ad copy for specific platforms.
inputs:
  - name: product
    description: "Product/Service Name"
    required: true
  - name: platform
    description: "Facebook, TikTok, Email, etc."
    required: true
  - name: angle
    description: "The main hook or angle (e.g., Fear of Missing Out, gain, logic)"
steps:
  - id: 1
    action: ask
    prompt: "What is the product/service and who is the target audience?"
    save_as: product_info

  - id: 2
    action: ask
    prompt: "Which platform is this for? (Facebook, Instagram, TikTok, Email)"
    save_as: platform

  - id: 3
    action: generate
    prompt: |
      Write an ad for {{product_info}} on {{platform}}.
      
      Structure:
      1. **Hook:** Grab attention immediately found in the first line.
      2. **Body:** Agitate the problem and present the solution.
      3. **CTA:** Clear instruction on what to do next.
      
      Tone: Persuasive and native to the platform style.
---
