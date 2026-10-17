# Additional Production Rules

Production workflow, cinematography craft, and prompt execution rules. Supplements `critical-rules.md` and `camera/angles.md`.

---

## 1. The 4-Layer Prompt Build (Mandatory in Every Start Frame & Every Video Shot)

Every Start Frame AND every individual Video Shot line (`SHOT 1` through `SHOT 4/6`) MUST include all 4 layers:

1. **Subject & Action** — Who/what is in frame, caught in purposeful gross-motor motion (never posed, never using fine finger tools/pens/keyboards).
2. **Camera & Motion** — Explicit framing archetype + movement from `camera/angles.md` (e.g., foreground-occluded lateral track, worm's-eye crane rise, 90° bird's-eye drift, OTS pan, low-angle Dutch dolly back).
3. **Lens & Light** — Focal length (`24mm`/`35mm`/`50mm`) + specific lighting contrast (`chiaroscuro side light`, `sodium vapor mist`, `cold clinical teal`, `slanted golden-hour blinds`).
4. **Texture & Mood** — Analog film finish (`35mm film grain`, `anamorphic halation`, `Fincher documentary tension`, `high-contrast desaturated grade`).

### Why Shots 2–6 Must Keep Compact Layer 3 & 4 Tokens:
In Grok Imagine, `SHOT 1` inherits the visual anchor (`@image1`), but **`SHOT 2` through `SHOT 4/6` cut to new angles or locations**. If `SHOT 2`–`6` omit lens, lighting, and texture tokens, the model drops the photographic look on the cut and generates flat, plastic CGI slop. Always include a compact 4–6 word style anchor (`35mm lens, deep shadows, film grain`) in every shot line while keeping each shot line under 35 words.

---

## 2. Subtext & Scene Staging Craft

### Never Illustrate Words Literally
- Do NOT turn voiceover words into literal stock-photo descriptions.
- Translate abstract claims into **visceral human status dynamics** or **monumental physical consequences** (see `camera/angles.md` Section 3).

### Depth & Foreground Composition (Make It Look Like a Movie, Not CCTV)
- Never place a subject flatly in the middle of an empty room or corridor.
- Build **3 planes of depth** in every composition:
  - **Foreground:** Out-of-focus doorframe, Venetian blinds, rain-streaked glass, archive shelving edge, or shoulder silhouette.
  - **Midground:** Primary subject in purposeful gross-motor motion.
  - **Background:** Architectural geometry, practical light sources, or environmental activity.

### Creative Edit-Level Transitions
- Design the final shot of Chunk $N$ and the Start Frame of Chunk $N+1$ to cut together with intent:
  - **Contrast Cut:** Cut from extreme wealth/power (e.g., sunlit corporate keynote stage) directly to hidden exploitation or aftermath (e.g., cramped midnight back-office or rain-slicked port yard).
  - **Graphic Match:** Match a geometric shape across cuts (e.g., circular turbine $\rightarrow$ circular radar sweep).
  - **Continuous Drone Chaining:** When requested by the director, the last frame of Clip $N$ becomes the Start Frame of Clip $N+1$. Keep continuous trajectories within a single physical scale—never morph from outer space to a street doorway in one unanchored clip.

---

## 3. Pacing & Timing Rules

- **Golden Ratio Pacing (~2.5s per shot):**
  - **10-second chunks:** 4 shots (`SHOT 1/4` to `SHOT 4/4`).
  - **15-second chunks:** 6 shots (`SHOT 1/6` to `SHOT 6/6`).
  - **Short Phase 3 Pickups (1–5s):** 2 or 3 shots (`SHOT 1/2` to `2/2` or `SHOT 1/3` to `3/3`).
- **Timing Calculation:** ~27 words or 145 characters (including spaces) = 10 seconds of narration.
- **Sequential Clause Mapping (Rule #33):** Act as a strict sequential visual director. When a chunk contains 2 or 3 distinct narrative clauses or locations, map Clause A $\rightarrow$ `SHOT 1–2`, Clause B $\rightarrow$ `SHOT 3–4`, Clause C $\rightarrow$ `SHOT 5–6`. Never trap multi-beat narration in a single room.

---

## 4. Subscribe / CTA Rules (Strict Zero-UI Policy)

- **NEVER** show people talking to camera, waving goodbye, or asking to subscribe.
- **NEVER** generate channel logos (`@channellogo`), subscribe buttons, like icons, notification bells, or phone screens with YouTube UI.
- All CTA chunks MUST feature **moody, atmospheric, story-world cinema** (e.g., monumental crane pull-back from a rain-slicked skyscraper at midnight, low-slung tracking shot along a misty border river, researcher walking down a vaulted archive aisle).
- The director adds all brand and YouTube UI overlays manually in Premiere Pro.

---

## 5. Mandatory Batch-Level Pre-Flight Verification

Before outputting ANY 6-chunk batch in Phase 2, evaluate every chunk against these non-negotiable checks:

1. **Batch Opening Diversity (`SHOT 1` Rule):**
   - Did you use `"slow push in"` in `SHOT 1` at most **ONCE** across all 6 chunks?
   - Does each of the 6 chunks start with a different framing archetype from `camera/angles.md`?
2. **2-Chunk Location Ceiling:**
   - Are there zero instances of 3+ consecutive chunks trapped in the same interior room or `@LOCATION` tag?
3. **Zero Fine-Hand / Tool Slop (Rule #40):**
   - Are there ZERO fountain pens writing, markers drawing, highlighters streaking, rubber stamps pressing, fingers typing on keyboards, or calipers/loupes held in hands?
4. **Zero Banned Physics & Geometry Slop:**
   - Zero character reflections in glass/monitors.
   - Zero doors opening or closing mid-shot.
   - Zero readable English text/headlines requested inside the image/video generation.
   - Zero frontal face shots combined with readable laptop screens (always use OTS for screens).
   - Zero multi-character physical grappling or combat.
5. **Moderation-Safe Human Tension (Rule #44):**
   - If a chunk is sensitive (trial, arrest, medical crisis), did you preserve human tension via silhouettes, OTS framing, and observers instead of lazily dumping `--no people, faces` on empty rooms?