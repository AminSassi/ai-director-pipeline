# Master Cinematography, Framing & Camera Movement Playbook

This module is the authoritative cinematography reference for the AI Director Pipeline. Every Start Frame and Video Prompt must be designed using these principles to guarantee **David Fincher / BBC Frontline documentary prestige**, **dynamic visual variety**, and **zero AI slop**.

---

## 1. THE ANTI-MONOTONY MANDATE (HARD BATCH CONSTRAINTS)

AI models naturally decay into repetitive, low-effort camera formulas (such as starting every single chunk with `"Cinematic medium shot... SHOT 1/4 slow push in"`). This is **strictly forbidden**.

### Hard Rules Across Every 6-Chunk Batch:
1. **The `SHOT 1` "Slow Push-In" Cap (Max 1 Per Batch):**
   - Across any batch of 6 chunks, `"slow push in"` (or `"slow dolly in"`) may be used in `SHOT 1` **at most ONCE (max 1 out of 6 chunks)**.
   - The other 5 chunks in the batch MUST open `SHOT 1` with different camera movements (e.g., lateral tracking, crane rise/descent, slow dolly out/pull-back, low-angle tilt up, overhead perpendicular drift, OTS rack focus).
2. **Zero Consecutive Opening Shot Sizes:**
   - Never start two consecutive chunks with the same shot size (e.g., if Chunk 1 starts with a `Medium shot`, Chunk 2 must start with an `Extreme wide`, `Low-angle worm's-eye`, `Top-down bird's-eye`, `Close-up macro`, or `Over-the-shoulder`).
3. **Zero Repeated Shot-Sequence Templates:**
   - Never repeat the same sequence of 4 or 6 camera movements from one chunk to the next.
   - Within every single chunk, use a **minimum of 3 distinct camera movements**, and **never repeat the same movement in consecutive shots** (including across the boundary from Shot 4/6 of Chunk $N$ to Shot 1 of Chunk $N+1$).
4. **The 2-Chunk Location Ceiling (Zero Single-Room Trapping):**
   - Never set more than **2 consecutive chunks** inside the same interior room or locked location tag (e.g., never trap 6–12 chunks inside a hospital room, lab, or office).
   - If the narration stays on an analytical topic (e.g., reviewing three medical or financial theories), visually manifest the **external physical world of each theory** (the factory floor, the shipping port, the prison corridor, the light-table schematic) rather than filming an analyst/doctor in the same room for 2 minutes.

---

5. **The Anti-Wandering Mandate (Zero Purposeless B-Roll — Rule #46):**
   - The camera must NEVER wander through an empty street, cruise through a library, or slowly zoom on a book, binder, or desk object. Every camera move must be anchored to an active, motivated human action event.
6. **100% Instant Script-to-Screen Action Sync (Rule #47):**
   - What is spoken on VO must be INSTANTLY visible and understood on screen. Put people in dynamic action events (walkouts, negotiations, trade halts, confrontations, revelations) rather than passive staring.

---

## 2. THE 12 SIGNATURE DOCUMENTARY FRAMING ARCHETYPES

Every chunk in a 6-chunk batch must draw from these **12 AI-stable, high-craft cinematic archetypes** so no two chunks in a batch feel alike:

| # | Archetype Name | Framing & Lens Setup | Safe AI Camera Movement | Best Narrative Use Case |
| :- | :--- | :--- | :--- | :--- |
| **1** | **Foreground Occlusion (Frame-Within-Frame)** | Shoot past a dark doorway frame, half-open Venetian blinds, glass wall partition, or archive shelving aisle toward subject in midground (`50mm lens, shallow DOF`). | Slow lateral tracking past the foreground obstruction. | Secrecy, surveillance, behind-closed-doors meetings, whistleblowers. |
| **2** | **Architectural Worm's-Eye** | Camera placed near floor/ground level looking sharply upward at towering concrete facades, skyscraper glass, gantry cranes, or courtroom pillars (`24mm wide lens, deep focus`). | Slow crane rise or low-angle tilt up. | Institutional power, overwhelming corporate/state scale, isolation. |
| **3** | **God's-Eye Perpendicular (90° Bird's-Eye)** | Camera mounted directly overhead looking 90° straight down at an evidence table, spiral stairwell, solitary figure crossing a plaza, or highway (`35mm lens`). | Slow overhead pedestal drift or slow rotation. | Systemic patterns, entrapment, forensic overview, geography. |
| **4** | **Low-Slung Surface Skimming** | Camera positioned inches above wet asphalt, polished marble, factory safety lines, or railway ballast (`28mm wide lens`). | Smooth forward or lateral ground-level tracking. | Momentum, supply chains, covert arrival, gritty atmospheric transitions. |
| **5** | **Over-The-Shoulder (OTS) Reveal** | Camera positioned behind the subject's shoulder looking toward a monitor, lightbox scan, or dossier (`50mm lens`). *Mandatory whenever screen/document content is described.* | Slow pan across the display or rack focus from shoulder to screen. | Discovery of fraud, diagnostic analysis, terminal logs, evidence review. |
| **6** | **Backlit Chiaroscuro Silhouette** | Subject framed in stark high-contrast silhouette against a bright window, illuminated corridor threshold, or sodium floodlight (`35mm anamorphic`). | Slow dolly out (pull-back) into deep shadow. | Anonymity, moral compromise, unanswered questions, quiet dread. |
| **7** | **Parallel Steadicam Glide** | Camera tracks sideways at the exact walking speed of a purposeful subject in a corridor, airport concourse, or industrial yard (`35mm lens`). | Smooth lateral tracking left or right. | Urgent mission, arrival at court/embassy, procedural momentum. |
| **8** | **Depth-Plane Rack Focus** | Two distinct subjects placed at extreme foreground and background (e.g., sealed evidence box in foreground, tense investigator in background, `50mm lens`). | Macro rack focus shifting cleanly from foreground to background. | Connecting cause and effect, linking physical evidence to human stakes. |
| **9** | **Low-Angle Dutch Tilt (15°)** | Canted horizon line tilting upward past a conference table, server aisle, or brutalist corridor (`28mm/35mm lens`). | Slow diagonal dolly back or tension hold. | Crisis reveal, psychological unraveling, market crash, deception exposed. |
| **10** | **Monumental Crane Pull-Back** | Wide exterior or cavernous interior framing a small human figure or vehicle against vast real-world infrastructure (`24mm wide lens`). | High-altitude crane rise + dolly back. | Aftermath, systemic scale, global reach, act transitions, CTA scenes. |
| **11** | **Threshold Pull-Back (Doorway Isolation)** | Camera retreats backward through an open doorway or glass partition, leaving the subject isolated in the illuminated room beyond (`35mm lens`). | Slow dolly back through frame (door stays stationary—never moves). | Cover-ups, abandonment, doors closing figuratively on an investigation. |
| **12** | **Tactile Forensic Light-Table / Vox Plate** | Top-down macro view of a physical cyanotype blueprint on a backlit drafting box, or flat 2D paper-cutout map collage (`35mm macro lens`). | Smooth single-axis macro glide across the static physical plate. | Technical mechanisms, flight paths, corporate shell networks, timelines. |

---

## 3. SUBTEXT EXTRACTION (THE GOLDEN DIRECTORIAL RULE)

Before writing any Start Frame or Video Prompt, **NEVER write literal captions of the voiceover**.
If the narration says *"The company was under immense stress,"* a lazy agent prompts *"A stressed executive at a desk."* A real film director finds the **specific physical detail or camera geometry** that makes the audience *feel* the truth without restating the words.

### Mandatory 4-Question Pre-Flight:
1. **Literal Text:** What do the words literally say?
2. **Subtext / Emotional Truth:** What is the power dynamic, irony, or hidden reality underneath?
3. **Physical Manifestation:** What concrete human transaction, physical environment, or tactile contrast embodies that truth?
4. **Camera Amplification:** Which of the 12 Archetypes above amplifies that power dynamic? (e.g., high-angle bird's-eye makes a character look trapped; worm's-eye makes an institution look crushing; OTS makes the viewer complicit in the discovery).

---

## 4. EDIT-LEVEL CONTINUITY & MATCH CUTS

True cinematic flow happens across shot boundaries. Design Shot $N$ and Shot $N+1$ (or Chunk $N$ and Chunk $N+1$) to cut together like a theatrical documentary:
- **Contrast Cut:** Juxtapose two starkly different worlds within the same chunk (e.g., Shot 1–2: lavish sunlit venture capital stage $\rightarrow$ Shot 3–4: cramped fluorescent back-office in Bangalore at 3 AM).
- **Graphic / Positional Match:** Align the geometry between cuts (e.g., a circular jet engine turbine in Shot 2 cuts to a circular radar scope or courtroom seal in the exact same screen position in Shot 3).
- **Scale Alternation Rhythm:** Never stay at eye-level medium distance for an entire chunk. Weave dynamically between **Monumental Wide** (24mm) $\rightarrow$ **Intimate Medium/OTS** (35mm/50mm) $\rightarrow$ **Tactile Macro Detail** (50mm macro).

---

## 5. HARD CAMERA GEOMETRY & PHYSICS BANS (ZERO SLOP)

1. **NO Talking Heads:** Never frame a narrator or character looking directly into the camera lens speaking.
2. **NO Laptop Screen Paradox:** Never shoot a person's face from the front while describing readable UI on their laptop/monitor screen (in physical reality, the camera sees the back of the monitor). Always use **Over-The-Shoulder (OTS)** for screens.
3. **NO Character Reflections in Glass/Monitors:** Never prompt a person's face reflected in a window, mirror, or monitor glass—AI video models duplicate and clone the character grotesquely.
4. **NO Unanchored Multi-Scale Morphs:** In a single 10s/15s video prompt anchored to `@image1`, never ask the camera to fly from outer space/satellite orbit all the way down into a street-level building entrance. Keep continuous camera trajectories within a single contiguous physical scale; use hard cuts (`SHOT 2/4`, `SHOT 3/4`) to jump between scales.
5. **NO Moving Doors or Fine Finger/Tool Mechanics:** Doors must already be open or closed (never opening/closing mid-shot). Hands must never write cursive with pens, press rubber stamps, type rapidly on keyboards, or manipulate fine calipers/loupes.
