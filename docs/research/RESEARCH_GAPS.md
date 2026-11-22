# Research Gaps — Signalbreakers Research

**Date:** 22 November 2026  
**Purpose:** Identify remaining research needs, open questions, and data gaps before proceeding to Phase 2 (Concept).

---

## 1. Completed Research

The following research areas have been addressed in Phase 1:

| Area | Document | Status |
|------|----------|--------|
| **Competitor analysis** | COMPETITOR_MATRIX.md | ✅ Complete — 15+ competitors analyzed across direct, adjacent, and narrative puzzle categories |
| **Player personas** | PLAYER_PERSONAS.md | ✅ Complete — Six personas defined with motivations, pain points, and design implications |
| **Platform requirements** | PLATFORM_REQUIREMENTS.md | ✅ Complete — Windows/Steam and Android/Google Play specs, costs, and submission requirements |
| **Business model** | BUSINESS_MODEL.md | ✅ Complete — Pricing, revenue projections, cost structure, and risk analysis |

---

## 2. Research Gaps

### Gap 1: Specific Steam Puzzle Game Wishlist Data

**What's missing:** Actual wishlist counts for comparable games at similar stages of development. This would help calibrate Signalbreakers' wishlist target (currently estimated at 5,000+).

**Why it matters:** Wishlist-to-purchase conversion rates and absolute wishlist numbers are the best leading indicators of Steam launch success. Without benchmark data, the 5,000-wishlist target is a reasonable guess but unverified.

**How to fill:**
- Use SteamDB or SteamCharts to find wishlist counts for games at similar release stages (Human Resource Machine, Hacknet, The Farmer Was Replaced)
- Check current wishlists for recently launched puzzle games on Steam
- **Priority:** Medium — can be done before Phase 2

### Gap 2: Android Educational Game Download/Conversion Benchmarks

**What's missing:** Average download numbers and conversion rates (free-to-paid) for educational puzzle games on Google Play in the STEM/coding category.

**Why it matters:** The base-case projection assumes 15,000 free downloads with 12% conversion ($9.99 IAP). Without benchmarks, this could be optimistic or conservative.

**How to fill:**
- Search for Google Play educational app market reports (App Annie/data.ai, Sensor Tower)
- Check similar apps' download counts and ratings on Google Play
- **Priority:** Medium — affects Android revenue confidence

### Gap 3: ADHD-Friendly Game Design Best Practices

**What's missing:** Specific design patterns proven to work for ADHD players in puzzle games. The persona "Curious Alex" and the general ADHD-friendly claim need more research backing.

**Why it matters:** ADHD-friendly design is a key differentiator but needs concrete implementation guidance (not just "short missions, optional timers").

**How to fill:**
- Research ADHD gaming studies and design guidelines
- Review existing games marketed as ADHD-friendly (e.g., Stardew Valley, Minecraft, Celeste's assist mode)
- **Priority:** Low — can be refined during Phase 3 (GDD)

### Gap 4: Cyberpunk Aesthetic Market Saturation

**What's missing:** How many cyberpunk-themed indie games have launched on Steam in the past 2–3 years, and how did they perform? Is there room for another?

**Why it matters:** Cyberpunk was heavily saturated around 2020 (Cyberpunk 2077 launch). Need to verify if the aesthetic still resonates with puzzle game audiences.

**How to fill:**
- Search Steam for "cyberpunk" tagged games released 2023–2026
- Check review scores and player counts for top results
- **Priority:** Medium — affects visual identity confidence

### Gap 5: Teacher/Classroom Adoption Barriers

**What's missing:** What specific barriers prevent teachers from adopting non-curriculum-aligned games? What would make Signalbreakers "classroom-ready"?

**Why it matters:** Teacher adoption (Persona 5) is a tertiary but valuable distribution channel. Understanding barriers helps prioritize teacher-facing features.

**How to fill:**
- Survey or interview 3–5 teachers about game adoption criteria
- Review existing educational game adoption studies
- **Priority:** Low — Phase 6 playtesting can validate assumptions

### Gap 6: Godot 4.x Android Build Size Benchmarks

**What's missing:** Actual APK build sizes for comparable 2D puzzle games exported from Godot 4.x to Android. This validates the 30–80 MB target.

**Why it matters:** Large APKs (>150 MB) face Google Play compression limits and may deter downloads on low-bandwidth connections.

**How to fill:**
- Check Google Play store listings for Godot-exported puzzle games
- Test build sizes during Phase 4 prototype
- **Priority:** Low — will be validated during technical prototyping

---

## 3. Open Decisions Requiring Research

| Decision | Dependencies | Recommended Timeline |
|----------|-------------|---------------------|
| **Final Steam price ($14.99 vs $19.99)** | Content volume at launch; competitor pricing analysis | Phase 2 (Concept) |
| **Android IAP price ($9.99 vs $12.99)** | Mobile price sensitivity research; competitor comparison | Phase 2 (Concept) |
| **Include Steam demo in MVP?** | Demo development effort assessment | Phase 3 (GDD) |
| **Target Android min SDK API 26 or 28?** | Device coverage vs. feature availability trade-off | Phase 4 (Prototype) |
| **Commission original music or use free assets?** | Budget vs. quality trade-off; timeline impact | Phase 5 (Vertical Slice) |

---

## 4. Assumptions to Validate in Playtesting

These assumptions from the research phase should be validated during Phase 6 playtesting:

1. **Players will engage with the cyberpunk narrative** even if they're primarily puzzle-focused
2. **Three difficulty modes are sufficient** — no player segment feels excluded
3. **Free introductory district on Android drives meaningful IAP conversions** (≥8%)
4. **"No ads, no loot boxes" is a genuine purchase driver** for the target audience
5. **ADHD-friendly features (short missions, undo, optional timers) are noticed and valued** by players

---

## 5. Recommended Next Research Actions

| Action | Priority | Effort | Owner |
|--------|----------|--------|-------|
| Check current wishlists for comparable Steam puzzle games | Medium | 1 hour | Researcher |
| Search Google Play for STEM puzzle app download benchmarks | Medium | 1 hour | Researcher |
| Survey 5–10 cyberpunk-themed indie games on Steam (2023–2026) | Medium | 2 hours | Researcher |
| Compile ADHD-friendly game design checklist | Low | 2 hours | Designer |
| Test Godot 4.x Android build sizes with sample project | Low | 1 hour | Developer |

---

## 6. Phase 1 Summary

Phase 1 research is **substantially complete**. The four core documents provide a strong foundation for Phase 2 (Concept):

- **Competitor landscape** is well-mapped with clear positioning opportunity
- **Six player personas** cover the full target audience spectrum
- **Platform requirements** are current as of November 2026, including Android API 36 deadline
- **Business model** shows low break-even (~90 Steam sales) with strong upside potential

The remaining gaps are refinements rather than blockers. Phase 2 can proceed with confidence while filling gaps in parallel.

---

*Phase 1 complete. Ready for PHASE 2: Concept.*
