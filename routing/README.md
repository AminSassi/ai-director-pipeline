# Intelligent Scene Routing — Visual Intent & Anti-Monotony System (Phase 0.75)

Routes each narration chunk to one of the **7 Documentary Visual Archetypes**, pre-assigns a distinct **`SHOT 1` Framing Archetype** from `camera/angles.md`, and enforces the **2-Chunk Location Ceiling** before Phase 2 prompt generation begins.

---

## Core Principle

The router asks three questions for every chunk:
1. **Subtext Extraction (Rule #42):** *"What is the emotional or institutional truth underneath this line, and what concrete human transaction or physical scale shows it?"*
2. **Location Ceiling (Rule #26):** *"Have we already spent 2 consecutive chunks in the current interior room? If so, how do we pivot to exterior infrastructure scale or a tactile explainer?"*
3. **Camera Variety (Rule #6):** *"Which of the 12 Documentary Framing Archetypes (`camera/angles.md`) opens `SHOT 1` so we never repeat consecutive medium shots or exceed 1 `slow push in` per 6 chunks?"*

---

## The 7 Documentary Visual Archetypes

| Visual Archetype | Description | Primary Generator |
| :--- | :--- | :--- |
| `HUMAN_CONFLICT` | High-stakes character drama, boardroom standoffs, interrogation tension, OTS/silhouette human presence (Rule #44) | **Nano Banana 2** (Start Frame) + **Grok Imagine** (Video) |
| `INFRASTRUCTURE_SCALE` | Monumental real-world exterior architecture, ports, factories, ghost cities, aerial scale (breaks interior fatigue) | **Nano Banana 2** + **Grok Imagine** |
| `EXPLAINER_LIGHT_TABLE` | Tactile physical evidence boards, frosted glass light-tables, physical architectural scale models (Rule #38 Mode A) | **Nano Banana 2** + **Grok Imagine** (`--no text, words, numbers, labels`) |
| `EXPLAINER_VOX_COLLAGE` | Flat 2D mixed-media paper cutout collages, halftone newspaper layers, crimson geometric lines (Rule #38 Mode B) | **Nano Banana 2** + **Grok Imagine** (`--no text, words, numbers, labels`) |
| `ARCHIVAL_TABLEAU` | Period-authentic historical reconstructions, vault rooms, static photographic plates with slow optical drift | **Nano Banana 2** + **Grok Imagine** |
| `MONTAGE_TIME_COMPRESSION` | Multi-beat sequences mapping 2–3 distinct clauses/locations across `SHOT 1–2`, `SHOT 3`, and `SHOT 4` (Rule #33) | **Nano Banana 2** + **Grok Imagine** |
| `ATMOSPHERIC_TRANSITION` | High-contrast mood bridges, threshold pull-backs, and **Rule #20 CTA chunks** (zero UI, zero logos) | **Nano Banana 2** + **Grok Imagine** |

---

## Structured Routing Output (`output-format.md`)

Every chunk produces structured metadata that locks in variety before prompts are written:

```yaml
chunk: 07
duration: 10s
shot_count: 4
narration: "Behind closed doors, the company was keeping two separate sets of accounting records."
subtext_extraction: "Institutional deception hidden beneath polished corporate calm — shown via physical evidence transfer, not a literal spreadsheet."
visual_archetype: EXPLAINER_LIGHT_TABLE
location_tag: "@FORENSIC_LIGHT_TABLE"
consecutive_location_count: 1 # Max allowed is 2 (Rule #26)
shot_1_framing_archetype: "#3 God's-Eye Perpendicular Overhead (90-degree bird's-eye)"
shot_1_camera_move: "slow perpendicular overhead drift across illuminated glass table" # NOT a slow push-in
human_presence_mode: "Silhouette hands resting on table edge (Rule #40 safe — zero writing/stamping)"
color_palette: "Warm 2700K tungsten edge-light against deep obsidian shadow"
priority: HIGH
```

---

## Batch-Level Routing Verification

At the end of every 6-chunk routing block, verify:
- **`SHOT 1` Slow Push-In Count:** $\le 1$ per 6 chunks (`PASS`)
- **Consecutive Opening Medium Shots:** $0$ (`PASS`)
- **Max Consecutive Chunks in Same Location:** $\le 2$ (`PASS`)

---

## Files in `routing/`

| File | Purpose |
| :--- | :--- |
| `classification-rules.md` | Definitions and constraints for the 7 Documentary Visual Archetypes |
| `model-recommendations.md` | Generator mapping and `SHOT 1` Framing Archetype pre-assignment |
| `output-format.md` | Structured YAML schema and 6-chunk batch verification |
| `README.md` | Overview of the Phase 0.75 Intelligent Scene Routing system |
