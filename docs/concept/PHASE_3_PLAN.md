# Phase 3 Plan — Game Design Document

**Date:** 23 November 2026  
**Purpose:** Outline the structure and scope of the full GDD, which will expand all Phase 2 decisions into detailed specifications.

---

## Phase 3 Deliverables

| # | Document | Status | Notes |
|---|----------|--------|-------|
| 1 | `GDD.md` — Full Game Design Document | 🔲 NOT STARTED | Core document; expands all Phase 2 decisions into detailed specs |
| 2 | `STORY_BIBLE.md` — Story bible with character profiles | 🔲 NOT STARTED | Expands LUMA-9 story premise into full narrative reference |
| 3 | `SYSTEMS_DESIGN.md` — Systems design documentation | 🔲 NOT STARTED | Core gameplay loops, UI systems, save/load, difficulty modes |
| 4 | `EDUCATIONAL_MAPPING.md` — Educational design mapping | 🔲 NOT STARTED | Maps each district/mission to CS concepts and learning outcomes |
| 5 | `ACCESSIBILITY_PLAN.md` — Accessibility plan | 🔲 NOT STARTED | Colorblind support, ADHD-friendly features, input options |
| 6 | `MONETIZATION_PLAN.md` — Monetization plan (expanded) | 🔲 NOT STARTED | Expands Phase 1 business model with pricing calendar and launch strategy |
| 7 | `PLATFORM_DEPLOYMENT.md` — Platform deployment plans | 🔲 NOT STARTED | Steam + Google Play submission checklists, release strategy |

---

## GDD Structure (Document #1)

The main GDD will be organized as follows:

### Part A: Game Overview
- Game concept and vision statement
- Target audience and player personas (from Phase 2)
- Core gameplay loop description
- Unique selling propositions (from Phase 2)
- Platform targets (Windows + Android)

### Part B: Story and World
- World lore: Aethelgard Prime, the Neon Protocol, anti-gravity core
- Character profiles: LUMA-9, AETHEL, Kai-7, Director Vespa, Nova
- Story progression across 8 districts
- Ending conditions (3 endings + secret)

### Part C: Gameplay Systems
- Core mechanics: signal decoding, robot programming, codebook lookup
- Difficulty modes: Explorer, Engineer, Blackout — detailed behavior for each
- Puzzle design patterns: loops, conditionals, nested logic, parallelism
- Progression systems: district map, lore collection, achievement tracking
- Save/load system and cloud sync

### Part D: Level Design
- District-by-district breakdown (8 districts)
- Mission-by-mission specifications (first 10 missions detailed; remaining 30+ summarized)
- Visual themes and environmental design per district
- Puzzle difficulty curve across all missions

### Part E: User Interface
- UI layout for Windows vs. Android
- Signal visualization system
- Codebook/reference panel design
- Menu structure and navigation flow
- Accessibility features (colorblind modes, text scaling, input options)

### Part F: Audio Design
- Music direction per district
- Sound effects catalog (signal processing, robot movement, UI feedback)
- Voice acting plan (minimal; environmental audio focus)

### Part G: Technical Specifications
- Engine: Godot 4.7+ with GDScript
- Target platforms and system requirements
- Build size targets (Android AAB < 80MB, Windows .exe < 50MB)
- Development pipeline and version control workflow

### Part H: Production Plan
- Phase breakdown with milestones
- Resource estimates (art, audio, programming, design)
- Testing plan (internal → closed beta → limited launch)
- Post-launch support schedule

---

## Estimated Effort

| Document | Lines of Content | Time Estimate |
|----------|-----------------|---------------|
| GDD.md | ~3000–4000 lines | 2–3 hours writing |
| Story Bible | ~1500–2000 lines | 1–2 hours writing |
| Systems Design | ~2000–2500 lines | 1.5–2 hours writing |
| Educational Mapping | ~800–1200 lines | 45 min writing |
| Accessibility Plan | ~600–800 lines | 30 min writing |
| Monetization Plan | ~800–1000 lines | 45 min writing |
| Platform Deployment | ~800–1000 lines | 45 min writing |

**Total estimated effort:** ~9–12 hours of focused writing  
**Approach:** Write all documents in this session using web research for current platform requirements and pricing data.

---

## Research Needs Before Writing

| Topic | Source | Priority |
|-------|--------|----------|
| Steam system requirements format | Steamworks documentation | High |
| Google Play target API level (Android 16/API 36 deadline) | Android developer docs | High |
| Current Steam pricing benchmarks for puzzle games | Steam store search | Medium |
| Accessibility features in comparable games | Steam accessibility tags | Low |

---

*Phase 3 will produce the definitive design reference for all development work through Phase 8. All decisions here will be locked unless validated/invalidated during playtesting.*
