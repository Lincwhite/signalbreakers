# Player Personas — Signalbreakers Research

**Date:** 22 November 2026  
**Purpose:** Define six target player archetypes to guide design decisions, difficulty curves, and marketing messaging.

---

## Persona Overview

Signalbreakers targets a broad but specific audience: players who enjoy cerebral puzzles with narrative depth, aged roughly 10–35, spanning from curious beginners to experienced programmers. The six personas below represent the primary segments the game must serve.

---

## Persona 1: "Curious Alex" — The Young Explorer

| Attribute | Details |
|-----------|---------|
| **Age** | 10–13 |
| **Platform** | Android (parent-purchased), later Windows |
| **Gaming experience** | Moderate — plays Roblox, Minecraft, Among Us |
| **Coding experience** | None or minimal — may have tried Scratch |
| **Motivation** | Wants to feel smart; enjoys solving puzzles that "click"; likes stories and mysteries |
| **Pain points** | Gets frustrated by text-heavy instructions; gives up if a puzzle feels too hard for too long |
| **What makes them stay** | Short missions (5–10 min); visual feedback when code runs; story progression; collecting badges/achievements |
| **Purchase driver** | Parent buys on Steam or Google Play; attracted by "learn coding while playing" messaging |
| **Preferred difficulty** | Explorer mode — generous hints, no timers, forgiving scoring |
| **Key design needs** | Large touch targets (Android); visual code representation (not just text); clear success/failure feedback; optional reading-aloud for instructions |

### Design Implications
- Tutorial mission must be playable in under 15 minutes with clear wins.
- Codebook lookup should use color-coding and icons, not just numbers.
- Explorer mode hints should explain the "why," not just give the answer.

---

## Persona 2: "Determined Sam" — The Teen Engineer

| Attribute | Details |
|-----------|---------|
| **Age** | 14–17 |
| **Platform** | Windows (Steam), Android for casual play |
| **Gaming experience** | Strong — plays strategy games, RPGs, puzzle games |
| **Coding experience** | Some — school Python/JavaScript, maybe personal projects |
| **Motivation** | Wants to prove they can solve "hard" puzzles; enjoys feeling like a hacker; likes progression systems |
| **Pain points** | Gets bored if puzzles are too easy or repetitive; wants meaningful challenge without hand-holding |
| **What makes them stay** | Engineer mode with moderate hints; leaderboard rankings; district completion milestones; unlockable lore entries |
| **Purchase driver** | Own purchase money (gifts, allowance); attracted by cyberpunk aesthetic and "real coding concepts" |
| **Preferred difficulty** | Engineer mode — balanced hints, optional timers, scoring based on efficiency |
| **Key design needs** | Efficient solution tracking; replayability for optimization; lore/lore-fragment collection; Steam achievements |

### Design Implications
- Engineer mode should reward code elegance (fewer instructions, cleaner logic), not just correctness.
- Lore fragments should be discoverable through exploration, not forced reading.
- Leaderboards should be per-district or per-mission to avoid discouragement from top players.

---

## Persona 3: "Experienced Jordan" — The Veteran Coder

| Attribute | Details |
|-----------|---------|
| **Age** | 20–35 |
| **Platform** | Windows (Steam) primary, Android secondary |
| **Gaming experience** | Strong — plays Zachtronics games, roguelikes, strategy games |
| **Coding experience** | Significant — professional or serious hobbyist programmer |
| **Motivation** | Enjoys elegant solutions; appreciates well-designed puzzle systems; wants to beat their own best times |
| **Pain points** | Games that "teach coding" but are actually just drag-and-drop; puzzles with obvious brute-force solutions |
| **What makes them stay** | Blackout mode (no hints, no feedback until submission); optimization leaderboards; complex multi-step missions in later districts |
| **Purchase driver** | Steam sale discovery; recommendation from Zachtronics fans; "real computational thinking" claim |
| **Preferred difficulty** | Blackout mode — submit-only evaluation, no intermediate feedback, efficiency scoring |
| **Key design needs** | Solution comparison tool (see how others solved it); code export/share; Steam Workshop support for custom missions |

### Design Implications
- Blackout mode must feel fair: solutions should have clear optimal paths, not rely on guessing.
- Include a "solution viewer" that shows other players' approaches after completion.
- Consider Steam Workshop integration for community-created missions (Phase 7+).

---

## Persona 4: "Parent Taylor" — The Purchasing Decision-Maker

| Attribute | Details |
|-----------|---------|
| **Age** | 35–50 |
| **Platform** | Android (purchases for child), Windows (may play alongside) |
| **Gaming experience** | Moderate — plays casual/mobile games, some PC gaming |
| **Coding experience** | Minimal — understands basics but won't play the puzzles themselves |
| **Motivation** | Wants screen time that's "good for my kid"; attracted by educational value; wants no ads/no IAPs |
| **Pain points** | Apps with hidden subscriptions; games that feel like worksheets; unclear learning outcomes |
| **What makes them buy** | Clear age range (10+); "no ads, no loot boxes" promise; parent dashboard showing progress; positive reviews mentioning educational value |
| **Purchase driver** | Google Play or Steam purchase for child; attracted by "learn computational thinking" messaging |
| **Key design needs** | Store page clearly states learning outcomes; optional parent progress report; offline play (no forced online); data privacy focused |

### Design Implications
- Store description must lead with educational value, not just gameplay.
- Include a simple "what your child learned" summary after each district.
- Offline-first design is essential for mobile parents concerned about data/ads.

---

## Persona 5: "Teacher Morgan" — The Classroom Integrator

| Attribute | Details |
|-----------|---------|
| **Age** | 25–55 |
| **Platform** | Windows (school lab), Android (personal) |
| **Gaming experience** | Moderate — uses educational tech tools, may not game personally |
| **Coding experience** | Some — runs school coding club or CS elective |
| **Motivation** | Needs engaging material that aligns with curriculum; wants students to practice concepts outside class |
| **Pain points** | Games that don't map to learning standards; too expensive for classroom licensing; no progress tracking |
| **What makes them use it** | Free introductory district on Android (students can try without purchase); clear mapping to CS concepts; printable worksheets or discussion prompts |
| **Purchase driver** | School/district license (~$5/student) or individual student purchases via Steam family sharing |
| **Key design needs** | Mission tags mapped to CS concepts (loops, conditionals, algorithms); optional teacher guide PDF; no time pressure for classroom use |

### Design Implications
- Tag each mission with underlying CS concept(s).
- Provide a free downloadable teacher guide (PDF) with discussion questions.
- Consider a "classroom mode" that disables leaderboards and timers.

---

## Persona 6: "Casual Riley" — The Story Puzzle Fan

| Attribute | Details |
|-----------|---------|
| **Age** | 18–35 |
| **Platform** | Windows (Steam) primary |
| **Gaming experience** | Strong — plays narrative puzzle games (Chants of Sennaar, Return of the Obra Dinn, The Witness) |
| **Coding experience** | Light to moderate — may have tried CodeCombat or similar |
| **Motivation** | Loves solving mysteries; enjoys beautiful worlds and compelling stories; doesn't mind some challenge but won't grind |
| **Pain points** | Puzzles that feel disconnected from the story; excessive text without visual support |
| **What makes them stay** | Strong narrative hook (LUMA-9 mystery); cyberpunk aesthetic; puzzles that feel like "decoding transmissions" rather than "writing code"; satisfying story reveals |
| **Purchase driver** | Steam store discovery; positive reviews mentioning story and atmosphere; wishlist from Steam tags |
| **Preferred difficulty** | Explorer or Engineer mode — willing to struggle but wants narrative payoff |
| **Key design needs** | Story progression tied to puzzle completion; atmospheric audio/visual design; lore that rewards curiosity |

### Design Implications
- Narrative must be the primary driver; puzzles are the vehicle, not the destination.
- Cyberpunk aesthetic is a key differentiator — invest in visual identity early.
- Avoid "coding worksheet" feel by framing puzzles as decoding/hacking tasks within the story world.

---

## Persona Priority Matrix

| Priority | Personas | Rationale |
|----------|----------|-----------|
| **P0 (Primary)** | Curious Alex, Determined Sam, Casual Riley | Core player base; drive reviews and word-of-mouth on Steam |
| **P1 (Secondary)** | Experienced Jordan, Parent Taylor | Jordan validates depth for Zachtronics fans; Taylor drives mobile purchases |
| **P2 (Tertiary)** | Teacher Morgan | Important for long-tail distribution but not critical for MVP launch |

---

## Cross-Persona Design Principles

1. **Three difficulty modes serve all personas:** Explorer (Alex, Riley), Engineer (Sam, Jordan), Blackout (Jordan).
2. **Story is the universal hook:** Every persona stays for narrative payoff, even if they're primarily puzzle-focused.
3. **Offline-first benefits everyone:** No forced online play, no ads on mobile, works on low-end devices.
4. **Visual code representation bridges experience gaps:** Alex sees colored blocks; Jordan sees efficient assembly-like code; both are solving the same logical problem.
5. **No single persona requires a unique platform:** Windows and Android serve all six, with different store strategies (Steam premium vs. Google Play freemium).

---

## Open Questions

| Question | Impact | Next Step |
|----------|--------|-----------|
| Should the Android version include parent dashboard? | P1 persona fit | Research competing apps' parent features |
| Is Steam Workshop feasible for MVP? | Jordan persona satisfaction | Assess Godot Workshop integration complexity |
| What CS concepts map to which districts? | Teacher Morgan + curriculum alignment | Draft concept-to-district mapping in Phase 3 |
| Should leaderboards be global or per-mission? | Sam/Jordan engagement | Playtest both approaches |

---

*Next: PLATFORM_REQUIREMENTS.md — Windows and Android platform specifications, system requirements, and store submission requirements.*
