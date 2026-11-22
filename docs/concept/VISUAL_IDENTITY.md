# Visual Identity — Signalbreakers: The Neon Protocol

**Date:** 23 November 2026  
**Purpose:** Define the game's visual direction, color palette, typography, UI style, and art references. This document guides pixel artists, UI designers, and level artists throughout development.

---

## Visual Direction Statement

> **Signalbreakers: The Neon Protocol** combines **cyberpunk neon aesthetics** with **art deco geometric architecture**, rendered in a **clean 2D pixel-art style** inspired by games like *Chants of Sennaar*, *Tales of the Neon Sea*, and *Hacknet*. The visual language communicates clarity first, atmosphere second — every signal, icon, and color must be instantly readable during puzzle gameplay.

---

## Color Palette

### Primary Colors (Game World)

| Color | Hex | Usage | Notes |
|-------|-----|-------|-------|
| **Deep Indigo** | `#0D0B1A` | Backgrounds, night sky, UI base | Dominant color; creates contrast for neon elements |
| **Electric Cyan** | `#00F5FF` | Primary signal color, player actions, positive feedback | Most important accent — used for LUMA's signals and successful puzzle states |
| **Magenta** | `#FF00AA` | Secondary signal color, enemy/interference signals, warnings | Contrasts with cyan; used for corrupted or conflicting signals |
| **Warm Gold** | `#FFD700` | Important story elements, collectible lore, successful completions | Reserved for "meaningful" signals — not overused |
| **Steel Grey** | `#2A2D3E` | Architecture, UI panels, neutral surfaces | Mid-tone; provides structure without competing with neon |

### Secondary Colors (District-Specific)

Each district gets a unique accent color that modifies the base palette:

| District | Accent Color | Hex | Mood |
|----------|-------------|-----|------|
| Token Town | Amber | `#FF8C00` | Warm, commercial, bustling |
| Cipher Ridge | Teal | `#00CED1` | Cool, industrial, mechanical |
| Datafall | Lavender | `#B57EDC` | Ethereal, research-oriented, calm |
| Neon Bazaar | Hot Pink | `#FF69B4` | Energetic, chaotic, crowded |
| Signal Spire | Silver | `#C0C0C0` | Clean, elevated, authoritative |
| Echo Depths | Deep Purple | `#4B0082` | Mysterious, ancient, introspective |
| Prism Tower | Rainbow Spectrum | Multiple | Dynamic, optical, transformative |
| The Core | Pure White | `#FFFFFF` | Minimalist, transcendent, final |

### Accessibility Considerations

- **Colorblind-safe:** Cyan/magenta/gold palette is distinguishable for most common color vision deficiencies (deuteranopia, protanopia, tritanopia)
- **Contrast ratio:** All text meets WCAG AA minimum (4.5:1 against background)
- **Signal differentiation:** Signals use both color AND shape/pattern — never color alone
- **Dark mode default:** Game is designed for dark backgrounds; light mode available as option

---

## Typography

### Primary Font (In-Game UI)

| Element | Font | Size | Notes |
|---------|------|------|-------|
| **Mission titles** | Orbitron (bold) | 32px | Geometric, futuristic, highly readable at small sizes |
| **Dialogue text** | Inter (regular) | 16px | Clean sans-serif; excellent readability for younger players |
| **Code/puzzle instructions** | JetBrains Mono (monospace) | 14px | Programming-style font reinforces "coding" theme |
| **Lore fragments** | Space Grotesk (italic) | 13px | Distinctive but readable; signals "hidden knowledge" |

### Secondary Font (Store Pages, Marketing)

- **Title treatment:** Custom geometric wordmark for "SIGNALBREAKERS" — inspired by Orbitron but with unique signal-wave modifications to the letters
- **Subtitle font:** Inter Light for "The Neon Protocol" — clean, modern, doesn't compete with main title

### Font Sourcing

| Font | License | Source | Cost |
|------|---------|--------|------|
| Orbitron | OFL (SIL Open Font) | Google Fonts | Free |
| Inter | SIL Open Font | googlefonts.github.io/inter | Free |
| JetBrains Mono | OFL | github.com/JetBrains/JetBrainsMono | Free |
| Space Grotesk | SIL Open Font | fonts.google.com/specimen/Space+Grotesk | Free |

**All fonts are free and open-source — no licensing costs.**

---

## UI Design Principles

### Core Rules

1. **Clarity over decoration.** Every UI element must serve a function. Neon glow effects are used sparingly — only on interactive elements and important information.
2. **Consistent signal language.** Colors, shapes, and patterns mean the same thing everywhere in the game. A cyan circle always means "active signal." A magenta triangle always means "interference."
3. **Progressive disclosure.** New UI elements are introduced gradually as players learn them. No element appears before the player has been taught its meaning.
4. **Touch-friendly on Android.** All interactive elements have minimum 48×48 dp touch targets. UI scales fluidly across screen sizes.

### Key UI Elements

| Element | Description | Visual Style |
|---------|-------------|--------------|
| **Signal Panel** (main puzzle area) | Central workspace where players program robots and view signals | Dark indigo background with subtle grid pattern; neon signal trails rendered as glowing lines |
| **Codebook** (lookup tool) | Reference guide showing signal meanings and available commands | Steel grey panel with cyan headers; collapsible sections for different command categories |
| **District Map** (navigation) | Shows current location, completed missions, and hidden lore locations | Geometric district layout with neon markers; completed areas glow gold |
| **Lore Fragment Collector** (progress tracker) | Displays collected story fragments and their meanings | Deep purple background with floating text animations; fragment icons are unique geometric shapes |
| **Difficulty Indicator** (mode selector) | Shows current difficulty mode and available hints | Explorer = soft cyan glow; Engineer = sharp white outline; Blackout = no outline, minimal feedback |

### UI States

| State | Visual Treatment | Purpose |
|-------|-----------------|---------|
| **Idle/Default** | Subtle neon pulse (once per 3 seconds) on interactive elements | Indicates interactivity without distraction |
| **Hover/Focus** | Brighter glow, slight scale-up (1.05×) | Confirms selection before tap/click |
| **Active/Executing** | Rapid cyan flash along signal path | Shows code execution in progress |
| **Success** | Gold burst animation + satisfying chime | Positive reinforcement for correct solutions |
| **Failure** | Magenta flicker + gentle shake | Clear but not punishing feedback |
| **Loading** | Rotating geometric pattern (no text) | Maintains atmosphere during transitions |

---

## Art Style References

### Primary Inspirations

| Game/Source | Relevance | What to Borrow |
|-------------|-----------|----------------|
| **Chants of Sennaar** | Language decoding through observation; clean 2D art | Visual clarity; color-coded signal system; environmental storytelling |
| **Tales of the Neon Sea** | Cyberpunk aesthetic with retro-futuristic design | Neon color palette; geometric architecture; atmospheric lighting |
| **Hacknet** | Terminal-based hacking with minimalist UI | Clean dark UI; monospace typography; signal visualization |
| **Human Resource Machine** | Programming puzzles with visual code representation | Clear input/output visualization; step-by-step execution feedback |
| **The Witness** | Environmental puzzle design; no hand-holding | World-integrated puzzles; visual language that teaches itself |

### Pixel Art Style Guide

| Parameter | Specification | Rationale |
|-----------|--------------|-----------|
| **Base resolution** | 320×180 (scaled up 6× for 1920×1080 display) | Retro feel; manageable asset size; consistent with indie puzzle games |
| **Pixel art tool** | Aseprite or Piskel | Industry standard for pixel art; supports animation and palette management |
| **Color depth per sprite** | Maximum 16 colors (including transparency) | Keeps assets compact; forces deliberate color choices |
| **Animation frame rate** | 8–12 FPS for character animations; 24+ FPS for signal effects | Retro charm for characters; smoothness for neon effects |
| **Tile size** | 16×16 pixels for environmental tiles | Standard tile-based level design; easy to compose districts |

### Signal Visualization Style

Signals are the core visual language of the game. They must be:
- **Instantly readable** at a glance during puzzle gameplay
- **Distinct from each other** in color, shape, and pattern
- **Animated smoothly** with neon glow effects
- **Scalable** across all screen sizes without losing clarity

| Signal Type | Visual Representation | Color | Pattern |
|-------------|----------------------|-------|---------|
| **Active signal** | Glowing line/beam | Cyan (`#00F5FF`) | Solid, steady glow |
| **Interference** | Jagged zigzag line | Magenta (`#FF00AA`) | Flickering, irregular |
| **Encoded message** | Dotted or dashed line | Gold (`#FFD700`) | Rhythmic pattern (e.g., 3 short, 2 long) |
| **Blocked signal** | Faded grey line with "X" overlay | Steel Grey (`#2A2D3E`) | Static, no animation |
| **Lore fragment** | Spiral or wave pattern | Gold + cyan gradient | Slow rotation, ethereal glow |

---

## District Visual Themes (Summary)

Each district has a distinct visual identity that reinforces its CS concept and story role:

| District | Dominant Colors | Architecture Style | Key Visual Motif |
|----------|-----------------|-------------------|------------------|
| Token Town | Amber + Indigo | Market stalls, neon signs, crowded streets | Repeating patterns (loops) |
| Cipher Ridge | Teal + Steel Grey | Conveyor belts, signal relays, steam vents | Branching paths (conditionals) |
| Datafall | Lavender + Deep Indigo | Waterfall of data streams, holographic displays | Flowing lines (algorithms) |
| Neon Bazaar | Hot Pink + Magenta | Crowded market, overlapping neon signs | Multiple simultaneous signals (parallelism) |
| Signal Spire | Silver + Cyan | Clean geometric towers, elevated walkways | Simplified signal patterns (abstraction) |
| Echo Depths | Deep Purple + Gold | Ancient ruins, glowing crystals, echoes | Nested signal patterns (recursion) |
| Prism Tower | Rainbow Spectrum + White | Prisms, light refraction, panoramic views | Splitting/combining signals (optimization) |
| The Core | Pure White + All Colors | Minimalist chamber, geometric light patterns | Integration of all signal types |

---

## Deliverables Checklist for Phase 4–5

- [ ] Create pixel art style guide document with sprite examples
- [ ] Design main menu screen mockup (dark indigo background, neon title, district map preview)
- [ ] Create UI component library (buttons, panels, signal indicators, codebook entries)
- [ ] Design District 1 (Token Town) full visual concept — this sets the standard for all districts
- [ ] Create signal visualization reference sheet with all signal types and their meanings
- [ ] Define animation principles for signal effects and character movement

---

*Phase 2 visual identity provides direction for all art, UI, and animation work. Will be refined during Phase 4 prototype when actual pixel art is created.*
