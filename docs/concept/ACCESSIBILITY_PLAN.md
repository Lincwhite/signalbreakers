# Accessibility Plan — Signalbreakers: The Neon Protocol

**Version:** 1.0 (Phase 3)  
**Date:** 23 November 2026  
**Purpose:** Comprehensive accessibility features covering visual, auditory, motor, and cognitive accessibility. Supports ADHD-friendly design, colorblind modes, text scaling, and input flexibility.

---

## TABLE OF CONTENTS

1. Accessibility Philosophy
2. Visual Accessibility
3. Auditory Accessibility
4. Motor Accessibility
5. Cognitive Accessibility (ADHD-Friendly Design)
6. Input Options
7. Accessibility Settings Menu
8. Testing & Validation Plan

---

## 1. ACCESSIBILITY PHILOSOPHY

> Signalbreakers is designed to be playable by anyone, regardless of ability. Accessibility is not an afterthought — it is baked into the core design from Day 1. Every feature has an accessible alternative, and no essential gameplay element relies on a single sensory modality.

### Core Principles

1. **Multiple ways to perceive information** — Never rely on color alone; never rely on sound alone
2. **Player-controlled pacing** — No forced timers; unlimited retries; skip-able story beats
3. **Customizable difficulty** — Three modes that adjust assistance, not just challenge
4. **Consistent UI patterns** — Learn once, apply everywhere; no hidden mechanics
5. **Respect player time** — Skip cutscenes; auto-save; fast mission restart

---

## 2. VISUAL ACCESSIBILITY

### Colorblind Support

| Mode | Changes Applied | Target Audience |
|------|-----------------|-----------------|
| **None (Default)** | Standard palette: cyan (#00F5FF), magenta (#FF00AA), gold (#FFD700) | Players with normal color vision |
| **Deuteranopia** | Cyan → teal (#00CED1); Magenta → purple (#9B59B6); Gold → yellow (#F1C40F) | Red-green color blindness (most common; ~6% of males) |
| **Protanopia** | Cyan → blue (#3498DB); Magenta → pink (#E91E63); Gold → orange (#F39C12) | Red-blind color blindness (~1% of males) |
| **Tritanopia** | Cyan → green (#2ECC71); Magenta → red (#E74C3C); Gold → light blue (#5DADE2) | Blue-yellow color blindness (~0.3% of population) |

### Pattern Coding (Color + Shape)

Signals are NEVER identified by color alone. Each signal type has a unique shape/pattern:

| Signal Type | Color | Shape/Pattern | Description |
|-------------|-------|---------------|-------------|
| Active | Cyan/Teal/Blue | Solid line with steady glow | Straight, unbroken |
| Interference | Magenta/Purple/Pink | Jagged zigzag with flicker | Irregular, broken |
| Encoded | Gold/Yellow/Orange | Dotted or dashed rhythm | Regular pattern (e.g., 3 short, 2 long) |
| Blocked | Steel Grey | Static/noise overlay | No animation, flat appearance |
| Lore Fragment | Gold + cyan gradient | Spiral/wave with rotation | Curved, flowing motion |

**Implementation:** Each signal sprite includes both color tint AND shape overlay. Players can identify signals even in grayscale mode.

### Text Scaling

| Setting | Font Size Multiplier | Use Case |
|---------|---------------------|----------|
| 100% (Default) | 1× | Standard readability |
| 125% | 1.25× | Mild visual impairment |
| 150% | 1.5× | Moderate visual impairment |
| 175% | 1.75× | Severe visual impairment |

**Implementation:** All UI text uses scalable font references (not baked-in textures). Godot's `Theme` resource allows runtime font size changes without layout breaking.

### High Contrast Mode

- **Toggle:** Settings → Visual → High Contrast
- **Effect:** Increases contrast ratio to meet WCAG AAA standards (7:1 minimum for text)
- **Changes:** Darker backgrounds (#05040A instead of #0D0B1A); brighter signal colors; bold outlines on all UI elements

### Grayscale Mode

- **Toggle:** Settings → Visual → Grayscale
- **Effect:** Removes all color, relies entirely on shape/pattern coding
- **Use case:** Players who prefer monochrome visuals or have specific color sensitivities

---

## 3. AUDITORY ACCESSIBILITY

### Subtitles/Captions

| Feature | Description | Configuration |
|---------|-------------|---------------|
| **Full subtitles** | All dialogue, narration, and story text displayed as captions | Always on by default; can be toggled off |
| **Speaker identification** | Caption includes speaker name in brackets: [LUMA], [AETHEL], [KAI-7] | Always visible when dialogue plays |
| **Sound effect cues** | Non-dialogue audio described in brackets: [cyan pulse], [gear whirring], [gold chime] | Toggleable in settings |
| **Subtitle styling** | High contrast text (white on dark semi-transparent background); readable font; positioned below puzzle area | Customizable position (bottom/center) and opacity |

### Audio Cues for Visual Events

Every important visual event has a corresponding audio cue:

| Visual Event | Audio Cue | Purpose |
|--------------|-----------|---------|
| Signal decoded successfully | Ascending chime (pitch varies by signal type) | Confirms success without requiring visual confirmation |
| Signal decoding failed | Descending tone | Indicates failure for visually impaired players |
| Robot moves | Gear whir + footstep | Confirms robot action |
| Package dropped | Metallic clink | Confirms package placement |
| Hint revealed | Soft bell ping | Alerts player that hint is available |
| Mission complete | District-specific melody | Celebrates completion |
| Lore fragment collected | Ethereal swell + gold chime | Rewards exploration |

### Audio Mixing Options

| Setting | Range | Default | Notes |
|---------|-------|---------|-------|
| Music Volume | 0–100% | 70% | Separate from SFX and voice |
| SFX Volume | 0–100% | 80% | Signal processing, robot movement, UI feedback |
| Voice Volume | 0–100% | 90% | Dialogue and story narration |
| Master Volume | 0–100% | 100% | Overall output level |
| Music Ducking | 0–30% reduction during dialogue | 20% | Lowers music when dialogue plays |

### Mute All

- **Keyboard shortcut:** M key (toggles all audio on/off)
- **Persistent setting:** Remembers state across sessions
- **Visual indicator:** Speaker icon with slash appears in HUD when muted

---

## 4. MOTOR ACCESSIBILITY

### Touch Controls (Android)

| Element | Minimum Size | Spacing | Notes |
|---------|-------------|---------|-------|
| Buttons | 48×48 dp | 8 dp minimum between interactive elements | Meets Android accessibility guidelines |
| Code editor text area | Full width, variable height | N/A | Supports pinch-to-zoom for text scaling |
| Instruction palette items | 60×60 dp | 12 dp spacing | Larger targets for drag-and-drop accuracy |
| Swipe gestures | 100 dp minimum swipe distance | N/A | Configurable sensitivity in settings |

### Keyboard Controls (Windows)

| Action | Default Key | Alternative | Notes |
|--------|-------------|-------------|-------|
| Move cursor | Arrow keys / WASD | Numpad | Both work simultaneously |
| Insert instruction | Click palette item or type command | Tab to cycle through available instructions | Full keyboard support for code entry |
| Run program | Enter key | Spacebar | Configurable in settings |
| Reset mission | R key | Esc → Reset button | Quick restart without leaving screen |
| Open Codebook | C key | Click Codebook toggle | Always accessible |
| Toggle hints | H key (Explorer mode) | Hint button | Contextual hint appears |
| Pause game | Escape key | P key | Both work simultaneously |
| Mute all audio | M key | Settings → Audio → Mute | Persistent setting |

### Remappable Controls

- **Platform:** Windows only (Android uses fixed touch layout)
- **Scope:** All keyboard actions can be remapped via Settings → Controls → Remap
- **Profiles:** Save multiple control profiles (e.g., "QWERTY," "Colemak," "Left-handed")
- **Import/Export:** Share control profiles with other players via file export

### Auto-Aim / Snap-to-Grid

- **Toggle:** Settings → Motor → Snap to Grid
- **Effect:** Robot movement snaps to nearest tile when within 10 pixels of grid intersection
- **Benefit:** Reduces precision requirements for motor-impaired players
- **Visual feedback:** Faint grid highlight appears when robot is near snap point

---

## 5. COGNITIVE ACCESSIBILITY (ADHD-FRIENDLY DESIGN)

### Short Mission Structure

| Metric | Value | Rationale |
|--------|-------|-----------|
| **Average mission time** | 5–10 minutes | Matches attention span for focused puzzle solving |
| **Maximum mission time** | 15 minutes (with hints disabled in Blackout mode) | Prevents frustration from overly long sessions |
| **Checkpoint frequency** | After every mission | Clear sense of progress; natural break point |

### Optional Timers

| Mode | Timer Behavior | Player Control |
|------|---------------|----------------|
| Explorer | Timer shown but NOT required; can be disabled entirely in settings | Toggle on/off in Settings → Gameplay → Show Timer |
| Engineer | Timer recommended for efficiency scoring; affects score but not completion | Optional; player chooses whether to enable |
| Blackout | Internal timer tracks speed for hidden scoring; no visible timer during play | Player sees result after submission only |

### Undo/Retry System

| Feature | Description | Limitations |
|---------|-------------|-------------|
| **Undo** | Revert last code edit (Ctrl+Z) | Unlimited undos within a mission |
| **Reset** | Clear robot position and state without clearing code | One-click reset; code preserved |
| **Retry from checkpoint** | Restart mission from last completed sub-objective | Available after first failure; prevents re-doing easy sections |
| **View Solution** | Show optimal solution after 3 failures or manual request | Hidden in Blackout mode until submission |

### Visual Clarity

| Feature | Implementation | Benefit |
|---------|----------------|---------|
| **No cluttered UI** | Only show relevant panels for current mission | Reduces cognitive load; prevents overwhelm |
| **Consistent color coding** | Same colors mean same things everywhere in the game | Learns once, applies always |
| **Progressive disclosure** | New UI elements introduced gradually as needed | Prevents information overload |
| **Clear success/failure feedback** | Distinct visual + audio cues for each outcome | Reduces uncertainty; builds confidence |

### Focus Mode (Optional)

- **Toggle:** Settings → Gameplay → Focus Mode
- **Effect:** Hides decorative background elements; simplifies puzzle area to essential grid and robot only
- **Use case:** Players who get distracted by visual noise or prefer minimal interfaces
- **Trade-off:** Slightly less atmospheric but improves concentration for complex puzzles

---

## 6. INPUT OPTIONS

### Supported Input Methods

| Input Type | Windows | Android | Notes |
|------------|---------|---------|-------|
| Mouse + Keyboard | Full support | N/A | Primary input for PC version |
| Touch (tap, swipe, drag) | Optional (touchscreen laptops) | Primary input | Optimized for 48×48 dp touch targets |
| Gamepad (Xbox/PS5) | Supported (Phase 6+) | Not supported | D-pad for navigation; A button to confirm |
| Eye tracker | Supported via Windows API (Phase 7+) | N/A | Gaze-based selection for motor-impaired players |

### Input Feedback

| Action | Visual Feedback | Audio Feedback | Haptic Feedback (Android) |
|--------|-----------------|----------------|--------------------------|
| Button press | Button highlights/scales up | Soft click sound | Short vibration pulse |
| Drag-and-drop success | Item snaps to grid with glow | Positive chime | Medium vibration pulse |
| Code execution start | Robot begins moving; instruction highlighted | Gear whirring sound | Continuous light vibration during movement |
| Mission complete | Gold burst animation + confetti particles | Full chord progression | Strong vibration pulse sequence |

---

## 7. ACCESSIBILITY SETTINGS MENU

### Settings Hierarchy

```
Settings
├── Visual
│   ├── Colorblind Mode (None / Deuteranopia / Protanopia / Tritanopia)
│   ├── Text Scale (100% / 125% / 150% / 175%)
│   ├── High Contrast (On / Off)
│   └── Grayscale Mode (On / Off)
├── Audio
│   ├── Music Volume (Slider: 0–100%)
│   ├── SFX Volume (Slider: 0–100%)
│   ├── Voice Volume (Slider: 0–100%)
│   ├── Master Volume (Slider: 0–100%)
│   └── Mute All (Toggle)
├── Gameplay
│   ├── Default Difficulty Mode (Explorer / Engineer / Blackout)
│   ├── Show Timer (On / Off)
│   ├── Focus Mode (On / Off)
│   ├── Auto-Save Frequency (After every mission / Every 3 missions)
│   └── Skip Story Beats (On / Off — skips to next puzzle after story text)
├── Motor
│   ├── Snap to Grid (On / Off)
│   └── Touch Sensitivity (Low / Medium / High) [Android only]
├── Controls [Windows only]
│   ├── Remap Keys...
│   ├── Load Profile...
│   └── Save Profile As...
└── About
    └── Accessibility Features List (links to this document)
```

### Accessibility Statement (In-Game)

> Signalbreakers is designed to be accessible to players of all abilities. This game includes colorblind modes, text scaling, subtitles, optional timers, unlimited retries, and multiple input methods. Full accessibility documentation is available in the settings menu under "About → Accessibility Features List."
>
> For questions or feedback, contact: accessibility@signalbreakers.game

---

## 8. TESTING & VALIDATION PLAN

### Internal Testing Checklist

| Test | Tool/Method | Pass Criteria |
|------|-------------|---------------|
| Colorblind simulation | Godot shader preview with colorblind filters | All signals distinguishable in all 3 colorblind modes |
| Text readability | Zoom to 175% text scale; read all UI text at arm's length | No blurring or clipping; all text legible |
| Subtitle timing | Play through all dialogue scenes; verify captions match audio | Captions appear within 200ms of speech; remain on screen for minimum 3 seconds |
| Touch target size | Measure all interactive elements on Android build | Minimum 48×48 dp for all buttons and controls |
| Keyboard navigation | Navigate entire UI using only keyboard (Tab, Arrow keys, Enter) | All menu items reachable; no mouse required |

### External Playtesting Focus

| Participant Type | Number | Accessibility Features to Test |
|------------------|--------|-------------------------------|
| Colorblind players | 3–5 | Colorblind mode effectiveness; pattern coding clarity |
| ADHD players | 3–5 | Mission length appropriateness; optional timer usefulness; focus mode benefit |
| Motor-impaired players | 2–3 | Snap-to-grid accuracy; touch target size; keyboard remapping ease |
| Visually impaired players | 2–3 | Text scaling readability; audio cue clarity; subtitle timing |
| Teachers/Educators | 3–5 | Classroom usability; accessibility features for diverse student needs |

### Accessibility Certification Targets

| Standard | Target Date | Notes |
|----------|-------------|-------|
| **WCAG 2.1 AA** | Phase 7 (MVP launch) | Web-based store page and privacy policy meet WCAG AA |
| **Steam Accessibility Features** | Phase 5 (Vertical Slice) | Tag game with relevant accessibility features on Steam store page |
| **Google Play Accessibility Rating** | Phase 7 (MVP launch) | Achieve "Good" or better rating in Google Play accessibility assessment |

---

*This accessibility plan supports all development through Phase 8. Features may be added or refined based on playtesting feedback and player requests.*
