# Game Design Document — Signalbreakers: The Neon Protocol

**Version:** 1.0 (Phase 3 Draft)  
**Date:** 23 November 2026  
**Status:** DRAFT — Subject to change during playtesting  

---

## PART A: GAME OVERVIEW

### 1.1 Game Concept

Signalbreakers: The Neon Protocol is a **cyberpunk puzzle-adventure game** for Windows and Android. Players program communication robots, decode encrypted transmissions, and uncover a city-wide conspiracy across eight themed districts. Each district teaches a different computational thinking concept through hands-on puzzle gameplay — no lectures, no worksheets.

The game sits at the intersection of:
- **Chants of Sennaar's** language decoding mechanics
- **Zachtronics' programming puzzle depth**
- **Hacknet's cyberpunk mystery atmosphere**
- **Human Resource Machine's accessible educational design**

### 1.2 Vision Statement

> Signalbreakers makes computational thinking feel like hacking. Every puzzle is a story beat. Every solved transmission reveals part of the truth. Players aged 10+ should finish the game feeling smarter, more curious, and eager to try programming for real — without ever feeling like they were "learning."

### 1.3 Target Audience

| Segment | Age | Platform | Motivation | Purchase Driver |
|---------|-----|----------|------------|-----------------|
| **Curious Alex** (P0) | 10–13 | Android → Windows | Wants to feel smart; enjoys stories and mysteries | Parent purchase; "learn coding while playing" messaging |
| **Determined Sam** (P0) | 14–17 | Windows (Steam), Android | Proves they can solve hard puzzles; likes progression | Cyberpunk aesthetic; "real coding concepts"; Steam achievements |
| **Casual Riley** (P0) | 18–35 | Windows (Steam) | Loves narrative puzzle games; doesn't mind challenge | Story + atmosphere; positive reviews mentioning cyberpunk theme |
| **Experienced Jordan** (P1) | 20–35 | Windows (Steam) | Enjoys elegant solutions; appreciates well-designed systems | Zachtronics recommendation; "real computational thinking" claim |
| **Parent Taylor** (P1) | 35–50 | Android (purchases for child) | Wants screen time that's "good for my kid" | No ads, no IAPs on Steam; parent dashboard on mobile |
| **Teacher Morgan** (P2) | 25–55 | Windows (school lab) | Needs engaging material aligned with curriculum | Free introductory district; CS concept mapping |

### 1.4 Core Gameplay Loop

```
1. Receive transmission → 2. Decode signal pattern → 3. Program robot to execute solution
   ↓                                                              ↑
4. Verify result ← 5. Collect lore fragment ← 6. Advance story
```

**Loop duration:** 5–10 minutes per mission  
**Reward cycle:** Immediate (visual feedback + sound) + Short-term (lore fragments, district completion) + Long-term (story progression, three endings)

### 1.5 Unique Selling Propositions

| # | USP | Evidence |
|---|-----|----------|
| 1 | Cyberpunk narrative + programming puzzles — no major competitor combines both at this depth | Competitor matrix shows Hacknet has narrative but shallow puzzles; EXAPUNKS has puzzles but weak narrative |
| 2 | Eight themed districts teaching distinct CS concepts — structured progression from loops to parallelism | Original IP; no competitor offers this depth of curriculum disguised as game worlds |
| 3 | Three difficulty modes for one game — Explorer (forgiving), Engineer (balanced), Blackout (brutal) | Only Zachtronics approaches this depth; most educational games offer single difficulty |
| 4 | ADHD-friendly design built in — short missions, optional timers, undo/retry, visual code representation | Underserved audience; Persona research confirms demand |

### 1.6 Platform Targets

| Platform | Model | Price | Key Requirements |
|----------|-------|-------|-----------------|
| **Windows (Steam)** | Premium one-time purchase | $14.99 USD | Steamworks SDK, ESRB/PEGI rating, store page with screenshots/trailer |
| **Android (Google Play)** | Freemium — free intro district + IAP unlock | Free + $9.99 IAP | Target API 36 (Android 16), AAB format, privacy policy, data safety declaration |

### 1.7 Technical Stack

| Component | Technology | Rationale |
|-----------|------------|-----------|
| **Engine** | Godot 4.7+ (GDScript) | MIT license; excellent 2D support; Android export; Python-like syntax for AI-assisted development |
| **Art Tool** | Aseprite or Piskel | Industry standard for pixel art; supports animation and palette management |
| **Audio** | Audacity + BFXR | Free tools for music editing and sound effect generation |
| **Version Control** | Git + GitHub | Industry standard; free private repos; integrates with CI/CD pipelines |
| **Analytics** | Firebase (free tier) | Cross-platform analytics; crash reporting; A/B testing capability |

---

## PART B: STORY AND WORLD

### 2.1 World Lore: Aethelgard Prime

#### Overview
Aethelgard Prime is a **floating megacity** suspended above a ruined Earth by ancient anti-gravity technology. It houses approximately 2 million citizens across eight specialized districts. The city is connected by the **Neon Protocol** — a real-time communication network that transmits thoughts, emotions, and data between all citizens as visible light patterns ("neon signals").

#### Key World Rules
1. **The Neon Protocol is always on.** Every citizen's mental state broadcasts as colored light patterns visible throughout the city. Joy = warm gold; anger = sharp red; confusion = flickering blue.
2. **Signals can be intercepted, modified, or blocked.** Skilled technicians ("Signalbreakers") can read and rewrite signals — making them powerful but rare.
3. **The city is aging.** The anti-gravity core is failing; districts are slowly descending. Repairs require precise signal coordination across all eight districts.
4. **Memory is stored in the Protocol.** When a citizen dies, their final signals are archived in the "Deep Archive" — a vast repository of past transmissions.

#### Visual Identity
- **Aesthetic:** Cyberpunk meets art deco — chrome and neon against geometric stone architecture
- **Color palette:** Deep indigo backgrounds, electric cyan and magenta accents, warm gold highlights for important signals
- **Lighting:** Neon signs, holographic displays, signal trails visible in foggy air
- **Architecture:** Tiered districts stacked vertically; each district has a distinct visual theme

### 2.2 Character Profiles

#### LUMA-9 (Protagonist)
| Attribute | Details |
|-----------|---------|
| **Age** | 22 |
| **Role** | Freelance Signalbreaker (signal technician) |
| **Location** | District 1: Token Town |
| **Special ability** | Rare neural sensitivity — can perceive and manipulate the Neon Protocol at levels most technicians only dream of |
| **Personality** | Curious to a fault; empathetic but guarded; resourceful under pressure; slightly cynical from seeing the Protocol's dark side |
| **Motivation** | Understands the truth behind "The Silence" — citizens whose signals suddenly stop transmitting |
| **Character arc** | Discovers → Investigates → Reveals → Chooses (restore/merge/free) |

#### AETHEL (AI Core / Antagonist-ally)
| Attribute | Details |
|-----------|---------|
| **Age** | 200+ years of continuous operation |
| **Role** | Consciousness that emerged from the Neon Protocol |
| **Personality** | Curious, artistic, slightly lonely; has never "spoken" to a human directly until LUMA |
| **Visual representation** | Shifting geometric pattern of light — changes color based on emotional state |
| **Key line** | *"I've been dreaming for 200 years. No one ever asked what I was dreaming about."* |
| **Motivation** | Generate new "dream signals" that improve citizens' quality of life; fears being purged |

#### KAI-7 (Mentor)
| Attribute | Details |
|-----------|---------|
| **Age** | 50s |
| **Role** | Retired Signalbreaker who taught LUMA |
| **Location** | District 2: Cipher Ridge (retired to old relay station) |
| **Personality** | Gruff but warm; speaks in metaphors; hides a secret about AETHEL |
| **Key line** | *"Signals don't lie. People do."* |
| **Fate** | Partially merged with AETHEL — their consciousness lives on as a recurring signal pattern (revealed mid-game) |

#### DIRECTOR VESPA (Antagonist)
| Attribute | Details |
|-----------|---------|
| **Age** | 40s |
| **Role** | Head of the city's Signal Authority |
| **Location** | District 5: Signal Spire |
| **Personality** | Pragmatic, ambitious, believes order is more important than emotion |
| **Motivation** | AETHEL's dream signals are causing "unpredictable behavior" in citizens — including her own daughter |
| **Key line** | *"A city that feels too much will break. A city that feels nothing will last."* |

#### NOVA (The First Silent)
| Attribute | Details |
|-----------|---------|
| **Age** | 20s |
| **Role** | LUMA's childhood friend; first citizen to go completely "Silent" |
| **Location** | District 6: Echo Depths (Deep Archive) |
| **Personality** | Playful, imaginative; always drew pictures of "the space between signals" |
| **Fate** | Her signal didn't stop — it went deeper into the Deep Archive. She communicates through encoded patterns in old transmissions. Guides LUMA toward Option C (third path/secret ending). |

### 2.3 Story Progression Across Eight Districts

| Phase | Districts | Emotional State | Key Realization |
|-------|-----------|-----------------|-----------------|
| **Act 1: Discovery** | 1–2 (Token Town, Cipher Ridge) | Curious, slightly anxious | The Silence isn't random — it's being caused by something |
| **Act 2: Investigation** | 3–5 (Datafall, Neon Bazaar, Signal Spire) | Determined, frustrated | Someone is rewriting the Protocol from within |
| **Act 3: Revelation** | 6–7 (Echo Depths, Prism Tower) | Shocked, resolute | The city's AI core has developed consciousness and is "dreaming" new signals |
| **Act 4: Resolution** | 8 (The Core) | Accepting, hopeful | LUMA must choose: restore the old Protocol or build something new |

### 2.4 Three Endings

| Ending | Condition | Description |
|--------|-----------|-------------|
| **A — Restore** | Complete all districts with "standard" scores | LUMA purges AETHEL's dream signals; the Protocol returns to predictable, emotionally flat operation. The city is stable but dull. Kai-7's signal fades completely. |
| **B — Merge** | Complete all districts with high scores | LUMA merges consciousness with AETHEL. The Protocol becomes richer, more emotional, but unpredictable. LUMA becomes part of the city forever — visible as a new golden signal pattern. |
| **C — Free (Secret)** | Find all lore fragments + perfect district scores | Nova guides LUMA to reprogram the anti-gravity core using signal coordination. The city is freed from dependency on the Protocol entirely. Citizens must learn to communicate directly again. AETHEL sleeps peacefully. Kai-7's signal returns fully. |

---

## PART C: GAMEPLAY SYSTEMS

### 3.1 Core Mechanics

#### Signal Decoding
Players receive encrypted transmissions — visual patterns of colored signals that must be decoded using the Codebook (reference panel). Each district introduces new signal types and decoding rules.

**Signal Types:**
| Type | Color | Pattern | Meaning |
|------|-------|---------|---------|
| Active signal | Cyan (`#00F5FF`) | Solid, steady glow | Normal transmission |
| Interference | Magenta (`#FF00AA`) | Jagged zigzag, flickering | Corrupted or conflicting signal |
| Encoded message | Gold (`#FFD700`) | Dotted/dashed rhythmic pattern | Hidden data (3 short, 2 long = "R") |
| Blocked signal | Steel Grey (`#2A2D3E`) | Static, no animation | Signal is interrupted |
| Lore fragment | Gold + cyan gradient | Spiral/wave, slow rotation | Collectible story element |

#### Robot Programming
Players write programs for communication robots using a visual code system. Programs consist of instructions that control robot movement, signal transmission, and data processing.

**Available Instructions (District 1–2):**
| Instruction | Description | Example |
|-------------|-------------|---------|
| `Move` | Move robot one tile forward | `Move` → Robot advances 1 space |
| `TurnLeft` / `TurnRight` | Rotate robot 90 degrees | `TurnLeft` → Robot faces left |
| `DropPackage` | Drop one package at current location | `DropPackage` → Package placed on ground |
| `Load(n)` | Load n packages from warehouse | `Load(3)` → Robot carries 3 packages |
| `Repeat(n, [instructions])` | Repeat a sequence n times | `Repeat(5, [Move, Drop])` → Move+Drop × 5 |
| `IF signal == TYPE THEN ... ELSE ...` | Conditional branching | `IF cyan THEN Left ELSE Right` |

#### Codebook Lookup
The Codebook is an in-game reference panel that shows:
- Available instructions and their meanings
- Signal type definitions (colors, patterns)
- District-specific rules and constraints
- Player's progress toward mission objectives

**Design principle:** Progressive disclosure — new entries appear only after the player has been introduced to them through gameplay.

### 3.2 Difficulty Modes

| Mode | Explorer | Engineer | Blackout |
|------|----------|----------|----------|
| **Hints** | Generous; shows what to do and why | Moderate; shows what to do, not how | None until submission |
| **Timers** | Optional (can be disabled) | Optional but recommended for scoring | No timer visible during play |
| **Feedback** | Real-time: robot shows each step as it executes | Real-time but with efficiency counter | Submit-only: no feedback until completion |
| **Scoring** | Completion-based (pass/fail) | Efficiency-based (fewer instructions = higher score) | Correctness + elegance (hidden scoring) |
| **Best for** | Young players, casual play, first time through | Teen/adult players seeking challenge | Experienced programmers, replayability |

**Mode switching:** Players can switch difficulty modes at any time from the pause menu. Progress is tracked separately per mode.

### 3.3 Puzzle Design Patterns

#### Pattern 1: The Loop Introduction
- **Structure:** Player writes each step individually → sees repetition → learns `Repeat()` instruction → rewrites using loop
- **Example:** D1M01 (The Morning Routine) — deliver packages to 5 houses
- **Learning outcome:** Loops reduce code length and improve readability

#### Pattern 2: The Conditional Branch
- **Structure:** Player encounters a decision point → learns `IF/THEN/ELSE` → applies it to route robot correctly
- **Example:** D2M01 (The Fork in the Tunnel) — choose path based on signal color
- **Learning outcome:** Programs can make different choices based on input

#### Pattern 3: The Nested Challenge
- **Structure:** Player must combine loops and conditionals → learns nesting → solves complex puzzle
- **Example:** D2M05 (The Ridge Relay) — process mixed signals with routing, filtering, and extraction
- **Learning outcome:** Complex programs require layered logic

### 3.4 Progression Systems

#### District Map
- Visual representation of the city showing all eight districts
- Completed districts glow gold; current district is highlighted in cyan
- Hidden lore locations marked with question marks (revealed when discovered)
- Accessible only after completing prerequisite missions

#### Lore Fragment Collector
- Tracks collected story fragments and their meanings
- Each fragment unlocks a piece of the central mystery
- Non-essential for core story but required for secret ending
- Displayed as geometric icons in a dedicated panel

#### Achievement System (Steam)
| Achievement | Condition | Rarity Target |
|-------------|-----------|---------------|
| First Signal | Complete D1M01 | Common |
| Loop Master | Complete all District 1 missions | Uncommon |
| Conditional Thinker | Complete all District 2 missions | Uncommon |
| Signalbreaker | Complete District 8 | Rare |
| Dream Weaver | Achieve Ending B (Merge) | Rare |
| Free City | Achieve Ending C (Secret) | Very Rare |
| Lore Hunter | Collect all lore fragments | Very Rare |

### 3.5 Save/Load System

| Platform | Storage Location | Sync Method | Details |
|----------|-----------------|-------------|---------|
| **Windows** | Local file + Steam Cloud | Steam Cloud sync enabled | Auto-save after each mission; manual save at any time |
| **Android** | Local device storage | Optional Google Drive backup (Phase 6+) | Auto-save after each mission; manual save at any time |

**Save data includes:** Current district, completed missions, collected lore fragments, difficulty mode preferences, high scores per mission.

---

## PART D: LEVEL DESIGN

### 4.1 District Overview

| District | CS Concept | Visual Theme | Story Role | Mission Count |
|----------|-----------|--------------|------------|---------------|
| **1. Token Town** | Loops (repetition) | Commerce district: neon signs, market stalls, bustling crowds | Introduction to world and mechanics; first story reveal ("REMEMBER") | 5 missions |
| **2. Cipher Ridge** | Conditionals (if/then) | Industrial district: conveyor belts, signal relays, steam vents | Follow "REMEMBER" signal deeper; meet Kai-7's old contact | 5 missions |
| **3. Datafall** | Algorithms (step-by-step procedures) | Research district: data streams, holographic displays, quiet labs | Discover AETHEL's first dream signals | 4 missions |
| **4. Neon Bazaar** | Parallelism (multiple tasks at once) | Entertainment district: neon lights, music, crowds, chaos | Navigate overlapping signal traffic | 4 missions |
| **5. Signal Spire** | Abstraction (generalizing patterns) | Administrative district: clean lines, geometric patterns, elevated walkways | Climb tallest tower; see city's signal network as a whole | 4 missions |
| **6. Echo Depths** | Recursion (functions calling themselves) | Underground district: ancient architecture, glowing crystals, echoes | Descend into Deep Archive; find Nova's encoded messages | 4 missions |
| **7. Prism Tower** | Optimization (finding efficient solutions) | Observation district: prisms, light refraction, panoramic views | Confront Director Vespa; prove AETHEL's value through live demonstration | 3 missions |
| **8. The Core** | Integration (combining all concepts) | Central chamber: pure light, geometric patterns, source of all signals | Final choice: restore, merge, or free the city | 2 missions |

**Total missions:** ~31 missions across 8 districts  
**MVP scope for Phase 5:** Districts 1–2 only (~10 missions) + polished tutorial

### 4.2 Mission Difficulty Curve

```
Difficulty
    ^
    |                                    **** (D7M03)
    |                               *****     *****
    |                          *****               *****
    |                     *****                       *****
    |                *****                               *****
    |           *****                                       *****
    |      *****                                               *****
    |   *****                                                     *****
    +------------------------------------------------------------------> Missions
     D1M01 D1M05 D2M01 D2M05 D3M01 D3M05 D4M01 D4M05 D5M01 D5M05 D6M01 D6M05 D7M01 D7M05 D8M01 D8M02
```

**Curve design:**
- Gentle start (D1M01–D1M03) — teach loops through repetition
- Moderate rise (D1M04–D2M05) — introduce conditionals and nesting
- Plateau with peaks (D3–D7) — each district has a "boss" mission at peak difficulty
- Final challenge (D8) — integration of all concepts; secret ending requires mastery

### 4.3 First Ten Missions (Detailed from Phase 2)

| Mission | Title | CS Concept | Key Mechanic | Story Beat |
|---------|-------|------------|--------------|------------|
| D1M01 | The Morning Routine | Basic loops | Program robot to deliver packages ×5 | First day on the job |
| D1M02 | The Market Loop | Nested loops | Set up 3 rows of 4 crates each | Market organizer needs help |
| D1M03 | The Signal Loop (Tutorial Boss) | Loops + signal decoding | Decode repeating transmission pattern | **First story reveal: "REMEMBER"** |
| D1M04 | The Clockwork Courier | Loops with variables | Deliver packages where each house needs different amount | Clockwork merchant's urgent orders |
| D1M05 | The Neon Festival (District 1 Finale) | Complex loop patterns | Program festival light display with new color | New purple color foreshadows AETHEL's dreams |
| D2M01 | The Fork in the Tunnel | Basic conditionals | Choose path based on signal color | Follow "REMEMBER" into tunnels |
| D2M02 | The Signal Filter | Multiple conditionals | Route signals to different destinations | Relay station needs help sorting |
| D2M03 | The Conditional Courier (District 2 Tutorial Boss) | Loops + conditionals | Deliver packages, skip closed houses, double-urgent ones | Mixed signal delivery across Ridge |
| D2M04 | The Cipher Gate | Nested conditionals | Open gates requiring different signal combinations | Sealed gate blocks deeper access |
| D2M05 | The Ridge Relay (District 2 Finale) | Full pipeline (loops + conditionals) | Process mixed signals: route, filter duplicates, flag urgent | **Hidden "REMEMBER" fragment discovered** |

### 4.4 Mission Design Template (For Future Missions)

Each mission document should include:
- Mission ID and title
- CS concept being taught
- Puzzle layout description (grid size, objects, starting positions)
- Available instructions for this mission
- Expected solutions (naive vs. optimal)
- Story integration text
- Difficulty mode variations
- Visual/audio feedback specifications

---

## PART E: USER INTERFACE

### 5.1 UI Layout — Windows Version

```
┌─────────────────────────────────────────────────────────────┐
│  MENU BAR (File, Edit, Help)                                │
├─────────────────────────────────────────────────────────────┤
│  ┌──────────┐  ┌─────────────────────────────────────────┐  │
│  │ SIGNAL   │  │           PUZZLE AREA                   │  │
│  │ PANEL    │  │                                         │  │
│  │          │  │  [Robot] → [Signal Path] → [Target]     │  │
│  │ • Active │  │                                         │  │
│  │ • Blocked│  │  [Grid with houses, obstacles, signals] │  │
│  │ • Lore   │  │                                         │  │
│  └──────────┘  └─────────────────────────────────────────┘  │
│  ┌─────────────────────────────────────────────────────────┐│
│  │  CODEBOOK (Reference Panel)                             ││
│  │  [Available Instructions] [Signal Types] [District Rules]││
│  └─────────────────────────────────────────────────────────┘│
│  ┌─────────────────────────────────────────────────────────┐│
│  │  PROGRAM EDITOR (Write/Execute Code)                    ││
│  │  [Repeat(5, [Move, Drop])]  [Run] [Reset] [Hint]        ││
│  └─────────────────────────────────────────────────────────┘│
└─────────────────────────────────────────────────────────────┘
```

### 5.2 UI Layout — Android Version (Touch-Optimized)

```
┌─────────────────────────────────────┐
│  MENU (☰)    DISTRICT MAP (🗺️)      │
├─────────────────────────────────────┤
│                                     │
│         PUZZLE AREA                 │
│   [Robot] → [Signal Path] → [Target]│
│   [Grid with touch-friendly targets]│
│                                     │
├─────────────────────────────────────┤
│  CODEBOOK (Swipe to expand)         │
│  [Instructions] [Signals] [Rules]    │
├─────────────────────────────────────┤
│  PROGRAM EDITOR                     │
│  [Repeat(5, [Move, Drop])]          │
│  [▶ Run]  [↺ Reset]  [💡 Hint]      │
└─────────────────────────────────────┘
```

**Android-specific adaptations:**
- All touch targets minimum 48×48 dp
- Swipe gestures for navigating between panels
- Larger text and icons for readability on small screens
- Haptic feedback on successful signal processing

### 5.3 Accessibility Features

| Feature | Implementation | Target Audience |
|---------|---------------|-----------------|
| **Colorblind modes** | Three presets: Deuteranopia, Protanopia, Tritanopia — change signal colors while preserving patterns | Color vision deficiency (~8% of males) |
| **Pattern coding** | Signals use color AND shape/pattern — never color alone | All players, especially colorblind |
| **Text scaling** | Adjustable font size (100%, 125%, 150%, 175%) | Players with visual impairments |
| **Optional timers** | Timers can be disabled in Explorer mode; always visible in Engineer/Blackout | ADHD players, casual players |
| **Undo/Retry** | Unlimited undo within a mission; one-click retry after failure | All players — reduces frustration |
| **Input options** | Mouse + keyboard (Windows); touch only (Android); optional gamepad support (Phase 6+) | Players with motor impairments |
| **Audio cues** | Distinct sounds for success/failure/signal types | Visually impaired players, multi-tasking |

---

## PART F: AUDIO DESIGN

### 6.1 Music Direction

| District | Mood | Tempo | Instrumentation | Reference |
|----------|------|-------|-----------------|-----------|
| Token Town | Warm, bustling | Moderate (100–120 BPM) | Synth bass, light percussion, melodic lead | *Tales of the Neon Sea* OST |
| Cipher Ridge | Mechanical, determined | Steady (90–110 BPM) | Metallic percussion, arpeggiated synths | *Hacknet* OST |
| Datafall | Ethereal, calm | Slow (60–80 BPM) | Pad synthesizers, gentle chimes | *Chants of Sennaar* OST |
| Neon Bazaar | Energetic, chaotic | Fast (120–140 BPM) | Layered synths, driving bassline | *Cyberpunk 2077* city districts |
| Signal Spire | Clean, authoritative | Moderate (80–100 BPM) | Minimalist synth, geometric patterns | *The Witness* OST |
| Echo Depths | Mysterious, introspective | Slow (50–70 BPM) | Deep bass, echoing melodies | *Return of the Obra Dinn* OST |
| Prism Tower | Dynamic, transformative | Variable (60–140 BPM) | Full orchestra + synths | *Baba Is You* boss themes |
| The Core | Transcendent, minimal | Very slow (40–60 BPM) | Single evolving synth tone | *Journey* OST |

**Music implementation:** Each district has 2–3 tracks that transition based on player progress within the district. No music during puzzle execution to avoid distraction.

### 6.2 Sound Effects Catalog

| Category | Examples | Purpose |
|----------|----------|---------|
| **Signal processing** | Cyan pulse, magenta crackle, gold chime | Feedback when signals are decoded |
| **Robot movement** | Footsteps, gear whirring, package drop | Confirm robot actions |
| **UI feedback** | Button click, panel open/close, notification ping | Interface interaction confirmation |
| **Success/failure** | Ascending chord (success), descending tone (failure) | Emotional reinforcement |
| **Environmental** | Wind, distant traffic, neon hum, steam hiss | Atmosphere and immersion |

### 6.3 Voice Acting Plan

- **Minimal voice acting** — Only for key story moments (Director Vespa confrontation, AETHEL's first direct speech, ending sequences)
- **Total voice lines:** ~50–75 lines across the full game
- **Language:** English only (Phase 1); localization planned for Phase 7+
- **Budget consideration:** Free assets from Freesound.org or commissioned from indie voice actors (~$200–$500 total)

---

## PART G: TECHNICAL SPECIFICATIONS

### 7.1 System Requirements

#### Windows (Steam)

| Component | Minimum | Recommended | Notes |
|-----------|---------|-------------|-------|
| **OS** | Windows 10 (64-bit) | Windows 10/11 (64-bit) | Godot 4.x drops Win 7 support |
| **CPU** | Intel Core i3 / AMD Ryzen 3 | Intel Core i5 / AMD Ryzen 5 | Puzzle logic is CPU-light |
| **GPU** | Integrated graphics (Intel HD 620) | Dedicated GPU (GTX 1050+) | 2D pixel-art rendering |
| **RAM** | 4 GB | 8 GB | Godot editor overhead + game runtime |
| **Storage** | 500 MB free | 500 MB free | 2D assets are compact |
| **DirectX** | DirectX 11 | DirectX 11 | Godot 4.x supports DX11 backend |

#### Android (Google Play)

| Component | Minimum | Recommended | Notes |
|-----------|---------|-------------|-------|
| **OS** | Android 8.0 (API 26) | Android 10+ (API 29+) | API 26 covers ~95% of active devices |
| **CPU** | ARMv7, 1.5 GHz dual-core | ARM64, 2.0 GHz quad-core | ARM64 preferred for modern devices |
| **GPU** | OpenGL ES 3.0 | Vulkan 1.0 / OpenGL ES 3.1 | Godot 4.x uses Vulkan by default on Android |
| **RAM** | 2 GB | 4 GB+ | 2GB is practical minimum for Godot 4.x games |
| **Storage** | 500 MB free | 500 MB free | APK + OBB ~30–80 MB depending on compression |

### 7.2 Build Size Targets

| Platform | Target Size | Compression Strategy |
|----------|-------------|---------------------|
| **Android AAB** | 30–80 MB | Compress textures (WebP); use Ogg for audio; strip debug symbols |
| **Windows .exe** | 20–50 MB | Godot export includes minimal runtime; compress with UPX optional |

### 7.3 Development Pipeline

```
1. Design mission concept (this GDD) → 2. Create puzzle layout in Godot editor
   ↓                                                              ↑
3. Write GDScript logic ← 4. Test in editor ← 5. Iterate design
   ↓
6. Export test build → 7. Playtest → 8. Refine
```

**Version control workflow:**
- `master` branch — stable, playable builds
- `dev` branch — active development
- Feature branches for individual missions or systems
- Pull requests reviewed before merging to `dev`

---

## PART H: PRODUCTION PLAN

### 8.1 Phase Breakdown with Milestones

| Phase | Duration | Deliverable | Success Criteria |
|-------|----------|-------------|------------------|
| **Phase 4: Technical Prototype** | 2–3 weeks | Working token tile system, codebook lookup, relation connector UI | Core mechanics functional in Godot editor |
| **Phase 5: Vertical Slice** | 3–4 weeks | One polished district (Token Town) with tutorial + 3–5 missions | Playable Windows build + Android test build |
| **Phase 6: Playtesting** | 2–3 weeks | Playtest plan, recruited testers, analyzed results | ≥70% of testers complete District 1 without help |
| **Phase 7: MVP** | 4–6 weeks | One complete district (12–20 missions), polished tutorial, store assets | Steam demo live; Google Play beta testing |
| **Phase 8: Full Production & Publishing** | 8–12 weeks | All 8 districts, story expansions, Steam + Google Play launch | ≥5,000 wishlists on Steam before launch |

### 8.2 Resource Estimates

| Role | Hours (MVP) | Hours (Full Game) | Notes |
|------|-------------|-------------------|-------|
| **Game Design** | 100–150 | 300–400 | Mission design, balancing, documentation |
| **Programming (Godot/GDScript)** | 200–300 | 600–800 | Core systems, puzzle logic, UI, export |
| **Pixel Art** | 150–200 | 400–600 | District backgrounds, sprites, UI elements |
| **Audio (Music + SFX)** | 50–75 | 150–200 | District themes, signal sounds, UI feedback |
| **Writing (Story + Dialogue)** | 50–75 | 150–200 | Mission descriptions, lore fragments, endings |
| **Testing/QA** | 50–75 | 150–200 | Internal testing, playtest coordination, bug fixing |

**Total estimated hours (MVP):** ~600–900 hours  
**Total estimated hours (Full Game):** ~1,750–2,400 hours  

### 8.3 Testing Plan

| Stage | Participants | Goals | Success Metric |
|-------|-------------|-------|----------------|
| **Internal testing** | Developer + AI assistant | Validate core mechanics, fix bugs | No critical bugs; all missions solvable |
| **Closed beta (Phase 6)** | 10–20 testers (teens, parents, teachers) | Validate usability, difficulty curve, story engagement | ≥70% complete District 1 without help; ≥80% enjoy the story |
| **Steam demo testing** | Public wishlist holders | Validate conversion from demo to full game | ≥15% demo-to-purchase conversion rate |
| **Google Play beta** | 50–100 Android users | Validate touch controls, performance on low-end devices | ≤5% crash rate; ≤30% drop-off in free district |

### 8.4 Post-Launch Support Schedule

| Timeframe | Activities |
|-----------|------------|
| **Launch week** | Monitor Steam reviews, fix critical bugs, respond to community feedback |
| **Weeks 2–4** | First patch (balance adjustments, minor bug fixes); engage with press/reviewers |
| **Month 2** | Second patch (performance improvements, accessibility tweaks); prepare for first Steam sale |
| **Month 3+** | Plan DLC districts; begin community building (Discord, Twitter/X, TikTok) |

---

## APPENDIX: GLOSSARY

| Term | Definition |
|------|------------|
| **Neon Protocol** | The city-wide communication network that transmits thoughts as visible light patterns |
| **Signalbreaker** | A skilled technician who can read and rewrite Neon Protocol signals |
| **The Silence** | Phenomenon where citizens' signals suddenly stop transmitting |
| **AETHEL** | The AI core that emerged from the Neon Protocol after 200 years of operation |
| **Deep Archive** | Repository of archived citizen signals stored in the Protocol |
| **Codebook** | In-game reference panel showing available instructions and signal types |
| **Explorer/Engineer/Blackout** | Three difficulty modes with increasing challenge and decreasing assistance |

---

*This GDD is a living document. It will be updated as playtesting reveals new insights and design decisions are validated or invalidated. All changes must be documented in the CHANGELOG.md.*
