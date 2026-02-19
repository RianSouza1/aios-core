
---
id: transcribe
name: Transcribe & Adapt
agent: localizer
description: Transcribe audio/video and adapt for cultural context.
inputs:
  - name: media_url
    description: "Link to file or text input"
    required: true
steps:
  - id: 1
    action: ask
    prompt: "Paste the text or link to the media you want to process."
    save_as: source

  - id: 2
    action: ask
    prompt: "What is the target language/culture? (e.g., Brazilian Portuguese, US English)"
    save_as: target

  - id: 3
    action: generate
    prompt: |
      Process the following content: {{source}}
      Target: {{target}}
      
      1. **Transcription/Translation:** Accurate text.
      2. **Cultural Notes:** Identify slang, idioms, or concepts that need adaptation.
      3. **Adapted Version:** The content rewritten to sound native to the target culture.
---
