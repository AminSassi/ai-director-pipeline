# Structured Routing Output Format (Phase 0.75)

Phase 0.75 produces the **Creative Director's Pre-Visualization & Routing Map**. It prevents Phase 2 from improvising repetitive camera angles or trapping the episode in a single room.

---

## Per-Chunk Routing Schema

Each chunk in `output/phase-0.75-routing.md` must specify:
- `chunk`: Chunk number and timestamp
- `visual_type`: `CINEMATIC_DRAMA` | `INVESTIGATIVE_PROCEDURAL` | `SCALE_INFRASTRUCTURE` | `EXPLAINER_LIGHT_TABLE` | `EXPLAINER_VOX_COLLAGE` | `CONTRAST_MONTAGE` | `CTA_ATMOSPHERIC`
- `shot_1_archetype`: One of the 12 Framing Archetypes from `camera/angles.md` (guaranteeing no consecutive repeats and max 1 `slow push in` per 6-chunk batch)
- `location_and_tags`: Primary setting and locked `@TAGS` (enforcing the **2-Chunk Location Ceiling**—never >2 consecutive chunks in the same room)
- `subtext_direction`: Non-literal physical action, human transaction, or visual metaphor to execute in Phase 2

---

## Routing Table Template

```markdown
# PHASE 0.75: INTELLIGENT SCENE ROUTING & CAMERA BLUEPRINT
**Channel:** [Verion | Insolvent]
**Total Chunks:** [N] | **Pacing:** [10s (4 shots) | 15s (6 shots)]

| Chunk | Timestamp | Visual Type | `SHOT 1` Framing Archetype (`camera/angles.md`) | Location & Locked `@TAGS` | Subtext & Non-Literal Visual Direction |
| :---: | :---: | :--- | :--- | :--- | :--- |
| **01** | 00:00–00:10 | `SCALE_INFRASTRUCTURE` | #4 Low-Slung Surface Skimming | Exterior `@PYONGYANG_HOSPITAL` | Security floodlight sweeping wet asphalt outside locked compound gates at dawn |
| **02** | 00:10–00:20 | `INVESTIGATIVE_PROCEDURAL` | #5 OTS Evidence Reveal (Pan) | `@UC_MEDICAL_CENTER` `@DR_KANTER` | OTS past Dr. Kanter studying dark cortical voids on backlit brain MRI films |
| **03** | 00:20–00:30 | `CONTRAST_MONTAGE` | #8 Depth-Plane Rack Focus | `@UC_MEDICAL_CENTER` $\rightarrow$ `@PYONGYANG_HOSPITAL` | Rack focus from April 2016 scan date to silhouette of guard in North Korean ward |
| **04** | 00:30–00:40 | `EXPLAINER_LIGHT_TABLE` | #12 Tactile Light-Table Glide | Forensic Lightbox | Top-down macro dolly across cyanotype toxicological & neural pathway plate |
| **05** | 00:40–00:50 | `CINEMATIC_DRAMA` | #6 Backlit Chiaroscuro Silhouette | Detention Wing Corridor | Slow dolly out from solitary backlit figure behind heavy barred partition |
| **06** | 00:50–01:00 | `CTA_ATMOSPHERIC` | #2 Architectural Worm's-Eye | Taedong River / Pyongyang | Worm's-eye crane rise past brutalist concrete monument in twilight rain (Zero UI) |
```

---

## Pre-Phase 2 Routing Audit Check

Before advancing from Phase 0.75 to Phase 1/2, verify:
1. **Zero 3-Chunk Room Traps:** Does any `@LOCATION` appear as the primary setting in 3+ consecutive rows? If yes, re-route the middle chunk to `EXPLAINER_LIGHT_TABLE`, `EXPLAINER_VOX_COLLAGE`, `SCALE_INFRASTRUCTURE`, or `CONTRAST_MONTAGE`.
2. **Opening Camera Diversity:** Across every group of 6 rows, does each row use a different `SHOT 1` Framing Archetype, with `"slow push in"` appearing at most once?
3. **Explainer Integration:** Are complex technical/financial mechanisms routed to `EXPLAINER_LIGHT_TABLE` or `EXPLAINER_VOX_COLLAGE` (Rule #38)?
