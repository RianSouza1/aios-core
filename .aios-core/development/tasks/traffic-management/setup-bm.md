
---
id: setup-bm
name: Setup Business Manager
agent: traffic-manager
description: Checklist and guide for a robust Business Manager structure.
inputs:
  - name: contingency_level
    description: "Basic or Advanced (Backup assets)"
    required: false
steps:
  - id: 1
    action: ask
    prompt: "Do you need a Basic setup (Single Business) or Advanced Contingency (Multiple BMs/Profiles)?"
    save_as: level

  - id: 2
    action: generate
    prompt: |
      Generate a Setup Checklist for {{level}} level.
      
      1. **Structure:**
         - Master BM (Asset Holder: Pixels, Domains).
         - Advertiser BM (Account Holder: Runs ads).
      
      2. **Verification:**
         - Domain Verification (DNS TXT record).
         - Business Verification (Documents readiness).
      
      3. **Assets:**
         - Pixel/CAPI Setup.
         - Pages and Instagram linkage.
         - Payment Methods (Backup cards).
---
