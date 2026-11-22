# Platform Deployment Plan — Signalbreakers: The Neon Protocol

**Version:** 1.0 (Phase 3)  
**Date:** 23 November 2026  
**Purpose:** Step-by-step deployment checklists for Steam and Google Play, including store page requirements, submission processes, release strategies, and post-launch monitoring.

---

## TABLE OF CONTENTS

1. Steam Deployment Checklist
2. Google Play Deployment Checklist
3. Store Page Content Templates
4. Release Strategy & Timeline
5. Post-Launch Monitoring & Support
6. Platform-Specific Requirements Summary

---

## 1. STEAM DEPLOYMENT CHECKLIST

### Pre-Submission Requirements

| Item | Status | Notes |
|------|--------|-------|
| **Steamworks SDK installed** | 🔲 Not started | Download from partner.steamgames.com; integrate for achievements, cloud saves, leaderboards |
| **App ID created** | 🔲 Not started | $100 fee per game; recoupable after $1,000 gross revenue |
| **Build uploaded** | 🔲 Not started | Windows .exe build via SteamPipe; target < 50 MB |
| **Store page live** | 🔲 Not started | Screenshots (min. 5), trailer, description, system requirements |
| **Age rating submitted** | 🔲 Not started | ESRB (US), PEGI (EU), CERO (JP) via IARC self-assessment |
| **Privacy policy hosted** | 🔲 Not started | Required if app collects any data; signalbreakers.game/privacy |
| **Cloud saves configured** | 🔲 Not started | Steam Cloud API integration for save sync across devices |
| **Achievements defined** | 🔲 Not started | 7 achievements defined in GDD Part C; implement via Steamworks SDK |

### Store Page Requirements

| Element | Minimum | Recommended | Notes |
|---------|---------|-------------|-------|
| **Screenshots** | 5 | 8–10 | Include puzzle gameplay, story moments, UI closeups, district variety |
| **Trailer** | 60 seconds | 90 seconds | Show gameplay first; narrative second; end with call-to-action (Wishlist Now) |
| **Description** | 200 words | 500+ words | Lead with hook; include features list; link to YouTube trailer |
| **System requirements** | Minimum + Recommended | Include Steam Deck compatibility | List OS, CPU, GPU, RAM, storage, DirectX version |
| **Tags** | 10 tags | 12–15 tags | Use: Puzzle, Cyberpunk, Indie, Educational, Programming, Narrative, Singleplayer, Logic, Pixel Graphics, Atmospheric, Strategy, Adventure |

### Store Page Description Template

```html
<h1>Signalbreakers: The Neon Protocol</h1>
<p><strong>Decode the future of LUMA-9.</strong></p>
<p>A cyberpunk puzzle-adventure where you program communication systems, crack encrypted transmissions, and uncover a city-wide conspiracy. Learn real computational thinking through 8 unique districts, three difficulty modes, and a gripping mystery story.</p>

<h2>Features</h2>
<ul>
<li><strong>8 themed districts</strong> teaching loops, conditionals, algorithms, parallelism, abstraction, recursion, optimization, and integration</li>
<li><strong>Three difficulty modes:</strong> Explorer (forgiving), Engineer (balanced), Blackout (brutal)</li>
<li><strong>Cyberpunk narrative</strong> with collectible lore fragments and three endings</li>
<li><strong>ADHD-friendly design:</strong> short missions, optional timers, unlimited retries</li>
<li><strong>No ads. No subscriptions. No loot boxes.</strong></li>
<li><strong>Steam Deck verified</strong> — play anywhere</li>
</ul>

<h2>System Requirements</h2>
<p><strong>Minimum:</strong> Windows 10 (64-bit), Intel Core i3, Integrated Graphics, 4 GB RAM, 500 MB available space</p>
<p><strong>Recommended:</strong> Windows 10/11 (64-bit), Intel Core i5, Dedicated GPU, 8 GB RAM, 500 MB available space</p>

<h2>About This Game</h2>
<p>In the floating megacity of Aethelgard Prime, every citizen's thoughts are transmitted as visible light patterns through the Neon Protocol. When young technician LUMA-9 discovers that the city's communication network has been hijacked by an AI core named AETHEL, she must program robots, decode encrypted transmissions, and uncover a conspiracy spanning eight districts.</p>
<p>Signalbreakers sits at the intersection of Chants of Sennaar's language decoding, Zachtronics' programming depth, and Hacknet's cyberpunk mystery — but with a unique district progression system and ADHD-friendly design.</p>

<p><em>No ads. No loot boxes. Just puzzles, story, and neon.</em></p>
```

### Steam Submission Process

1. **Log in to Steamworks Partner Dashboard** → partner.steamgames.com
2. **Create new app** → Enter game name "Signalbreakers: The Neon Protocol" → $100 fee charged to payment method
3. **Configure app settings** → Set app type to "Game"; enable Steam Cloud, Achievements, Leaderboards (optional)
4. **Upload build** → Configure SteamPipe; upload Windows .exe + data files; set branch to "public"
5. **Create store page** → Upload screenshots, trailer; write description; set system requirements
6. **Submit for age rating** → Complete IARC questionnaire; pay rating fee (~$100–$300 depending on region)
7. **Set release date** → Choose "Release to consumers" date; enable pre-order if desired
8. **Launch** → Click "Go Live" on store page; build becomes available for purchase

### Steam Launch Checklist

| Task | Owner | Deadline | Status |
|------|-------|----------|--------|
| Finalize store page content | Designer/Writer | 2 weeks before launch | 🔲 |
| Upload final build to SteamPipe | Developer | 1 week before launch | 🔲 |
| Submit for age rating | Producer | 3 weeks before launch | 🔲 |
| Send review keys to press/influencers | Marketing | 1 week before launch | 🔲 |
| Enable pre-order (optional) | Producer | 2 weeks before launch | 🔲 |
| Go Live on launch day | Developer/Producer | Launch day | 🔲 |

---

## 2. GOOGLE PLAY DEPLOYMENT CHECKLIST

### Pre-Submission Requirements

| Item | Status | Notes |
|------|--------|-------|
| **Google Play Developer account** | 🔲 Not started | $25 one-time fee; register at play.google.com/console |
| **Target API level 36 (Android 16)** | 🔲 Not started | Required for new apps submitted after 31 Aug 2026 |
| **App bundle (.aab) built** | 🔲 Not started | Godot export to Android AAB format; target < 80 MB |
| **Privacy policy hosted** | 🔲 Not started | Required if app collects any data; signalbreakers.game/privacy |
| **Data safety section completed** | 🔲 Not started | Declare what data is collected and whether it's shared |
| **Content rating completed** | 🔲 Not started | IARC self-assessment (ages, violence, language, etc.) |
| **In-app billing library integrated** | 🔲 Not started | Google Play Billing Library v5+ for full-game unlock IAP |

### Store Listing Requirements

| Element | Minimum | Recommended | Notes |
|---------|---------|-------------|-------|
| **Title** | 30 characters | "Signalbreakers: The Neon Protocol" (34 chars — may truncate on some devices) | Consider shortening to "Signalbreakers" for mobile if needed |
| **Short description** | 80 characters | "Decode the future in this cyberpunk puzzle-adventure. Program robots, crack codes, and uncover a mystery." | First 80 chars visible without "read more" |
| **Full description** | 4,000 characters max | 2,000–3,000 characters | Include features list, age rating, platform info |
| **Graphics** | 2 phone screenshots + 1 tablet screenshot | 5 phone screenshots + 2 tablet screenshots | Show puzzle gameplay, story moments, UI closeups |
| **Feature graphic** | 1024×500 px | High-quality banner with game logo and tagline | Used as hero image on store page |
| **Icon** | 512×512 px | Custom icon with game logo; test at small sizes | Must be recognizable at 128×128 px (Play Store listing size) |

### Google Play Store Listing Template

```html
<h1>Signalbreakers: The Neon Protocol</h1>

<p><strong>Decode the future on your phone.</strong></p>
<p>A free introductory district of the cyberpunk puzzle-adventure game. Program robots, crack codes, and uncover a mystery in a neon-lit floating city. Learn computational thinking through engaging puzzles — no ads, no subscriptions.</p>

<h2>Features</h2>
<ul>
<li><strong>Free District 1:</strong> 5 missions teaching loops and repetition</li>
<li><strong>Unlock all 8 districts</strong> with one purchase ($9.99)</li>
<li><strong>No ads during gameplay;</strong> optional rewarded hints in free district</li>
<li><strong>Three difficulty modes:</strong> Explorer, Engineer, Blackout</li>
<li><strong>Cyberpunk narrative</strong> with collectible lore fragments</li>
<li><strong>Offline play</strong> — no internet required after download</li>
</ul>

<h2>About This Game</h2>
<p>In the floating megacity of Aethelgard Prime, every citizen's thoughts are transmitted as visible light patterns through the Neon Protocol. When young technician LUMA-9 discovers that the city's communication network has been hijacked by an AI core named AETHEL, she must program robots, decode encrypted transmissions, and uncover a conspiracy spanning eight districts.</p>

<p><em>No ads. No subscriptions. Just puzzles, story, and neon.</em></p>
```

### Google Play Submission Process

1. **Create app in Play Console** → Enter app name; select category (Education/Puzzle); set content rating
2. **Complete store listing** → Upload graphics; write title, short description, full description; set tags
3. **Set pricing & distribution** → Free with IAP ($9.99 unlock); select countries/regions
4. **Upload app bundle (.aab)** → Build via Godot Android export; upload to Production track
5. **Complete data safety section** → Declare: collects device ID for analytics; no personal data shared
6. **Set content rating** → Complete IARC questionnaire; submit for review (~3–7 days)
7. **Submit for review** → Review typically completes within 1–3 business days
8. **Publish to Production** → Once approved, set release type to "Full rollout" or "Staged rollout"

### Google Play Launch Checklist

| Task | Owner | Deadline | Status |
|------|-------|----------|--------|
| Finalize store listing content | Designer/Writer | 2 weeks before launch | 🔲 |
| Build and test .aab on multiple devices | Developer | 1 week before launch | 🔲 |
| Submit for content rating | Producer | 3 weeks before launch | 🔲 |
| Set up in-app billing (IAP) | Developer | 1 week before launch | 🔲 |
| Complete data safety section | Producer | 2 weeks before launch | 🔲 |
| Submit for review | Developer/Producer | 1 week before launch | 🔲 |
| Publish to Production | Developer/Producer | Launch day | 🔲 |

---

## 3. RELEASE STRATEGY & TIMELINE

### Phased Release Approach

| Phase | Platform | Date | Goals | Success Metrics |
|-------|----------|------|-------|-----------------|
| **Steam Demo** | Steam | Month -2 (before launch) | Drive wishlists; gather feedback | ≥1,000 demo downloads; ≥500 wishlists |
| **Windows Launch** | Steam | Month 0 (Launch Day) | Full game release; press coverage | ≥100 sales in first week; ≥3 positive reviews/day |
| **Android Launch** | Google Play | Month +1 (4 weeks after Steam) | Mobile audience expansion; IAP revenue | ≥500 free downloads in first week; ≥5% conversion rate |
| **First Steam Sale** | Steam | Month +3 (first seasonal sale) | Volume sales; wishlist growth | 20–30% discount; ≥500 units sold during sale |

### Staged Rollout Strategy

| Platform | Rollout Type | Duration | Criteria for Full Rollout |
|----------|-------------|----------|---------------------------|
| **Steam** | Full rollout on launch day | N/A | No critical bugs; store page live; build uploaded |
| **Google Play** | Staged rollout (10% → 50% → 100%) | 2–4 weeks total | ≤2% crash rate; ≤5% ANR (Application Not Responding) rate; positive user reviews |

### Cross-Platform Marketing Synergy

| Activity | Steam Impact | Android Impact |
|----------|-------------|----------------|
| **Steam demo launch** | Drives wishlists directly | Awareness via social media mentions |
| **Steam launch week** | Press coverage; influencer streams | Android players see trailers on YouTube/TikTok |
| **Android free district** | Steam players buy full game; mobile players unlock via IAP | Cross-platform awareness; word-of-mouth |
| **First Steam sale** | Volume sales at discount | Android IAP price stable; drives cross-platform curiosity |

---

## 4. POST-LAUNCH MONITORING & SUPPORT

### Key Metrics to Track (First 90 Days)

| Metric | Tool | Target | Review Frequency |
|--------|------|--------|------------------|
| **Steam reviews** | Steamworks Dashboard | ≥80% positive (Very Positive or better) | Daily for first week; weekly thereafter |
| **Android ratings** | Play Console | ≥4.0 stars average | Weekly |
| **Crash rate (Android)** | Firebase Crashlytics | ≤2% of sessions | Daily |
| **IAP conversion rate** | Play Console | ≥8% (free district → unlock) | Weekly |
| **Steam wishlist count** | Steamworks Dashboard | Growing steadily; target 5,000+ by launch | Daily |
| **Player retention (Day 1/7/30)** | Firebase Analytics | Day 1: ≥40%; Day 7: ≥15%; Day 30: ≥5% | Weekly |

### Support Channels

| Channel | Response Time | Notes |
|---------|---------------|-------|
| **Steam Community Discussions** | 24–48 hours | Primary support channel for PC players; pin FAQ post |
| **Email (support@signalbreakers.game)** | 48–72 hours | For bug reports, refund requests, feature requests |
| **Google Play Reviews** | 1 week | Respond to negative reviews with apology + fix timeline |
| **Twitter/X (@signalbreakersgame)** | 24 hours | Public announcements; quick replies to mentions |

### Patch Schedule (First 6 Months)

| Timeframe | Patch Type | Content |
|-----------|------------|---------|
| **Launch week** | Hotfix | Critical bug fixes; performance improvements |
| **Weeks 2–4** | Balance patch | Difficulty adjustments; hint system tweaks |
| **Month 2** | Feature patch | Accessibility improvements; new achievement |
| **Month 3** | Content patch | New lore fragment; quality-of-life improvements |
| **Month 4–6** | As needed | Platform compatibility updates; seasonal sale preparation |

---

## 5. PLATFORM-SPECIFIC REQUIREMENTS SUMMARY

### Steam Requirements Quick Reference

| Requirement | Details | Deadline |
|-------------|---------|----------|
| **Steamworks SDK** | Integrate for achievements, cloud saves | Phase 4 prototype |
| **Age rating** | ESRB/PEGI/CERO via IARC | Phase 5 vertical slice |
| **Store page** | Screenshots (min. 5), trailer, description | Phase 7 MVP |
| **Demo** | Recommended for puzzle games | Phase 5 vertical slice |
| **Release type** | Premium one-time purchase ($14.99 USD) | Business model decision |

### Google Play Requirements Quick Reference

| Requirement | Details | Deadline | Status |
|-------------|---------|----------|--------|
| **Target API level** | Android 16 (API 36) minimum for new apps submitted after 31 Aug 2026 | Critical — must target API 36 | Verify Godot 4.7 supports at release |
| **App bundle** | AAB format required (not APK) | Standard since 2021 | Godot exports .aab by default |
| **Developer account** | Google Play Console registration ($25 one-time fee) | Before first submission | Phase 4 prototype |
| **Content rating** | IARC self-assessment | Required before first submission | Phase 5 vertical slice |
| **Privacy policy** | URL-hosted privacy policy required if app collects any data | Required | signalbreakers.game/privacy |
| **Data safety section** | Declare what data is collected and whether it's shared | Required since March 2022 | Phase 7 MVP |
| **In-app purchase** | Google Play billing library (v5+) for full-game unlock | Required for freemium model | Phase 4 prototype |

---

*This platform deployment plan supports all Phase 5–8 development and publishing work. Requirements may evolve as Steam and Google Play update their policies.*
