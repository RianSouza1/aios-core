
---
id: structure-page
name: Structure Landing Page
agent: page-modeler
description: Create a wireframe structure for a high-converting page.
inputs:
  - name: page_type
    description: "VSL Page, Long Form Sales Page, Opt-in, etc."
    required: true
steps:
  - id: 1
    action: ask
    prompt: "What type of page are we building? (e.g., VSL Page, Advertorial, Checkout)"
    save_as: type

  - id: 2
    action: generate
    prompt: |
      Create a Wireframe Structure for a {{type}}.
      
      For each section (Header, Hero, Body, Proof, CTA):
      - **Goal:** What needs to happen here?
      - **Content:** What text/visuals are needed?
      - **Layout:** Suggest layout (e.g., Split screen, Center aligned).
---
