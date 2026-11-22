# Platform Requirements — Signalbreakers Research

**Date:** 22 November 2026  
**Purpose:** Define Windows (Steam) and Android (Google Play) platform specifications, system requirements, and store submission requirements.

---

## 1. Windows / Steam Platform

### 1.1 System Requirements (Target)

Based on analysis of comparable puzzle games (Hacknet, Human Resource Machine, TIS-100), Signalbreakers should target the following minimum and recommended specifications:

| Component | Minimum | Recommended | Rationale |
|-----------|---------|-------------|-----------|
| **OS** | Windows 10 (64-bit) | Windows 10/11 (64-bit) | Broadest compatibility; Godot 4.x drops Win 7 |
| **CPU** | Intel Core i3 / AMD Ryzen 3 (dual-core, 2.0 GHz+) | Intel Core i5 / AMD Ryzen 5 (quad-core) | Puzzle logic is CPU-light; rendering is the main load |
| **GPU** | Integrated graphics (Intel HD 620 / AMD Radeon Vega 3) | Dedicated GPU (GTX 1050 / RX 560 or better) | 2D pixel-art rendering; integrated GPUs handle this easily |
| **RAM** | 4 GB | 8 GB | Godot editor overhead + game runtime |
| **Storage** | 500 MB free | 500 MB free | 2D assets are compact; 8 districts with art/audio ~300–400 MB |
| **DirectX** | DirectX 11 | DirectX 11 | Godot 4.x uses Vulkan by default but supports DX11 via backend |

**Design targets:**
- Target resolution: 1920×1080 (scale down to 1280×720 for lower-end devices)
- Frame rate target: 60 FPS on recommended hardware; 30 FPS minimum on minimum hardware
- Steam Deck verified: Yes — Godot 4.x has excellent Steam Deck support

### 1.2 Steam Store Requirements

| Requirement | Details | Status |
|-------------|---------|--------|
| **Steamworks SDK** | Integrate for achievements, cloud saves, leaderboards (optional) | Phase 4 prototype |
| **Age rating** | ESRB (US), PEGI (EU), CERO (JP) — target E10+ / PEGI 7 | Phase 5 |
| **Store page** | Screenshots (min. 5), trailer, description, system requirements | Phase 7 |
| **Demo** | Recommended for puzzle games — Steam supports free demos natively | Phase 5 |
| **Release type** | Premium one-time purchase ($14.99–$19.99 USD) | Business model decision |
| **Steam features** | Achievements (recommended), Cloud Saves (required), Trading Cards (optional) | Phase 4+ |

### 1.3 Steam Publishing Costs

| Item | Cost | Notes |
|------|------|-------|
| **Steam developer fee** | $100 per game | Recoupable after $1,000 in gross revenue |
| **Steam revenue share** | 30% standard | Drops to 25% after $10M lifetime; 20% after $50M |
| **Payment processing** | ~2.9% + $0.30 per transaction | Handled by Steam; deducted from revenue share |

---

## 2. Android / Google Play Platform

### 2.1 System Requirements (Target)

Android has extreme device fragmentation. Signalbreakers should target:

| Component | Minimum | Recommended | Rationale |
|-----------|---------|-------------|-----------|
| **OS** | Android 8.0 (API 26) minimum | Android 10+ (API 29+) | API 26 covers ~95% of active devices; Godot 4.x supports this |
| **CPU** | ARMv7, 1.5 GHz dual-core | ARM64, 2.0 GHz quad-core | ARM64 preferred for modern devices; ARMv7 for legacy |
| **GPU** | OpenGL ES 3.0 | Vulkan 1.0 / OpenGL ES 3.1 | Godot 4.x uses Vulkan by default on Android |
| **RAM** | 2 GB | 4 GB+ | 2GB is the practical minimum for Godot 4.x games |
| **Storage** | 500 MB free | 500 MB free | APK + OBB ~30–80 MB depending on asset compression |

**Design targets:**
- Target resolution: Scales from 720p to device native resolution
- Aspect ratios: 16:9, 18:9, 19.5:9 (modern phones); support for ultrawide (20:9+) with letterboxing
- Touch controls: Tap/swipe/gesture-based; no virtual joystick needed for puzzle game
- Offline play: Full offline functionality required

### 2.2 Google Play Store Requirements

| Requirement | Details | Deadline / Status |
|-------------|---------|-------------------|
| **Target API level** | Android 16 (API 36) minimum for new apps submitted after 31 Aug 2026 | **Critical — must target API 36** |
| **Existing apps** | Must target Android 15 (API 35) to remain available to new users on newer devices | Extension available until 1 Nov 2026 |
| **App bundle** | AAB format required (not APK) | Standard since 2021 |
| **Developer account** | Google Play Console registration | $25 one-time fee |
| **Content rating** | IARC self-assessment (ages, violence, language, etc.) | Required before first submission |
| **Privacy policy** | URL-hosted privacy policy required if app collects any data | Required |
| **Data safety section** | Declare what data is collected and whether it's shared | Required since March 2022 |
| **Ads policy** | If ads present: max 3 interstitials per hour; no ads in first 60 seconds of session | If applicable |
| **In-app purchase** | Google Play billing library (v5+) for full-game unlock | Required for freemium model |

### 2.3 Google Play Publishing Costs

| Item | Cost | Notes |
|------|------|-------|
| **Developer registration** | $25 one-time fee | Per Google account, not per app |
| **Google Play revenue share** | 15% for first $10M/year (per developer) | Reduced rate since 2023; standard 30% above that |
| **In-app purchase processing** | 15% + payment processing fees | Same reduced rate applies to IAPs |

### 2.4 Android-Specific Considerations

| Concern | Mitigation |
|---------|------------|
| **Device fragmentation** | Test on at least 3 device tiers: low-end (2GB RAM), mid-range (4GB), high-end (8GB+) |
| **Screen size/aspect ratio** | Use Godot's viewport scaling; test on 16:9, 18:9, and 20:9 aspect ratios |
| **Touch vs. keyboard** | Android version uses touch controls; Windows version supports mouse + keyboard |
| **App size** | Keep APK under 150 MB (Google Play's uncompressed limit); use OBB for larger assets if needed |
| **Background restrictions** | Android 8+ limits background services; design game to not require background activity |
| **Google Play Pass** | Consider submitting for inclusion — provides exposure and subscription revenue |

---

## 3. Godot 4.x Platform Export Requirements

### 3.1 Required Tools

| Tool | Purpose | Installation Priority |
|------|---------|---------------------|
| **Godot 4.7 stable** | Game engine | P0 — already identified in Phase 0 |
| **Java JDK 17 or 21** | Android build toolchain | P0 — required for Godot's Android export |
| **Android SDK + NDK** | Android platform tools | P0 — bundled with Godot's Android export template (auto-installs) |
| **Android Studio (optional)** | Advanced Android debugging | P1 — useful for device-specific testing |

### 3.2 Export Templates

Godot requires separate export templates for each target platform:

- **Windows:** `.exe` via Godot's built-in Windows export (no external tools needed)
- **Android:** `.aab` via Godot's Android export (requires JDK + SDK, auto-configured by Godot)
- **Linux/macOS:** Optional secondary platforms — not in MVP scope

### 3.3 Build Size Targets

| Platform | Target APK/AAB Size | Notes |
|----------|---------------------|-------|
| **Android** | 30–80 MB (APK) + OBB if needed | Compress textures; use Ogg for audio; strip debug symbols |
| **Windows** | 20–50 MB (.exe + data) | Godot export includes minimal runtime; compress with UPX optional |

---

## 4. Cross-Platform Design Decisions

### 4.1 Input Handling

| Input Type | Windows | Android |
|------------|---------|---------|
| Mouse click | Primary interaction | N/A |
| Keyboard (arrow keys, enter) | For code input/confirmation | Optional (on-device keyboard) |
| Touch tap | Secondary (for tablet users) | Primary interaction |
| Swipe gestures | N/A | For navigation between panels |

### 4.2 UI Scaling Strategy

- **Windows:** Fixed layout at 1920×1080, scales down proportionally for lower resolutions
- **Android:** Fluid layout using Godot's anchors/margins; tested on 720p–1440p range
- **Common:** All text uses scalable font sizes (not pixel-fixed); touch targets minimum 48×48 dp

### 4.3 Save System

| Platform | Storage Location | Sync |
|----------|-----------------|------|
| **Windows** | Local file + Steam Cloud | Steam Cloud sync enabled |
| **Android** | Local device storage | Optional Google Drive backup (Phase 6+) |

---

## 5. Platform-Specific Store Descriptions (Draft)

### Windows / Steam

> **Signalbreakers: The Neon Protocol** — Decode the future of LUMA-9.  
> A cyberpunk puzzle-adventure where you program communication systems, crack encrypted transmissions, and uncover a city-wide conspiracy. Learn real computational thinking concepts through 8 unique districts, three difficulty modes, and a gripping mystery story. No ads. No loot boxes. Just puzzles, story, and neon.

### Android / Google Play

> **Signalbreakers: The Neon Protocol** — Decode the future on your phone.  
> A free introductory district of the cyberpunk puzzle-adventure game. Program robots, crack codes, and uncover a mystery in a neon-lit floating city. Learn computational thinking through engaging puzzles — no ads, no subscriptions. Unlock all 8 districts with one purchase.

---

## 6. Open Questions

| Question | Impact | Next Step |
|----------|--------|------------|
| Target API 36 (Android 16) by Aug 2026 deadline? | Android launch timing | Verify Godot 4.7 supports API 36 at release |
| Steam demo included in MVP or Phase 5+? | Marketing lead time | Include if feasible; demos drive wishlists |
| Google Play Pass submission target? | Revenue diversification | Prepare assets for Play Pass application post-launch |
| Windows-only first, then Android? | Development sequencing | Parallel development recommended; Godot supports both from same project |

---

## 7. Sources and Verification Dates

| Source | URL | Verified |
|--------|-----|----------|
| Google Play Target API Requirements | https://developer.android.com/google/play/requirements/target-sdk | 22 Nov 2026 |
| Play Console Help — Target API Levels | https://support.google.com/googleplay/android-developer/answer/11926878 | 22 Nov 2026 |
| Noun Town — Steam System Requirements Guide | https://noun.town/blog/what-are-steams-system-requirements-a-plain-english-guide-for-non-gamers/ | 22 Nov 2026 |
| Google Play Store Statistics (42matters) | https://42matters.com/google-play-statistics-and-trends | 22 Nov 2026 |

---

*Next: BUSINESS_MODEL.md — Monetization strategy with revenue projections, pricing scenarios, and cost analysis.*
