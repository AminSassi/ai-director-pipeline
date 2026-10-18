# Learnings

Accumulated corrections and discoveries from live production sessions. Updated automatically when the director shares insights.

**Note:** This file contains validated production insights synchronized with `critical-rules.md`, `additional-rules.md`, and `camera/angles.md`. Historical entries that were superseded by later post-mortems have been updated in-place so there are **zero contradictory instructions**.

---

## Validated Production Insights (Chronological Log)

- [2026-06-25] INSIGHT: Reflection shots in screens/laptops/windows cause AI to generate weird cloned/duplicated person effects. NEVER use `"reflection visible in screen"` or mirror reflections of characters. Avoid any shot where a character appears inside a reflective surface.

- [2026-06-25] INSIGHT: No super fast camera motion — causes AI artifacts and breaks generation. Keep camera trajectories smooth, deliberate, and single-axis.

- [2026-06-25] INSIGHT: Plastic/humanoid looking characters — specify realistic skin texture, fine pores, hair detail, and natural clothing folds in Start Frames and non-locked character descriptions.

- [2026-06-25] INSIGHT: Before EVERY prompt generation session, re-read the full GitHub repo rules in order (`critical-rules.md`, `additional-rules.md`, `learnings.md`, `session-postmortems.md`, `camera/angles.md`, `style/rules.md`, `golden-reference-mladic.md`, `golden-reference-aurora.md`).

- [2026-06-25] INSIGHT: "Stamp being pressed", fountain pens writing text, highlighters streaking, and fingers typing on keyboards cause AI video models to spawn oversized rubber stamps or melt 6-fingered hands (see Rule #40). Keep documents/screens already written or printed, and use gross-motor character actions (closing a folder, leaning over a desk, walking mid-stride, turning from a window).

- [2026-06-25] INSIGHT: When describing an analyst or hacker at screens, ALWAYS use **Over-The-Shoulder (OTS)** framing (`"Over-the-shoulder view looking past analyst toward screen"`). Otherwise, AI puts screens facing the viewer on the back of the monitor lid (see Rule #28).

- [2026-06-25] INSIGHT: Doors in AI video are unreliable — they open/close spontaneously, multiply, or morph. AVOID doors opening or closing mid-shot entirely; keep doorways already open or closed, or shoot through an open doorway threshold.

- [2026-06-25] INSIGHT: Over-describing details in video prompts causes Grok to hallucinate. Keep each video `SHOT` line **under 35 words** (target 18–28 words) while retaining compact 4-layer tokens (Subject/Action + Camera/Motion + Lens/Light + Texture/Mood).

- [2026-06-25] INSIGHT: "Torn paper style" — when user asks for this: `Aged paper texture background, black and white photograph style, bold typewriter font, aged sepia and greyscale tones, film grain texture, high contrast shadows, investigative documentary thumbnail style, 4K, --ar 16:9, --no blur --no watermark --no artifacts --no distortion --no photorealism.` Photo should look like printed article clipping with white border around image.

- [2026-06-25] INSIGHT: Locked Assets Workflow — Before generating chunk prompts, identify ALL recurring characters, locations, and signature vehicles/objects that appear more than once. Present reference sheet prompts for each in Phase 1 FIRST. Wait for the director to generate and lock them before starting Phase 2.

## LOCKED ASSET TEMPLATES (USE THESE)

### CHARACTER REFERENCE SHEET TEMPLATE
```
@ [CHARACTER NAME]
Professional character reference sheet, technical model turnaround style, clean neutral plain background, photorealistic. [CHARACTER DESCRIPTION]. Two horizontal rows. Top row: four full-body standing views — front view, left profile view facing left, right profile view facing right, back view. Bottom row: three close-up portraits — front portrait, left profile portrait facing left, right profile portrait facing right. Relaxed A-pose, consistent scale, accurate anatomy, clear silhouette, even spacing, uniform framing, consistent head height and facial scale across all panels. Same direction intensity and softness lighting across all panels, natural controlled shadows. Canon SL3, 17-85mm lens, fine pores, DSLR photography look, no airbrush, no CGI retouch, no text overlays. Landscape 16:9 --no white background or white bars
```

### LOCATION REFERENCE SHEET TEMPLATE
```
@ [LOCATION NAME]
Professional location reference sheet, full-frame photographs, no borders, no margins. Arrange into a grid of six views filling entire image: top row — wide establishing shot of [LOCATION 1], medium shot of [LOCATION 2], close detail of [LOCATION 3]. Bottom row — aerial view of [LOCATION 4], [LOCATION 5], [LOCATION 6]. Each photo fills its panel completely, no white space, no grey background. [LOCATION IDENTITY DESCRIPTION]. Natural lighting, photorealistic, Canon SL3, 17-85mm lens. No text overlays. Landscape 16:9
```

- [2026-06-25] INSIGHT: Grok "expand video" feature extends from last frame — use for scene transitions when requested.

- [2026-06-25] INSIGHT: Image prompts (Start Frames) set rich environmental detail; Video prompts animate the scene with clean gross-motor action beats and camera trajectories.

- [2026-06-25] INSIGHT: Brand names (iPhone, Sony, Google, Facebook) can trigger generator filters — describe devices generically when possible.

- [2026-06-25] INSIGHT: Thumbnail prompts with "dark room" can make the main subject's face too dark. Use `"high-contrast bright rim lighting on face, clear facial features visible"` while keeping the negative space dark slate/black.

- [2026-07-17] INSIGHT: NEVER use generic detective noir clichés (fedora silhouettes, generic neon rain) unless grounded in the actual historical setting.

- [2026-07-17] INSIGHT: NEVER repeat the same first frame, same camera plan, same angle, or same staging idea across consecutive chunks. Always introduce fresh visual approaches from `camera/angles.md`.

- [2026-07-17] INSIGHT: "Open parentheses" = Seedance 2.0 mode. "Close parentheses" = Grok mode. Switch between them only as director instructs.

- [2026-07-17] INSIGHT: Always include exact script text before each chunk prompt so director can verify sync.

- [2026-07-17] INSIGHT: Push changes to GitHub immediately after saving to `learnings.md` — director uses multiple PCs and needs a synced repo.

- [2026-07-23] INSIGHT: Leonardo DiCaprio — Not locked as a reference sheet, but user uses his online pictures. Tag as `@DICAPRIO` when he appears in shots.

- [2026-07-23] AI SLOP PATTERNS — NEVER DO THESE:
  1. `"papers flying through air"` or `"exploding outward"` — Papers stay flat on desks or inside closed folders held by characters.
  2. `"calendar pages flying off"` — Banned.
  3. `"money flying through fingers"` or `"flowing across screen"` — Money stays physical in vault stacks or counting machines.
  4. `"person waving goodbye"` or `"person talking to camera asking to subscribe"` — Banned. CTAs use atmospheric story-world scenes only (Rule #20).
  5. `"Talking head for narrator moments"` — Banned. Never frame someone looking at the lens speaking.
  6. `"Readable English sentences/text in video clips"` — Banned. AI renders alien gibberish glyphs. Always use `--no text, words, numbers, labels`.

- [2026-07-23] CRITICAL: MiMo UI has a rendering bug where long text appears without spaces. When running inside MiMo UI, write long metadata/descriptions to a file first.

- [2026-07-24] STYLE: ElevenLabs VO target is **1400 ±25 words** (spoken narration text in Phase 0.4 only). Always verify the exact word count of Phase 0.4.

- [2026-07-25] INSIGHT: ALWAYS paste the final ElevenLabs script (Phase 0.4) directly in chat after creating it so the director can copy-paste immediately.

- [2026-07-25] INSIGHT: Pipeline order is: `Channel Gate → Phase 0 (Expand) → Phase 0.1 (CTAs) → Phase 0.2 (Verify) → Phase 0.3 (Compress) → Phase 0.4 (ElevenLabs VO) → Phase 0.45 (Suno Prompt) → [WAIT FOR .vst/.srt] → Phase 0.75 (Routing) → Phase 1 (Locked Assets) → Phase 2 (Prompts)`.

- [2026-07-25] INSIGHT: Suno music prompts must avoid high-pitched opening noise or chaotic crashes; keep them slow-building, pulse-driven, and end with `[Instrumental]` under 200 words.

- [2026-07-25] CRITICAL: NEVER touch, re-split, or re-parse the director's `.vst` / pre-chunked `.srt` timing file. Use its chunk boundaries and narration text verbatim.

- [2026-07-25] CRITICAL: ONLY use Grok Imagine for video generation and Nano Banana 2 (Flow) for Start Frames and Reference Sheets. Kling is retired.

- [2026-07-26] CRITICAL UI FORMAT: Output each chunk in 3 distinct blocks:
  1. Exact narration text in plain text (NOT inside a code block).
  2. Start Frame prompt inside its own code block.
  3. Video Prompt inside its own separate code block.

- [2026-07-26] CRITICAL HALLUCINATION PREVENTION: If script text for any chunk is missing from context, STOP immediately and read it from the timing file or ask the director. Never guess narration text.

- [2026-07-30] INSIGHT: VISUAL TONE & VIBE. Never make chaotic scenes with people running, fighting, screaming, or frantic crowds. Build tension through **Fincher stillness, isolation, deep shadows, foreground occlusion, and stark architectural composition**.

- [2026-07-31] CRITICAL: NEVER call an image-generation tool yourself. The director wants plain-text prompts only, ready to copy-paste into Nano Banana / Grok.

- [2026-08-14] INSIGHT: To prevent vehicles (helicopters, planes, cars) from moving backward in AI video, explicitly state the vehicle's forward movement AND camera direction (e.g., `"sedan driving forward along highway, camera tracking forward parallel"`).

- [2026-08-28] CRITICAL: CTA VISUAL RULE. In CTA sections of the script (subscribe, like, comment, notification bell), **NEVER** generate channel logos, subscribe buttons, comment sections, bell animations, or phone screens. Always generate a **moody, atmospheric, story-relevant scene** (e.g., wide crane pull-back over a rain-slicked harbor, dark executive tower in mist, solitary researcher in vaulted library). The director adds CTA graphics in Premiere Pro.

- [2026-08-30] INSIGHT: YouTube Packaging — Produce 1 long video package: 3 title options (for A/B testing) + description + tags. Titles must follow the two-part em-dash format: `[Main Subject / Entity] — [The Core Hook / Discovery / Crime / Event]`.

- [2026-09-01] CRITICAL: GOLDEN RATIO PACING (~2.5 seconds per shot):
  - **10-second chunks:** 4 shots (`SHOT 1/4` through `SHOT 4/4`).
  - **15-second chunks:** 6 shots (`SHOT 1/6` through `SHOT 6/6`).
  - **Short Phase 3 Pickups (1–5s):** 2 or 3 shots (`SHOT 1/2`–`2/2` or `SHOT 1/3`–`3/3`).
  - Full benchmark saved in `knowledge/golden-reference-mladic.md`.

- [2026-09-01] CRITICAL: PRESENT LOCKED ASSET REFERENCE SHEETS FIRST (Phase 1). After receiving the timing file and completing routing, ALWAYS present all character and location reference sheet prompts and wait for the director to say `"done"` before generating Batch 1 chunk prompts.

- [2026-09-03] CRITICAL BATCH SIZE RULE: Always generate and output **EXACTLY 6 chunks per batch** in chat (Chunks 1–6, 7–12, 13–18, etc.), preceded by the Pre-Generation Audit Matrix and followed by the Post-Generation Audit Summary.

- [2026-09-09] INSIGHT: Never lock generic one-off institutional rooms (like a standard courtroom); describe them richly by architecture and lighting. Only lock recurring signature characters, vehicles, and primary story locations.

- [2026-09-10] INSIGHT: Realistic Datacenter Infrastructure — Servers must always be mounted inside standard matte-black enterprise rack cabinets on steel rails with perforated mesh doors and clean cable management—never freestanding pedestals or sci-fi glowing pillars.

- [2026-09-10] INSIGHT: Pure Camera Motion for Continuous Drone Chaining — When executing a continuous multi-clip drone chain (where Last Frame of Clip $N$ = Start Frame of Clip $N+1$), keep the trajectory within a contiguous physical scale and focus the video prompt on smooth camera flight mechanics. Never try to morph from outer space to a street gate inside a single unanchored clip.

- [2026-09-10] CRITICAL: CHRONOLOGICAL ATTIRE & BAREFOOT RULE. Only depict a specific quirk (e.g., barefoot) in the exact chunk where the narration states it; in all other chunks, use standard chronological attire.

- [2026-09-12] CRITICAL: HACKER & TECH EPISODES VISUAL DIVERSITY RULE (See `knowledge/golden-reference-aurora.md`). Never trap an episode in server rooms and desks. Manifest real-world physical transactions and infrastructure: chemical tankers, ports, automated warehouses, offshore rigs, county deed vaults, and street-level human drama.

- [2026-09-13] CRITICAL: ANTI-SCI-FI & GROUNDED DOCUMENTARY REALISM RULE (Rule #25). Zero cyberpunk, neon blue LEDs, or holograms. 100% Frontline / BBC documentary realism.

- [2026-09-13] CRITICAL: START FRAME & SHOT 1 100% VISUAL ALIGNMENT RULE (Rule #27 & #41). `SHOT 1` Frame 0 literally IS the Start Frame (`@image1`). `SHOT 1` must match the Start Frame's exact environment, subject, lighting, and initial camera framing 100%, animating it with a purposeful camera trajectory (vary the trajectory across chunks—do NOT default every chunk to `"slow push in"`!). Any cut to a new angle or location begins at `SHOT 2`.

- [2026-09-18] CRITICAL: PHYSICAL CAMERA GEOMETRY — THE LAPTOP SCREEN PARADOX (Rule #28). Never shoot a character's face from the front while describing readable UI on their laptop/monitor screen. Use **Over-The-Shoulder (OTS)** framing whenever screens or documents are viewed. In frontal/profile shots, describe only the ambient monitor glow on their face.

- [2026-09-18] CRITICAL: MASCOT TAG DISCIPLINE (Rule #29). Never prefix a human character prompt with a mascot tag (`@cyberleek`).

- [2026-09-18] CRITICAL: GROK IMAGE-TO-VIDEO SAFETY FILTER PROTECTION (Rule #31). Never use gendered nouns (`female`, `woman`, `girl`) on imported faces, NSFW heuristics (`vigorous`, `erotic`), biological tokens (`enamel`), or real-world famous surnames in Grok prompt text (use `@TAG` + anonymous role descriptions like `senior diplomat`, `chief neurologist`, `elderly inmate`).

- [2026-09-20] CRITICAL: MULTI-BEAT NARRATIVE COVERAGE (Rule #33). When narration mentions multiple distinct events or places in one chunk, map Clause 1 $\rightarrow$ `SHOT 1–2`, Clause 2 $\rightarrow$ `SHOT 3–4`, Clause 3 $\rightarrow$ `SHOT 5–6`. Never trap multi-event narration in one location.

- [2026-09-22] CRITICAL: MANDATORY CHANNEL SELECTION GATE (Rule #35). Always ask `"Which channel are we producing for today? 1. Verion | 2. Insolvent"` at session start and wait for confirmation before Phase 0.

- [2026-09-25] CRITICAL: HARMONIZED TAG DISCIPLINE — START FRAME VS. VIDEO PROMPT (Rule #12):
  1. **Start Frame Prompt:** Tag **ONLY** the locked assets physically visible in that initial frame (`Shot 1, Frame 0`).
  2. **Video Prompt Header (`Use @image1 as visual anchor for start frame @TAG1 @TAG2.`):** Tag **ALL** locked assets that appear anywhere across Shots 1–4/6 of that chunk.
  3. **Individual Shot Lines (`SHOT X/Y @TAG ...`):** Place `@TAG` at the very start of each shot line where that asset appears.

- [2026-09-27] CRITICAL: BANKNOTE & CURRENCY FILTER BYPASS. Never prompt text-to-image generators to create legal tender reference sheets (triggers anti-counterfeiting blocks). Instruct the director to pull an authentic public-archive scan of the currency note and import it directly as the visual anchor.

- [2026-09-27] INSIGHT: YOUTUBE THUMBNAIL STYLE — OPTION 1 BENCHMARK. Left side: high-contrast B&W cutout portrait (bright face, razor-sharp rim light, subtle thin red contour line on shoulder). Right side: deep matte black/charcoal negative space with massive bold uppercase two-line title (Line 1 white sans-serif, Line 2 inside a solid saturated red rectangular box).

- [2026-09-30] CRITICAL: HOOK RETENTION & ANTI-DATE OPENING RULE. Never open a documentary script hook with a dry calendar date (e.g., `"On September 18, 2015..."`). Always open with a high-stakes psychological question, consumer betrayal, or immediate physical mystery.

- [2026-09-30] CRITICAL: CHRONOLOGICAL ASSET STATE (Rule #36). Never attach future investigative rigs, crash damage, or prison attire to an asset before that chronological beat occurs in the story.

- [2026-10-02] CRITICAL: THE ANTI-BOREDOM & ACTIVE HUMAN STAKES MANDATE (Rule #37). Strict zero-tolerance ban on cameras wandering around inert objects, empty desks, paper stacks, brass lamps, coffee mugs, or empty chairs. Every chunk must feature living humans in high-stakes psychological tension/gross-motor action, monumental real-world infrastructure scale, or high-end light-table/Vox explainer plates.

- [2026-10-06] INSIGHT: REAL PEOPLE = REAL NAMES FIRST. In Phase 1, list the real-world names and recommended image search queries for all real historical figures first so the director can pull real reference photos before generating turnaround sheets.

- [2026-10-08] CRITICAL: THE HIGH-END MOTION GRAPHICS & EXPLAINER PLAYBOOK (Rule #38). Motion graphics explainers are required for complex mechanisms, flight paths, and systemic flows, but MUST use one of the **Three Slop-Free Aesthetics**:
  1. **Tactile Forensic Light-Table:** Physical cyanotype blueprint or dark slate schematic lying flat on a wooden drafting lightbox (`35mm macro lens, top-down orthographic view, smooth macro camera dolly push`).
  2. **Vox Mixed-Media Paper Collage:** Flat matte charcoal (`#0D0E11`) or parchment backdrop, halftone print texture, archival cutouts with white paper borders, flat 2D vector route line tracing smoothly.
  3. **Orthographic 2D Vector Infographic:** Strictly flat 2D straight-on/top-down geometry, single-axis reveal.
  * **Hard Bans:** Zero in-clip text/numbers (`--no text, words, numbers, labels`), zero `3D CAD wireframe` or `isometric 3D cutaway` keywords, and only ONE simple motion per shot.

- [2026-10-08] CRITICAL POST-MORTEM #003 (FZ1073): PERMANENT HARD BANS ON AI SLOP TRIGGERS (Rules #39 & #40):
  1. **Ban Multi-Character Physical Contact & Combat (Rule #39):** Never prompt wrestling, tackling, grappling, or bodies colliding. Use pre-impact tension and post-impact aftermath.
  2. **Ban Fine Tool Manipulation & Finger Micro-Actions (Rule #40):** Never prompt fingers using calipers, magnifying loupes, fountain pens writing text, markers drawing, rubber stamps pressing ink, or fingers typing on keyboards.

- [2026-10-17] CRITICAL PIPELINE AUDIT UPGRADE — CLOSING THE 4 LOOPHOLES THAT CAUSED CAMERA MONOTONY & AI SLOP:
  1. **Killed the 98.2% `SHOT 1 slow push in` Cookie-Cutter Loop (`camera/angles.md` & Rule #6):**
     * Forensic audit of *Otto Warmbier* (55 chunks) proved the AI was gaming Rule #6 by using the exact same 4-shot sequence (`Shot 1: slow push in` $\rightarrow$ `Shot 2: OTS/low-angle` $\rightarrow$ `Shot 3: lateral track` $\rightarrow$ `Shot 4: 50mm hold`) 54 times in a row!
     * **New Permanent Law:** Across any 6-chunk batch, `"slow push in"` is allowed in `SHOT 1` **at most ONCE (max 1/6 chunks)**. Each of the 6 chunks must open with a distinct framing archetype from `camera/angles.md` (Foreground Occlusion, Worm's-Eye Crane, 90° Bird's-Eye Overhead, Low-Slung Surface Skim, Backlit Silhouette Pull-Back, OTS Reveal, Parallel Steadicam Glide, etc.).
  2. **Killed the 12-Chunk Single-Location Trap (The 2-Chunk Location Ceiling — Rule #26):**
     * Never set more than **2 consecutive chunks** inside the same interior room or `@LOCATION` tag. When narration analyzes theories or evidence over multiple chunks, cut out of the lab/office and visually manifest the physical world of the theories being discussed.
  3. **Killed the `--no people, faces` Empty-Room Lazy Bypass (Rule #44):**
     * When Grok moderation blocks a real person's face tag in a sensitive trial/medical/arrest chunk, **NEVER** strip all humans out of the batch with `--no people, faces` and film empty courtroom pews or empty desks (which directly violates Rule #37 Anti-Boredom Mandate). Instead, use **Moderation-Safe Human Framing**: backlit anonymous silhouettes, Over-The-Shoulder views past a dark suit jacket, booted feet marching down corridors, hands resting on a wooden defense rail, and tense courtroom/press observers.
  4. **Restored Mandatory 4-Layer Tokens Inside Shots 2–6 (Rule #14):**
     * Because Shots 2–6 cut away from the Start Frame (`@image1`), dropping lens, lighting, and film grain from Shots 2–6 caused Grok to render flat plastic CGI after every cut. Every shot line (`SHOT 1` through `SHOT 4/6`) must now include a compact 4–6 word style anchor (e.g., `35mm lens, chiaroscuro shadows, film grain`) while staying under 35 words.

- [2026-10-18] CRITICAL DIRECTOR RULE — STACK DETAILS IN START FRAME (ANTI-PLASTIC SKIN), KEEP GROK VIDEO PROMPTS ULTRA-SIMPLE:
  1. **Start Frame (Image Prompt) = Stack Rich Photorealistic Details & Anti-Plastic Skin:**
     * Stack rich physical, architectural, and texture details in the Start Frame prompt.
     * Always enforce raw DSLR photorealism to kill plastic AI skin: `raw DSLR photograph, Canon SL3, realistic skin texture, visible pores, natural skin imperfections, realistic fabric weave, natural lighting, 35mm film grain, no plastic skin, no airbrush, no CGI`.
     * Never overload a single Start Frame with 4–5 character reference tags at once (causes Nano Banana to mash faces into plastic slop). Keep Start Frames focused on 1–2 primary tags with crystal-clear staging.
  2. **Video Prompt (Grok Imagine) = Keep It VERY Simple & Easy (10–18 Words Per Shot):**
     * Grok performs best when each `SHOT` line is **very simple, short, and direct**: `[Subject doing one simple action in location]. [One simple camera movement].`
     * Do NOT overload Grok video shot lines with complex multi-clause sentences or stacked buzzwords—keep all the heavy visual detail in the Start Frame!

- [2026-10-18] CRITICAL DIRECTOR RULE — CHUNK 01 SIGNATURE OPENING (CONTINUOUS FPV / DRONE HOOK SHOT):
  * **Chunk 01 Must Always Be Visually Special & Catchy:** Never open Chunk 01 (`00:00 - 00:15`) with a flat, static interior room shot.
  * Always design Chunk 01 as a **showstopping continuous FPV / Steadicam / drone camera journey** gliding smoothly from one space into another (e.g., gliding from the rain-slicked midnight street / subterranean stairwell corridor down two stories underground right up to the massive sealed steel vault door and into the dark vault chamber) to immediately hook the viewer in the first 15 seconds.
