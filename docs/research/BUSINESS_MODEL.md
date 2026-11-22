# Business Model — Signalbreakers Research

**Date:** 22 November 2026  
**Purpose:** Define monetization strategy, pricing scenarios, cost structure, and revenue projections for Signalbreakers: The Neon Protocol.

---

## 1. Revenue Models by Platform

### 1.1 Windows (Steam) — Premium One-Time Purchase

| Element | Detail |
|---------|--------|
| **Model** | One-time purchase, no subscriptions, no IAPs, no ads |
| **Target price** | $14.99–$19.99 USD (final pricing depends on content volume at launch) |
| **Steam demo** | Free introductory district (~3 missions) to drive wishlists and conversions |
| **Sales frequency** | Steam seasonal sales (Summer, Winter, Spring, Autumn) — typically 20–50% discounts |
| **Revenue share** | 70% to developer after Steam's 30% cut (standard tier) |

### 1.2 Android (Google Play) — Freemium with One-Time Unlock

| Element | Detail |
|---------|--------|
| **Model** | Free introductory district + one-time full-game unlock IAP |
| **Free content** | District 1 (Token Town) — ~5 missions, teaches core mechanics |
| **Unlock price** | $9.99–$12.99 USD (lower than Steam to account for mobile price sensitivity) |
| **Ads** | Optional: non-intrusive rewarded ads (watch ad for hint) in free district only; no interstitials during gameplay |
| **Google Play revenue share** | 85% to developer on first $10M/year per developer (reduced rate since 2023) |

### 1.3 Why This Hybrid Model?

| Factor | Steam Premium | Android Freemium | Rationale |
|--------|---------------|------------------|-----------|
| **Audience expectation** | PC gamers expect premium pricing | Mobile users expect free-to-try | Matches platform norms |
| **Acquisition cost** | Driven by wishlists + store visibility | Driven by organic search + free trial | Free district lowers mobile barrier |
| **Price sensitivity** | Lower ($14.99–$19.99 acceptable) | Higher (under $10 IAP preferred) | Reflects actual consumer behavior |
| **Development cost** | Single codebase in Godot | Same codebase, touch UI layer | Minimal incremental cost |

---

## 2. Cost Structure

### 2.1 One-Time Development Costs

| Category | Estimated Range | Notes |
|----------|-----------------|-------|
| **Engine** | $0 | Godot 4.x — MIT license, no royalties |
| **Development tools** | $0–$200 | VS Code (free), GIMP/Krita (free), Audacity (free); optional paid tools |
| **Music/SFX licensing** | $0–$500 | Free assets (Kenney.nl, OpenGameArt) or commissioned original score |
| **Art assets** | $0–$1,000 | Pixel art can be self-created; external artist for key visuals |
| **Steam developer fee** | $100 | Per-game fee, recoupable after $1,000 revenue |
| **Google Play developer fee** | $25 | One-time, per account |
| **Domain + privacy policy host** | $10–$20/year | Required for Google Play |
| **Total one-time** | **$135–$1,845** | Lean approach: ~$200; polished approach: ~$1,800 |

### 2.2 Ongoing Annual Costs

| Category | Estimated Range | Notes |
|----------|-----------------|-------|
| **Domain renewal** | $10–$20/year | Privacy policy hosting |
| **Analytics service** | $0–$50/month | Firebase (free tier) or self-hosted; optional paid analytics |
| **Customer support** | 2–4 hours/month | Email + Steam community replies; ~$50–$100/month if outsourced |
| **Bug fixes / updates** | 4–8 hours/month | Post-launch patches, compatibility updates |
| **Total annual** | **$700–$2,000/year** | Lean solo dev: ~$700; with support outsourcing: ~$2,000 |

### 2.3 Per-Unit Costs

| Cost | Amount | Notes |
|------|--------|-------|
| **Steam payment processing** | ~33% of sale price | Steam 30% + payment fees |
| **Google Play payment processing** | ~15% of IAP price | Google's reduced rate for first $10M/year |
| **Refund rate (estimated)** | 5–10% | Steam refund rate averages ~5%; Google Play varies by region |

---

## 3. Revenue Projections

### 3.1 Assumptions

| Assumption | Conservative | Base Case | Optimistic |
|------------|-------------|-----------|------------|
| **Steam units (Year 1)** | 2,000 | 5,000 | 15,000 |
| **Steam avg. price** | $12.99 (with sales) | $14.99 | $16.99 |
| **Android downloads (Year 1)** | 5,000 | 15,000 | 50,000 |
| **Android conversion rate** | 8% | 12% | 18% |
| **Android unlock price** | $7.99 | $9.99 | $11.99 |
| **Steam revenue share** | 67% (after fees) | 67% | 67% |
| **Google Play revenue share** | 82% (after fees) | 82% | 82% |

### 3.2 Year 1 Revenue Scenarios

| Scenario | Steam Revenue | Android Revenue | Total Gross | Net (after platform cuts) |
|----------|--------------|-----------------|-------------|---------------------------|
| **Conservative** | $2,000 × $12.99 × 67% = **$17,400** | 5,000 × 8% × $7.99 × 82% = **$2,620** | **$20,020** | **~$20,020** (Steam + Google take their cuts) |
| **Base Case** | 5,000 × $14.99 × 67% = **$50,200** | 15,000 × 12% × $9.99 × 82% = **$14,730** | **$64,930** | **~$64,930** |
| **Optimistic** | 15,000 × $16.99 × 67% = **$170,800** | 50,000 × 18% × $11.99 × 82% = **$88,800** | **$259,600** | **~$259,600** |

### 3.3 Break-Even Analysis

| Metric | Value |
|--------|-------|
| **Total Year 1 costs (lean)** | ~$200 one-time + $700 ongoing = **$900** |
| **Break-even units (Steam only, base price)** | $900 / ($14.99 × 67%) = **~90 Steam sales** |
| **Break-even (Android only, base IAP)** | $900 / ($9.99 × 82% × 12% conversion) = **~915 free downloads** |

**Conclusion:** Break-even is achievable with very few sales — the financial risk is low even in the conservative scenario.

---

## 4. Pricing Strategy

### 4.1 Launch Pricing

| Platform | Price | Rationale |
|----------|-------|-----------|
| **Steam (full game)** | $14.99 USD | Competitive with Human Resource Machine ($9.99) and The Farmer Was Replaced ($7.99), but justified by 8 districts + narrative |
| **Android (unlock IAP)** | $9.99 USD | Lower than Steam to reflect mobile price sensitivity; still above typical mobile game IAPs ($0.99–$4.99) |

### 4.2 Post-Launch Pricing Adjustments

| Event | Price Change | Duration |
|-------|-------------|----------|
| **Steam launch week** | $14.99 (full price) | First 7 days |
| **First Steam sale** | $10.49 (30% off) | 5–7 days |
| **Standard sale discount** | 20–30% off | Regular seasonal sales |
| **Deep sale (Winter)** | 50% off | Annual major sale |
| **Android IAP price** | Stable at $9.99; occasional promo to $6.99 | Rare, tied to Steam sales |

### 4.3 Price Justification

- **8 districts × ~5 missions each = ~40 missions** of content (vs. 12–20 for Human Resource Machine)
- **Narrative-driven** with cyberpunk aesthetic — higher production value than most educational games
- **Three difficulty modes** extend replayability
- **Cross-platform** — one purchase covers both Windows and Android (if linked accounts in future)

---

## 5. Monetization Risks and Mitigations

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| **Steam sales cannibalize full-price sales** | High | Medium | Steam sales drive wishlists and long-tail revenue; full price is only ~30% of the year |
| **Android conversion rate below 10%** | Medium | Medium | Improve free district quality; add "unlock full game" prompt after mission completion |
| **Refund rate exceeds 10% on Steam** | Low | Low | Free demo reduces refunds; Steam's 2-hour/14-day refund policy is standard |
| **Google Play reduces developer revenue share above $10M** | Medium (long-term) | Low | At $10M/year, rate drops to 85% → still very favorable vs. historical 70% |
| **Price sensitivity in non-US markets** | High | Medium | Steam regional pricing; Google Play local currency IAPs |

---

## 6. Additional Revenue Streams (Post-MVP)

| Stream | Timing | Estimated Revenue | Notes |
|--------|--------|-------------------|-------|
| **Steam DLC — additional districts** | Year 2+ | $4.99–$7.99 per DLC | Expand story/world; proven model for puzzle games |
| **Google Play Pass inclusion** | Post-launch | Variable royalty | Provides exposure + subscription revenue share |
| **School/district licensing** | Year 1+ | $5/student/year | Bulk licenses for classroom use; requires teacher resources |
| **Merchandise (post-success)** | Year 2+ | Variable | Stickers, posters, art book — only if player base justifies |
| **Console ports (Switch)** | Year 2+ | $14.99 | Godot supports Switch export; Nintendo eShop distribution |

---

## 7. Key Financial Unknowns

| Unknown | Why It Matters | How to Reduce Uncertainty |
|---------|---------------|--------------------------|
| **Actual Steam wishlist-to-purchase conversion** | Drives revenue projection accuracy | Track wishlists from demo launch; industry benchmark is 10–30% for well-marketed indie games |
| **Android free-district drop-off rate** | Determines how many users see the IAP prompt | A/B test IAP placement (after mission completion vs. district end) |
| **Player retention across districts** | Impacts perceived value and refund rates | Implement in-game analytics; track % of players completing each district |
| **Steam sale performance vs. full-price periods** | Informs pricing calendar | Monitor first 2–3 sales cycles; adjust discount depth/frequency accordingly |

---

## 8. Sources and Verification Dates

| Source | URL | Verified |
|--------|-----|----------|
| Google Play Reduced Revenue Share (15% developer) | https://support.google.com/googleplay/android-developer/answer/7093603 | 22 Nov 2026 |
| Steam Revenue Share | https://partner.steamgames.com/doc/store/discounts | 22 Nov 2026 |
| Google Play Store Statistics (42matters) | https://42matters.com/google-play-statistics-and-trends | 22 Nov 2026 |
| Education App Market Data | https://www.educationalappstore.com/blog/education-app-market | 22 Nov 2026 |

---

*Next: RESEARCH_GAPS.md — Identify remaining research needs and open questions before Phase 2 (Concept).*
