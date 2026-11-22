# First Ten Mission Concepts — Signalbreakers

**Date:** 23 November 2026  
**Purpose:** Define the first ten missions (covering Districts 1–2, plus preview missions from later districts) with puzzle mechanics, learning objectives, and story integration. These are design concepts — not final implementations.

---

## Mission Design Framework

Each mission follows this structure:

| Element | Description |
|---------|-------------|
| **Mission ID** | District.MissionNumber (e.g., D1M03 = District 1, Mission 3) |
| **Title** | In-game name for the mission |
| **CS Concept** | The computational thinking concept being taught |
| **Puzzle Type** | The core mechanic players use to solve it |
| **Learning Objective** | What the player understands after completing this mission |
| **Story Integration** | How the narrative advances during/after the puzzle |
| **Difficulty Mode Notes** | How Explorer/Engineer/Blackout modes affect this mission |

---

## District 1: Token Town — Loops (Repetition)

### Mission D1M01: "The Morning Routine"

| Element | Details |
|---------|---------|
| **CS Concept** | Introduction to loops — repeating a sequence of actions |
| **Puzzle Type** | Program a delivery robot to drop packages at 5 houses in order |
| **Learning Objective** | Players understand that "repeat N times" is more efficient than writing each step individually |
| **Story Integration** | LUMA's first day on the job. A nervous new technician asks for help delivering morning mail before the market opens. |
| **Explorer Mode** | Shows a hint: "Notice how steps 1–4 repeat? Try using Repeat." |
| **Engineer Mode** | No hints; scores based on number of instructions used (fewer = better) |
| **Blackout Mode** | Submit-only evaluation; no feedback until the robot completes or fails |

**Puzzle Layout:**
- 5 houses arranged in a row along a street
- Robot starts at the post office with 5 packages
- Player must program: Move → Drop Package (×5)
- Solution A (naive): Move, Drop, Move, Drop, Move, Drop, Move, Drop, Move, Drop = 10 instructions
- Solution B (optimal): Repeat(5, [Move, Drop]) = 2 instructions

**Visual Feedback:** Packages glow gold when delivered. Houses light up sequentially.

---

### Mission D1M02: "The Market Loop"

| Element | Details |
|---------|---------|
| **CS Concept** | Nested loops — repeating a pattern within a pattern |
| **Puzzle Type** | Program a robot to set up market stalls: arrange 3 rows of 4 crates each |
| **Learning Objective** | Players understand that loops can contain other loops (nesting) |
| **Story Integration** | The market organizer needs help setting up before the Neon Bazaar opens. "We need three rows, four crates per row — but I only have one robot." |
| **Explorer Mode** | Shows: "You already know how to repeat 4 times. Now think about doing that 3 times." |
| **Engineer Mode** | Scores on instruction count; also tracks whether player used nested loops vs. flat repetition |
| **Blackout Mode** | Same as D1M01 Blackout — submit-only evaluation |

**Puzzle Layout:**
- Grid of 3 rows × 4 columns (12 crate positions)
- Robot starts at corner with 12 crates
- Player must program: Repeat(3, [Repeat(4, [Move, Place]), MoveRight])
- Visual: Crates form a grid pattern as robot places them

**Key Insight:** This is the first mission where nested loops feel "necessary" — writing it flat would be 12 instructions vs. 3 with nesting.

---

### Mission D1M03: "The Signal Loop" (Tutorial Boss)

| Element | Details |
|---------|-------------|
| **CS Concept** | Loops applied to signal processing — repeating a decoding pattern |
| **Puzzle Type** | Program LUMA's signal decoder to process a repeating transmission pattern |
| **Learning Objective** | Players apply loop concept to the game's core mechanic (signal decoding) for the first time |
| **Story Integration** | LUMA receives a repeating signal from an unknown sender. The pattern is: "GOLD-CYAN-GOLD-CYAN..." repeated 10 times. LUMA must decode it by recognizing the loop. |
| **Explorer Mode** | Highlights the repeating section with a gold border; hint text: "This part repeats. Can you tell the decoder to repeat too?" |
| **Engineer Mode** | Requires player to identify both the pattern AND the repetition count (10) without being told either |
| **Blackout Mode** | Signal plays once; player must remember the pattern and program the loop from memory |

**Puzzle Layout:**
- Signal waveform displayed as colored bars (gold/cyan alternating)
- Player programs decoder: Repeat(10, [DecodeGold, DecodeCyan])
- On success: The decoded message reveals "REMEMBER" — the first clue of the central mystery
- Visual: Waveform collapses into a single clean signal; text "REMEMBER" appears in gold

**Significance:** This is the **first story reveal**. Players who complete this mission have unlocked the game's central mystery. It ties the mechanical concept (loops) to the narrative hook ("REMEMBER").

---

### Mission D1M04: "The Clockwork Courier"

| Element | Details |
|---------|-------------|
| **CS Concept** | Loops with variation — repeating a pattern that changes each iteration |
| **Puzzle Type** | Program a robot to deliver packages where each house needs a different number of items (1, 2, 3, 4, 5) |
| **Learning Objective** | Players understand that loops can include variables that change with each repetition |
| **Story Integration** | A clockwork merchant needs urgent deliveries. Each house ordered a different amount — the robot must adapt its load based on which house it's visiting. |
| **Explorer Mode** | Shows: "The number of packages changes each time. Can you make the loop 'remember' how many to carry?" |
| **Engineer Mode** | Requires player to use a counter variable inside the loop (advanced concept introduced naturally) |
| **Blackout Mode** | Same as previous Blackout missions — submit-only evaluation |

**Puzzle Layout:**
- 5 houses, each with a numbered order slip (1–5 packages)
- Robot starts at warehouse with all packages loaded
- Player must program: For i = 1 to 5, [Load(i), MoveToHouse(i), Drop(i)]
- Visual: Each house receives the correct number of packages; order slips turn gold

**Key Insight:** This introduces **loop variables** — a natural extension of basic loops that prepares players for more complex concepts later.

---

### Mission D1M05: "The Neon Festival" (District 1 Finale)

| Element | Details |
|---------|-------------|
| **CS Concept** | Combining loops with signal patterns — creating complex sequences from simple repetitions |
| **Puzzle Type** | Program the festival light display: a sequence of neon colors that follows a repeating pattern with variations |
| **Learning Objective** | Players can create complex, multi-layered signal sequences using nested loops and variables |
| **Story Integration** | Token Town is hosting its annual Neon Festival. LUMA must program the central light tower to display the festival's traditional signal pattern — but this year, a new color has been added that doesn't fit the old pattern. |
| **Explorer Mode** | Shows the base pattern; hint: "The new color appears every 3rd flash. Can you add it to the loop?" |
| **Engineer Mode** | Requires player to integrate the new color without breaking the existing pattern; scores on elegance of solution |
| **Blackout Mode** | Pattern plays once at full speed; player must program from memory |

**Puzzle Layout:**
- Light tower with 8 colored bulbs (cyan, magenta, gold, and a new purple)
- Base pattern: CYAN-MAGENTA-GOLD repeats
- New requirement: Insert PURPLE every 3rd cycle
- Solution: Repeat(3, [Cyan, Magenta, Gold]), then Purple, then repeat...
- Visual: Tower lights up in the correct sequence; festival crowd cheers (animated NPCs)

**Significance:** District 1 finale. Players have mastered loops at multiple levels and are ready for conditionals in District 2. The new purple color foreshadows AETHEL's "dream signals" introduced in later districts.

---

## District 2: Cipher Ridge — Conditionals (If/Then)

### Mission D2M01: "The Fork in the Tunnel"

| Element | Details |
|---------|-------------|
| **CS Concept** | Introduction to conditionals — making decisions based on conditions |
| **Puzzle Type** | Program a robot to navigate a tunnel with two paths: take LEFT if signal is cyan, RIGHT if magenta |
| **Learning Objective** | Players understand that programs can make different choices based on input |
| **Story Integration** | LUMA follows the "REMEMBER" signal into Cipher Ridge's old mining tunnels. The path splits — a broken signal relay determines which way to go. |
| **Explorer Mode** | Shows: "If the light is cyan, go left. If it's magenta, go right." |
| **Engineer Mode** | No explicit hint; player must infer the conditional structure from the puzzle layout |
| **Blackout Mode** | Signal color changes each run; player programs once and tests against multiple scenarios |

**Puzzle Layout:**
- Tunnel splits into two paths (left = cyan signal, right = magenta signal)
- Robot starts at junction with a signal sensor
- Player must program: IF signal == CYAN THEN MoveLeft ELSE MoveRight
- Visual: Robot follows the correct path; tunnel lights up behind it

**Key Insight:** This is the first mission where **branching logic** matters. The robot's behavior changes based on input — a fundamental shift from linear loops.

---

### Mission D2M02: "The Signal Filter"

| Element | Details |
|---------|-------------|
| **CS Concept** | Multiple conditionals — handling more than two cases |
| **Puzzle Type** | Program a signal filter that routes signals to different destinations based on color (cyan → archive, magenta → alert, gold → display) |
| **Learning Objective** | Players understand IF/ELSE IF/ELSE chains for multi-way decisions |
| **Story Integration** | A relay station in Cipher Ridge needs help sorting incoming signals. Some go to the archive, some trigger alerts, some are displayed publicly. |
| **Explorer Mode** | Shows a flowchart: "Cyan goes here, magenta goes there, gold goes somewhere else." |
| **Engineer Mode** | Requires player to handle an unexpected "grey" signal (unknown type) with an ELSE clause |
| **Blackout Mode** | Signals arrive in random order; player must program all three paths correctly |

**Puzzle Layout:**
- Three output channels (archive, alert, display) each with a destination icon
- Signal input arrives as colored packets
- Player programs: IF cyan THEN Archive ELSE IF magenta THEN Alert ELSE IF gold THEN Display ELSE Unknown
- Visual: Packets flow to correct destinations; wrong destinations flash red

**Key Insight:** Introduces the **ELSE clause** for handling unexpected inputs — a practical skill that mirrors real-world programming.

---

### Mission D2M03: "The Conditional Courier" (District 2 Tutorial Boss)

| Element | Details |
|---------|-------------|
| **CS Concept** | Conditionals combined with loops — making decisions inside repeated sequences |
| **Puzzle Type** | Program a robot to deliver packages, but skip houses that are closed (signal is grey) and double-deliver houses with urgent orders (signal is gold) |
| **Learning Objective** | Players understand conditionals can exist inside loops, creating dynamic behavior |
| **Story Integration** | LUMA must deliver urgent messages across Cipher Ridge. Some houses are closed for repairs; others have emergency orders that need double the usual amount. |
| **Explorer Mode** | Shows: "Check each house's signal before delivering. Closed houses get nothing; gold signals get extra." |
| **Engineer Mode** | Requires player to optimize by checking signal once per house and branching accordingly |
| **Blackout Mode** | House conditions change between runs; player programs once and tests against all scenarios |

**Puzzle Layout:**
- 6 houses in a row, each with a random signal state (cyan = normal, magenta = urgent, grey = closed)
- Robot starts at post office with packages for all houses
- Player must program: For each house, IF grey THEN Skip ELSE IF gold THEN Deliver(2×) ELSE Deliver(1×)
- Visual: Houses light up as robot delivers; closed houses stay dark

**Significance:** This is the **first mission combining loops and conditionals** — a major conceptual leap. It mirrors real programming where decisions happen inside repeated processes.

---

### Mission D2M04: "The Cipher Gate"

| Element | Details |
|---------|-------------|
| **CS Concept** | Nested conditionals — decisions within decisions |
| **Puzzle Type** | Program a robot to open a series of locked gates, each requiring different signal combinations |
| **Learning Objective** | Players understand that conditions can contain other conditions (nested IF statements) |
| **Story Integration** | A sealed gate blocks access to deeper Cipher Ridge. It requires a specific sequence of signals to open — but the requirements change based on the time of day (morning = cyan+magenta, afternoon = gold only). |
| **Explorer Mode** | Shows: "First check the time. Then check which signals are available." |
| **Engineer Mode** | Requires player to handle all four possible combinations (morning/afternoon × signal availability) |
| **Blackout Mode** | Time and signals change randomly; player programs once and tests against all scenarios |

**Puzzle Layout:**
- Gate with two locks: Time Lock (morning/afternoon) and Signal Lock (which signals are present)
- Robot must check time first, then available signals, then open correct combination
- Player programs nested IFs: IF morning THEN IF cyan AND magenta THEN Open ELSE Wait ELSE IF gold THEN Open Else Wait
- Visual: Gate opens with a satisfying mechanical animation; deeper tunnel revealed

**Key Insight:** Nested conditionals are introduced naturally — the player needs them to solve the puzzle, not because they were told to use them.

---

### Mission D2M05: "The Ridge Relay" (District 2 Finale)

| Element | Details |
|---------|-------------|
| **CS Concept** | Combining loops + conditionals + nested logic — full signal processing pipeline |
| **Puzzle Type** | Program a relay station to process a stream of mixed signals: route them, filter duplicates, and flag urgent messages |
| **Learning Objective** | Players can build a complete signal-processing program using all concepts learned so far (loops, conditionals, nested logic) |
| **Story Integration** | The Cipher Ridge relay station is overwhelmed with incoming signals. LUMA must reprogram it to handle the load efficiently — and in doing so, discovers a hidden pattern: every 7th signal contains a fragment of the "REMEMBER" message. |
| **Explorer Mode** | Shows the three tasks separately; hints for each |
| **Engineer Mode** | Scores on efficiency: fewer instructions = better; also checks that duplicate filtering works correctly |
| **Blackout Mode** | Signal stream plays at full speed; player programs once and tests against a longer, more complex stream |

**Puzzle Layout:**
- Input: Stream of 20 mixed signals (cyan, magenta, gold, grey in random order)
- Output: Three channels (routed signals, filtered duplicates, urgent alerts)
- Player must program: Loop through all signals → IF duplicate THEN skip ELSE route based on color → IF every 7th signal THEN extract fragment
- Visual: Signal stream flows through the relay; correct routing lights up green; hidden "REMEMBER" fragments glow gold

**Significance:** District 2 finale. Players have mastered loops and conditionals at multiple levels. The hidden "REMEMBER" fragment reinforces the central mystery and rewards careful observation — a skill that will be important in later districts.

---

## Mission Design Summary (Missions 1–10)

| Mission | CS Concept | Complexity | Story Beat |
|---------|-----------|------------|------------|
| D1M01 | Basic loops | ★☆☆☆☆ | Tutorial — first day on the job |
| D1M02 | Nested loops | ★★☆☆☆ | Market setup — practical application |
| D1M03 | Loops + signal decoding | ★★★☆☆ | **First story reveal: "REMEMBER"** |
| D1M04 | Loops with variables | ★★★★☆ | Clockwork courier — adaptation |
| D1M05 | Complex loop patterns | ★★★★★ | Festival finale — new color foreshadowing |
| D2M01 | Basic conditionals | ★★☆☆☆ | Tunnel fork — first decision-making |
| D2M02 | Multiple conditionals | ★★★☆☆ | Signal filter — multi-way routing |
| D2M03 | Loops + conditionals | ★★★★☆ | Conditional courier — combined concepts |
| D2M04 | Nested conditionals | ★★★★★ | Cipher gate — decisions within decisions |
| D2M05 | Full pipeline (loops + conditionals) | ★★★★★★ | **Hidden "REMEMBER" fragment** |

---

## Open Questions for Phase 3 (GDD)

| Question | Impact | Decision Needed By |
|----------|--------|-------------------|
| Should each mission have a unique robot character or use the same generic one? | Affects art workload and player attachment | Phase 3 — recommend same robot with cosmetic variations per district |
| How many hints should Explorer mode provide per mission? | Balances accessibility vs. challenge | Phase 3 — target 2–3 progressive hints (show → explain → demonstrate) |
| Should Blackout mode show the optimal solution after completion? | Affects replayability and learning | Phase 3 — recommend yes, but hide it behind a "View Solution" button |
| Are there any missions where the player's choice affects later puzzles? | Adds branching narrative complexity | Phase 3 — keep linear for MVP; add choices in Phase 6+ |

---

*Phase 2 mission concepts provide actionable design direction for Phase 4 prototype. Each mission is scoped to be buildable in 1–3 days of development, with the first 5 missions (District 1) forming a complete playable vertical slice.*
