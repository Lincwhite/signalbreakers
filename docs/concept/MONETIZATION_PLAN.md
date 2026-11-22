# Monetization Plan — Signalbreakers: The Neon Protocol

**Version:** 1.0 (Phase 3)  
**Date:** 23 November 2026  
**Purpose:** Expanded monetization strategy with pricing calendar, DLC roadmap, launch marketing budget, and revenue projections by platform. Builds on Phase 1 Business Model research.

---

## TABLE OF CONTENTS

1. Revenue Models by Platform
2. Pricing Strategy & Calendar
3. Cost Structure (Detailed)
4. Revenue Projections (Conservative/Base/Optimistic)
5. DLC Roadmap
6. Launch Marketing Budget
7. Monetization Risks and Mitigations
8. Key Financial Unknowns

---

## 1. REVENUE MODELS BY PLATFORM

### Windows (Steam) — Premium One-Time Purchase

| Element | Detail | Rationale |
|---------|--------|-----------|
| **Model** | One-time purchase, no subscriptions, no IAPs, no ads | Matches player expectations for PC puzzle games; contrasts with mobile freemium fatigue |
| **Target price** | $14.99 USD at launch | Competitive with Human Resource Machine ($9.99) and The Farmer Was Replaced ($7.99), justified by 8 districts + narrative depth |
| **Steam demo** | Free introductory district (~3 missions: D1M01–D1M03) to drive wishlists and conversions | Puzzle games benefit from demos; Steam data shows demos increase conversion by 20–40% |
| **Sales frequency** | Steam seasonal sales (Summer, Winter, Spring, Autumn) — typically 20–50% discounts | Standard indie game practice; builds long-tail revenue |
| **Revenue share** | 70% to developer after Steam's 30% cut (standard tier); drops to 75%/80% after $10M/$50M lifetime | Industry standard; favorable for solo/small team |

### Android (Google Play) — Freemium with One-Time Unlock

| Element | Detail | Rationale |
|---------|--------|-----------|
| **Model** | Free introductory district + one-time full-game unlock IAP | Matches mobile player expectations; free district lowers barrier to entry |
| **Free content** | District 1 (Token Town) — ~5 missions, teaches core mechanics (loops) | Sufficient to demonstrate value without giving away too much |
| **Unlock price** | $9.99 USD (lower than Steam to account for mobile price sensitivity) | Mobile players expect lower prices; $9.99 is above typical IAPs ($0.99–$4.99) but below Steam premium |
| **Ads** | Optional: non-intrusive rewarded ads (watch ad for hint) in free district only; no interstitials during gameplay | Rewarded ads have 80%+ acceptance rate; no interstitials preserves gameplay flow |
| **Google Play revenue share** | 85% to developer on first $10M/year per developer (reduced rate since 2023) | Favorable vs. historical 70%; still very good after $10M threshold |

### Why This Hybrid Model Works

| Factor | Steam Premium | Android Freemium | Rationale |
|--------|---------------|------------------|-----------|
| **Audience expectation** | PC gamers expect premium pricing | Mobile users expect free-to-try | Matches platform norms; no surprise at checkout |
| **Acquisition cost** | Driven by wishlists + store visibility | Driven by organic search + free trial | Free district lowers mobile barrier; demo drives Steam wishlists |
| **Price sensitivity** | Lower ($14.99 acceptable) | Higher (under $10 IAP preferred) | Reflects actual consumer behavior on each platform |
| **Development cost** | Single codebase in Godot | Same codebase, touch UI layer | Minimal incremental cost for dual-platform release |

---

## 2. PRICING STRATEGY & CALENDAR

### Launch Pricing

| Platform | Price | Rationale |
|----------|-------|-----------|
| **Steam (full game)** | $14.99 USD | Competitive with Human Resource Machine ($9.99) and The Farmer Was Replaced ($7.99), but justified by 8 districts + narrative |
| **Android (unlock IAP)** | $9.99 USD | Lower than Steam to reflect mobile price sensitivity; still above typical mobile game IAPs ($0.99–$4.99) |

### Post-Launch Pricing Adjustments

| Event | Price Change | Duration | Notes |
|-------|-------------|----------|-------|
| **Steam launch week** | $14.99 (full price) | First 7 days | Standard practice; no launch discount |
| **First Steam sale** | $10.49 (30% off) | 5–7 days | Occurs during first seasonal sale (~2–3 months post-launch) |
| **Standard sale discount** | 20–30% off | Regular seasonal sales | Never deeper than 30% for first year; preserves perceived value |
| **Deep sale (Winter)** | 50% off | Annual major sale | Once per year; drives volume but not frequency |
| **Android IAP price** | Stable at $9.99; occasional promo to $6.99 | Rare, tied to Steam sales | Android price rarely changes; promos coincide with Steam sales for cross-platform awareness |

### Price Justification

- **8 districts × ~5 missions each = ~40 missions** of content (vs. 12–20 for Human Resource Machine)
- **Narrative-driven** with cyberpunk aesthetic — higher production value than most educational games
- **Three difficulty modes** extend replayability
- **Cross-platform** — one purchase covers both Windows and Android (if linked accounts in future)

---

## 3. COST STRUCTURE (DETAILED)

### One-Time Development Costs

| Category | Estimated Range | Notes |
|----------|-----------------|-------|
| **Engine** | $0 | Godot 4.x — MIT license, no royalties |
| **Development tools** | $0–$200 | VS Code (free), GIMP/Krita (free), Audacity (free); optional paid tools like Aseprite ($25) |
| **Music/SFX licensing** | $0–$500 | Free assets (Kenney.nl, OpenGameArt) or commissioned original score (~$300–$500 for 8 district themes) |
| **Art assets** | $0–$1,000 | Pixel art can be self-created; external artist for key visuals ($500–$1,000 if needed) |
| **Steam developer fee** | $100 | Per-game fee, recoupable after $1,000 revenue |
| **Google Play developer fee** | $25 | One-time, per account |
| **Domain + privacy policy host** | $10–$20/year | Required for Google Play; signalbreakers.game or similar |
| **Voice acting** | $200–$500 | ~50–75 lines; indie voice actors charge $3–$8 per line |
| **Total one-time** | **$335–$2,445** | Lean approach: ~$335 (self-created assets); polished approach: ~$2,400 |

### Ongoing Annual Costs

| Category | Estimated Range | Notes |
|----------|-----------------|-------|
| **Domain renewal** | $10–$20/year | Privacy policy hosting |
| **Analytics service** | $0–$50/month | Firebase (free tier) or self-hosted; optional paid analytics (~$30/month for advanced features) |
| **Customer support** | 2–4 hours/month | Email + Steam community replies; ~$50–$100/month if outsourced |
| **Bug fixes / updates** | 4–8 hours/month | Post-launch patches, compatibility updates |
| **Marketing (ongoing)** | $100–$300/month | Social media ads, influencer partnerships, press outreach |
| **Total annual** | **$1,320–$4,160/year** | Lean solo dev: ~$1,320; with support outsourcing + marketing: ~$4,160 |

### Per-Unit Costs

| Cost | Amount | Notes |
|------|--------|-------|
| **Steam payment processing** | ~33% of sale price | Steam 30% + payment fees (~3%) |
| **Google Play payment processing** | ~15% of IAP price | Google's reduced rate for first $10M/year |
| **Refund rate (estimated)** | 5–10% | Steam refund rate averages ~5%; Google Play varies by region |

---

## 4. REVENUE PROJECTIONS (CONSERVATIVE/BASE/OPTIMISTIC)

### Assumptions

| Assumption | Conservative | Base Case | Optimistic |
|------------|-------------|-----------|------------|
| **Steam units (Year 1)** | 2,000 | 5,000 | 15,000 |
| **Steam avg. price** | $12.99 (with sales) | $14.99 | $16.99 |
| **Android downloads (Year 1)** | 5,000 | 15,000 | 50,000 |
| **Android conversion rate** | 8% | 12% | 18% |
| **Android unlock price** | $7.99 | $9.99 | $11.99 |
| **Steam revenue share** | 67% (after fees) | 67% | 67% |
| **Google Play revenue share** | 82% (after fees) | 82% | 82% |

### Year 1 Revenue Scenarios

| Scenario | Steam Revenue | Android Revenue | Total Gross | Net (after platform cuts) |
|----------|--------------|-----------------|-------------|---------------------------|
| **Conservative** | 2,000 × $12.99 × 67% = **$17,400** | 5,000 × 8% × $7.99 × 82% = **$2,620** | **$20,020** | **~$20,020** (Steam + Google take their cuts) |
| **Base Case** | 5,000 × $14.99 × 67% = **$50,200** | 15,000 × 12% × $9.99 × 82% = **$14,730** | **$64,930** | **~$64,930** |
| **Optimistic** | 15,000 × $16.99 × 67% = **$170,800** | 50,000 × 18% × $11.99 × 82% = **$88,800** | **$259,600** | **~$259,600** |

### Break-Even Analysis

| Metric | Value |
|--------|-------|
| **Total Year 1 costs (lean)** | ~$335 one-time + $1,320 ongoing = **$1,655** |
| **Break-even units (Steam only, base price)** | $1,655 / ($14.99 × 67%) = **~165 Steam sales** |
| **Break-even (Android only, base IAP)** | $1,655 / ($9.99 × 82% × 12% conversion) = **~1,685 free downloads** |

**Conclusion:** Break-even is achievable with very few sales — the financial risk is low even in the conservative scenario. Base case projects ~$63K net profit in Year 1.

---

## 5. DLC ROADMAP

| DLC | Timing | Price | Content | Estimated Development Cost |
|-----|--------|-------|---------|---------------------------|
| **District 9: The Undercity** | Year 2, Q1 | $4.99 | New district teaching graph theory and pathfinding; expands LUMA-9 backstory | ~$300–$500 (art + design) |
| **District 10: Signal Void** | Year 2, Q3 | $4.99 | Final district with advanced concepts (state machines, finite automata); secret ending variant | ~$400–$600 |
| **Soundtrack Pack** | Year 1, Q4 | $2.99 | All 8 district themes in high-quality Ogg/FLAC format; bonus unreleased tracks | ~$50 (compilation + mastering) |
| **Art Book** | Year 2, Q2 | $6.99 | Digital PDF with concept art, character designs, district maps, developer commentary | ~$100 (layout + editing) |

### DLC Pricing Strategy

- **District DLCs:** $4.99 each; bundle both for $7.99 (save 20%)
- **Soundtrack Pack:** $2.99; included free with pre-order of full game at launch
- **Art Book:** $6.99 digital only; physical version ($19.99) via Kickstarter in Year 3

### DLC Impact on Revenue

| Scenario | Year 1 (Base Game) | Year 2 (DLC + Base Game Sales) | Total 2-Year Revenue |
|----------|-------------------|-------------------------------|---------------------|
| **Conservative** | $20,020 | $15,000 (base game decline) + $3,000 (DLC) = $18,000 | **$38,020** |
| **Base Case** | $64,930 | $40,000 (base game decline) + $10,000 (DLC) = $50,000 | **$114,930** |
| **Optimistic** | $259,600 | $120,000 (base game decline) + $35,000 (DLC) = $155,000 | **$414,600** |

---

## 6. LAUNCH MARKETING BUDGET

### Pre-Launch (Months -3 to 0)

| Activity | Cost | Expected Outcome |
|----------|------|------------------|
| **Steam page launch** | $0 (free) | Wishlist tracking begins; target: 1,000 wishlists by launch |
| **Press kit creation** | $50–$100 | PDF with screenshots, trailer, description, system requirements |
| **Trailer production** | $200–$500 | 60-second trailer; self-produced or commissioned |
| **Influencer outreach** | $100–$300 | Send keys to 20–30 YouTubers/Streamers in puzzle/coding niche |
| **Social media ads** | $200–$500 | Twitter/X, TikTok, Instagram ads targeting puzzle game fans |
| **Subtotal pre-launch** | **$550–$1,400** | |

### Launch Week (Month 0)

| Activity | Cost | Expected Outcome |
|----------|------|------------------|
| **Steam launch promotion** | $0 (free) | New Release tag; front-page feature if wishlist count >5,000 |
| **Press outreach** | $100–$200 | Send review keys to 30–50 gaming publications |
| **Community engagement** | $50–$100 | Discord server management; Reddit AMAs; Twitter threads |
| **Subtotal launch week** | **$150–$300** | |

### Post-Launch (Months 1–6)

| Activity | Cost | Expected Outcome |
|----------|------|------------------|
| **Ongoing social media ads** | $100–$300/month | Maintain wishlist growth; drive day-one sales |
| **Influencer partnerships** | $200–$500/month | Sponsored streams/reviews; affiliate links |
| **Steam sale participation** | $0 (discount cost) | 20–30% off during seasonal sales; drives volume |
| **Subtotal post-launch (6 months)** | **$1,800–$4,800** | |

### Total Marketing Budget (Year 1)

| Phase | Conservative | Base Case | Optimistic |
|-------|-------------|-----------|------------|
| Pre-launch | $550 | $900 | $1,400 |
| Launch week | $150 | $200 | $300 |
| Post-launch (6 months) | $1,800 | $3,000 | $4,800 |
| **Total** | **$2,500** | **$4,100** | **$6,500** |

### Marketing ROI Targets

| Metric | Target | Notes |
|--------|--------|-------|
| **Wishlist-to-purchase conversion** | 15–30% | Industry benchmark for well-marketed indie puzzle games |
| **Cost per wishlist** | $0.25–$0.50 | Driven by social media ads + influencer partnerships |
| **Return on marketing spend** | 10:1 minimum | $4,100 marketing → $41,000+ revenue (base case) |

---

## 7. MONETIZATION RISKS AND MITIGATIONS

| Risk | Probability | Impact | Mitigation |
|------|-------------|--------|------------|
| **Steam sales cannibalize full-price sales** | High | Medium | Steam sales drive wishlists and long-tail revenue; full price is only ~30% of the year |
| **Android conversion rate below 10%** | Medium | Medium | Improve free district quality; add "unlock full game" prompt after mission completion |
| **Refund rate exceeds 10% on Steam** | Low | Low | Free demo reduces refunds; Steam's 2-hour/14-day refund policy is standard |
| **Google Play reduces developer revenue share above $10M** | Medium (long-term) | Low | At $10M/year, rate drops to 85% → still very favorable vs. historical 70% |
| **Price sensitivity in non-US markets** | High | Medium | Steam regional pricing; Google Play local currency IAPs |
| **DLC sales underperform expectations** | Medium | Low | DLC priced at $4.99 (impulse buy range); bundle discounts encourage multiple purchases |

---

## 8. KEY FINANCIAL UNKNOWNS

| Unknown | Why It Matters | How to Reduce Uncertainty |
|---------|---------------|--------------------------|
| **Actual Steam wishlist-to-purchase conversion** | Drives revenue projection accuracy | Track wishlists from demo launch; industry benchmark is 10–30% for well-marketed indie games |
| **Android free-district drop-off rate** | Determines how many users see the IAP prompt | A/B test IAP placement (after mission completion vs. district end) |
| **Player retention across districts** | Impacts perceived value and refund rates | Implement in-game analytics; track % of players completing each district |
| **Steam sale performance vs. full-price periods** | Informs pricing calendar | Monitor first 2–3 sales cycles; adjust discount depth/frequency accordingly |

---

*This monetization plan supports all Phase 5–8 development and publishing work. Pricing and DLC roadmap may evolve based on playtesting feedback, player demand, and market conditions.*
