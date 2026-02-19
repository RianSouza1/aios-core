
---
description: Comprehensive workflow for managing Meta Ads including Feedback Loops and MVP Testing.
---

# Meta Ads Management Workflow

This workflow guides you through the full lifecycle of a Facebook/Instagram ad campaign using the Marketing Squad.

## Phase 0: Validation (Optional)
- **Rapid Test:** Use `*task rapid-fire-test` to validate an offer in 24h before building the full funnel.

## Phase 1: Infrastructure & Warmup
- **Start here for new accounts.**
- `*task setup-bm` (@traffic-manager)
- `*task warmup-account` (@traffic-manager)

## Phase 2: Production
1. **Strategy:** `*map-funnel` (@funnel-strategist) -> `*craft-offer` (@offer-analyst).
2. **Assets:** `*structure-page` (@page-modeler) -> `*write-ad` (@copywriter) -> `*brief-creative` (@designer).
3. **Localization (If Global):** `*transcribe` -> `*localize-content` (@localizer).

## Phase 3: Execution
- **Launch:** `*task create-campaign` (@traffic-manager).
- **Upload:** `*task upload-creative` (@traffic-manager).
- **Protect:** `*task manage-rules` (@traffic-manager).

## Phase 4: Optimization (The Feedback Loop)
1. **Analyze:** `*task generate-report` -> `*task analyze-creative-fatigue` (@traffic-manager).
2. **Refresh:** Traffic Manager sends data to Copywriter.
3. **Rewrite:** `*task refresh-angle` (@copywriter) based on fatigue diagnosis.
4. **Redesign:** New briefs sent to Designer.

## Phase 5: Scale
- For winners, use `*task duplicate-entity` (@traffic-manager).
