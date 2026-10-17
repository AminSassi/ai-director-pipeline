# Prompt Quality Checklist & Pre-Generation Audit Matrix

Use this mandatory checklist and verification matrix to audit every 6-chunk batch **before** presenting prompts to the director.

---

## 1. Mandatory 6-Chunk Pre-Generation Audit Matrix

Before printing any batch of 6 chunks, you MUST print this exact verification matrix in chat to prove **zero camera monotony**, **zero single-room trapping**, and **genuine subtext extraction**:

```markdown
### 🛡️ PRE-GENERATION AUDIT MATRIX (BATCH X: CHUNKS A–B)

| Chunk | Primary Location / Tag | Subtext / Visual Metaphor (Non-Literal) | Start Frame Archetype (`camera/angles.md`) | `SHOT 1` Camera Move (Max 1 Push-In/Batch!) | Shots 2–4/6 Movements | Locked Tags (SF vs Video Header) |
| :---: | :--- | :--- | :--- | :--- | :--- | :--- |
| **01** | ... | ... | ... | ... | ... | SF: `[...]` / VH: `[...]` |
| **02** | ... | ... | ... | ... | ... | SF: `[...]` / VH: `[...]` |
| **03** | ... | ... | ... | ... | ... | SF: `[...]` / VH: `[...]` |
| **04** | ... | ... | ... | ... | ... | SF: `[...]` / VH: `[...]` |
| **05** | ... | ... | ... | ... | ... | SF: `[...]` / VH: `[...]` |
| **06** | ... | ... | ... | ... | ... | SF: `[...]` / VH: `[...]` |
```

---

## 2. Hard Gate Verification Checks (Zero Exceptions)

### A. Anti-Monotony & Creative Staging Checks
- [ ] **`SHOT 1` Slow Push-In Cap:** Is `"slow push in"` used in `SHOT 1` **at most ONCE** across all 6 chunks in this batch? (If 2+ chunks use `slow push in` in `SHOT 1`, STOP and rewrite using lateral tracking, crane rise, dolly out, overhead 90° drift, or foreground-occluded glide).
- [ ] **Opening Archetype Diversity:** Does every chunk in the batch open with a distinct framing archetype from `camera/angles.md`? Zero consecutive `Cinematic medium shot` openings.
- [ ] **2-Chunk Location Ceiling (Rule #26):** Are there ZERO instances of 3+ consecutive chunks trapped in the same interior room or `@LOCATION` tag?
- [ ] **Subtext Extraction (Rule #42):** Does every chunk translate the narration into a compelling physical human transaction, contrast cut, or architectural scale metaphor rather than writing literal captions of the words?
- [ ] **Multi-Beat Clause Mapping (Rule #33):** If a chunk's narration mentions multiple distinct events, places, or clauses, are ALL of them mapped sequentially (`SHOT 1–2` $\rightarrow$ `SHOT 3–4` $\rightarrow$ `SHOT 5–6`)?

### B. Anti-Slop & Physics Integrity Checks
- [ ] **4-Layer Persistence in Shots 2–6 (Rule #14):** Does EVERY individual shot line (`SHOT 1` through `SHOT 4/6`) include a compact Lens/Light + Texture/Mood anchor (`35mm lens, deep shadows, film grain`) so Grok never drops the photographic grade on cuts?
- [ ] **Start Frame = Shot 1 Frame 0 Alignment (Rule #27 & #41):** Does `SHOT 1` match the Start Frame's exact environment, subject, lighting, and initial camera geometry 100%? Zero unanchored orbital-to-street morphs inside a single clip.
- [ ] **Zero Fine Hand / Tool Mechanics (Rule #40):** Are there ZERO fountain pens writing, markers drawing, highlighters streaking, rubber stamps pressing ink, fingers typing on keyboards, or calipers/loupes held in hands?
- [ ] **Zero Multi-Character Combat / Contact (Rule #39):** Zero wrestling, tackling, grappling, or colliding bodies (pre-impact tension and post-impact aftermath only).
- [ ] **Zero Reflections / Moving Doors / In-Clip Text:**
  - Zero character reflections in windows, mirrors, or monitor glass.
  - Zero doors opening or closing mid-shot.
  - Zero requests for readable English text/sentences on screens or papers inside the prompt.
  - Zero frontal face shots combined with readable laptop screens (always use OTS for screens per Rule #28).
- [ ] **Zero Inert Object Wandering & Zero Empty-Room `--no people` Bypasses (Rule #37 & #44):**
  - Zero cameras wandering across empty desks, paper stacks, brass lamps, or empty courtroom pews.
  - In sensitive/moderation-prone chunks, human tension is preserved via backlit silhouettes, OTS framing past a suit jacket, marching boots, hands gripping a rail, or courtroom observers—NEVER `--no people, faces` on empty rooms.

### C. Tagging & Format Checks
- [ ] **Harmonized Tagging (Rule #12):**
  - Start Frame tags ONLY locked assets physically visible in Shot 1, Frame 0.
  - Video Prompt header (`Use @image1 as visual anchor for start frame...`) tags ALL locked assets appearing anywhere in Shots 1–4/6.
  - `@TAG` is placed at the VERY BEGINNING of each shot line where the asset appears.
- [ ] **Word Count & Pacing:**
  - 4 shots per 10s chunk (`SHOT 1/4`–`4/4`) or 6 shots per 15s chunk (`SHOT 1/6`–`6/6`).
  - Every shot line is **18–34 words** (strictly under 35 words).
- [ ] **CTA Purity (Rule #20):** Zero logos, subscribe buttons, or phone screens in CTA chunks.
