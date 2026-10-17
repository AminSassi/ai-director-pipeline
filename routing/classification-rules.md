# Scene Classification Rules — Visual Intent & Documentary Archetypes

Every chunk receives ONE primary **Visual Archetype** during Phase 0.75. The classification asks:

**"What kind of visual is required to tell this part of the story with maximum documentary prestige, camera variety, and zero AI slop?"**

NOT "what literal words appear in the narration" (Rule #42 Subtext Extraction).

---

## The 7 Documentary Visual Archetypes

### 1. `HUMAN_CONFLICT`
High-stakes character drama, psychological realization, boardroom standoffs, interrogation tension, courtroom confrontations.

**Examples:**
- Executive slowly closing a leather dossier and turning toward a rain-streaked window
- Prosecutor standing in a dark walnut courtroom while the defendant sits rigid in the dock
- Two silhouettes separated by a long mahogany table under cold overhead light
- Moderation-safe human framing for sensitive beats (backlit silhouettes, OTS past a dark suit jacket, low-angle marching boots — Rule #44)

**Mandatory Constraints:**
- **Zero Multi-Person Physical Contact (Rule #39):** Never prompt fighting, wrestling, tackling, or hands grabbing wrists. Use pre-impact standoff tension and post-impact aftermath.
- **Zero Fine Hand Mechanics (Rule #40):** Never prompt pens writing, fingers typing, or stamps pressing. Keep props already printed/signed.
- **2-Chunk Location Ceiling (Rule #26):** Never stay in the same interior room or `@LOCATION` for more than 2 consecutive chunks.

---

### 2. `INFRASTRUCTURE_SCALE`
Monumental real-world exterior architecture, industrial supply chains, ports, megastructures, environmental aftermath, and physical world-building. Used both for geographic/industrial beats AND as the mandatory **Chunk 3 Location Ceiling Breaker** after 2 consecutive interior chunks.

**Examples:**
- Container gantry cranes towering over a rain-slicked harbor under yellow sodium mist
- Abandoned unfinished concrete high-rises in a ghost city (`24mm` worm's-eye crane rise)
- High-altitude aerial pull-back over a massive desert solar array or factory complex

**When to use:**
- Whenever the narration describes scale, systemic reach, geography, or industry
- Whenever the previous 2 chunks were set inside an interior room (Rule #26 Location Ceiling)

---

### 3. `EXPLAINER_LIGHT_TABLE`
Tactile physical evidence boards, illuminated glass forensic light-tables, physical brass/wooden scale models, and analog blueprints viewed in physical space (**Rule #38 Mode A**).

**Examples:**
- Overhead `90°` God's-eye drift across a dark frosted glass light-table where already-printed photographs and red string connections sit under warm tungsten edge-lighting
- Low-angle macro skim across a physical architectural scale model of a dam or facility
- Over-the-shoulder view of an investigator leaning over an already-marked physical map

**Mandatory Constraints (Rule #38 & #40):**
- **NO 3D CAD wireframes, glowing sci-fi holograms, or isometric 3D cutaways** in video prompts (they melt into slop).
- **NO readable text/numbers:** Always append `--no text, words, numbers, labels`.
- **NO active drawing/stamping:** Strings, pins, and markers are already placed on the board before the shot begins.

---

### 4. `EXPLAINER_VOX_COLLAGE`
Flat 2D mixed-media paper cutout collages, halftone newspaper texture layers, and physical timeline strips moving across a textured matte surface (**Rule #38 Mode B**).

**Examples:**
- Top-down `90°` perpendicular camera gliding across layered matte paper cutouts on a dark slate surface with stark chiaroscuro drop-shadows
- High-contrast black-and-white halftone photographic cutouts separated by bold crimson geometric divider lines (zero readable text)

**When to use:**
- Abstract financial flows, corporate shell structures, historical timelines, or statistical comparisons where live-action rooms would feel repetitive.

---

### 5. `ARCHIVAL_TABLEAU`
Period-authentic historical reconstructions, static photographic plates with slow Ken Burns optical drift, and physical evidence rooms.

**Examples:**
- 1990s mahogany vault room with stacked archival bankers boxes under dusty tungsten shafts
- Static historical portrait plate inside a physical dossier frame with a slow optical push-in (papers never float or fly)

**Mandatory Constraints:**
- Never make newspapers or documents fly, spin, or morph.
- Never prompt readable paragraphs of English text (`--no text, words, numbers, labels`).

---

### 6. `MONTAGE_TIME_COMPRESSION`
Multi-beat sequences that map 2–3 distinct clauses, locations, or years across `SHOT 1–2`, `SHOT 3`, and `SHOT 4` (**Rule #33 Multi-Beat Narrative Mapping**).

**Examples:**
- *Narration:* "Ghost cities, a quiet transfer of assets, and a midnight departure to Vancouver."
  - `SHOT 1–2`: Abandoned concrete megastructure under a crane pull-back
  - `SHOT 3`: Executive closing a leather briefcase in a dark office (`35mm`, chiaroscuro)
  - `SHOT 4`: Silhouetted figure walking toward a night airport terminal gate (`50mm`, film grain)

**When to use:**
- Any chunk whose narration spans multiple distinct places, clauses, or time jumps. Never trap multi-beat narration inside a single room.

---

### 7. `ATMOSPHERIC_TRANSITION`
High-contrast mood bridges, threshold pull-backs, and **Rule #20 CTA chunks** (Hook CTA, Midpoint CTA, Outro CTA).

**Examples:**
- Camera retreating backward through a heavy oak doorway into darkness as a lone silhouette stands by a window
- Low-slung surface skim inches above wet midnight asphalt reflecting amber streetlights

**Mandatory CTA Constraint (Rule #20):**
- CTA chunks MUST use `ATMOSPHERIC_TRANSITION` or `INFRASTRUCTURE_SCALE`. Never show YouTube subscribe buttons, notification bells, phone screens, or `@channellogo` graphics.

---

## Classification Priority & Anti-Monotony Routing Rules

When routing a batch of 6 chunks:
1. **Enforce the 2-Chunk Location Ceiling (Rule #26):** If Chunks $N$ and $N+1$ are routed to `HUMAN_CONFLICT` in the same room, Chunk $N+2$ MUST route to `INFRASTRUCTURE_SCALE`, `EXPLAINER_LIGHT_TABLE`, `EXPLAINER_VOX_COLLAGE`, or a different location.
2. **Pre-Assign `SHOT 1` Framing Archetypes (`camera/angles.md`):**
   - Maximum **1 chunk per 6-chunk batch** may use `"slow push in"` in `SHOT 1`.
   - Zero consecutive chunks may open with `Cinematic medium shot`.
3. **Subtext Over Literal Keywords (Rule #42):**
   - Never route a biography line ("Born in 1942") to an explainer diagram just because it contains a year.
   - Never route a financial loss ("The stock plunged") to chaotic physical running or screaming; route to `HUMAN_CONFLICT` (Fincher stillness) or `EXPLAINER_LIGHT_TABLE` / `EXPLAINER_VOX_COLLAGE`.

---

## Common Routing Mistakes Fixed by v2.0

| Legacy Mistake | Why It Failed | v2.0 Correct Routing |
| :--- | :--- | :--- |
| Routing "fighting / crowd panic / running" to `ACTION` | Violates Rule #1 (Anti-Chaos) & Rule #39 (Contact Ban); produces multi-limb AI body horror | Route to `HUMAN_CONFLICT` using pre-impact standoff tension or post-impact aftermath |
| Routing headlines/quotes to `TEXT FOCUS` with on-screen text | Grok renders English text as alien gibberish (Blacklist #13) | Route to `EXPLAINER_LIGHT_TABLE`, `ARCHIVAL_TABLEAU`, or `HUMAN_CONFLICT` with `--no text, words, numbers, labels` |
| Routing 10 consecutive chunks to `CINEMATIC` in one room | Creates single-location fatigue and repetitive `SHOT 1 slow push in` loops | Enforce the **2-Chunk Location Ceiling** by alternating `HUMAN_CONFLICT` with `INFRASTRUCTURE_SCALE` and `EXPLAINER_*` |
