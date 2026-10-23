# Critical Rules

Hard-learned rules from live production. NEVER VIOLATE. Single source of truth.

---

## ⚠️ MANDATORY SESSION STARTUP PROTOCOL — EXECUTE BEFORE ANYTHING ELSE

Before generating ANY prompt, you MUST do ALL of the following IN ORDER:

1. Read `knowledge/critical-rules.md` in full ← you are reading this now
2. Read `knowledge/additional-rules.md` in full
3. Read `knowledge/learnings.md` in full
4. Read `knowledge/session-postmortems.md` to know what mistakes were made before
5. Read `camera/angles.md` and `style/rules.md` — master cinematography & visual style playbooks
6. Read `knowledge/golden-reference-mladic.md` and `knowledge/golden-reference-aurora.md` — the gold standard production benchmarks
7. Open and read the `.vst` / `.srt` pre-chunked timing file provided by the director (when in Phase 0.5+)
8. Confirm to director: "I have read all repo files. Ready to generate."
9. **MANDATORY CHANNEL GATE:** Explicitly ask the director: "Which channel are we producing for today? 1. Verion | 2. Insolvent" — never proceed to Phase 0 or insert any CTAs until answered.

**This is not optional. Not skippable. Not replaceable by memory or context summaries.**
Every session starts with this protocol. Every single time.

---

## Character Rules

### Rule #1 — Characters NEVER Posed (Gross-Motor Implied Motion)
- Characters are NEVER posed statically looking at the camera. Always caught mid-action in natural, grounded gross-motor movement.
- Examples: walking mid-stride down a colonnade, turning away from a panoramic window, leaning forward across a conference table, closing a heavy binder, stepping across a threshold.
- **Test:** Could you freeze this frame and see implied motion and psychological weight? Yes = correct.
- **Note (See Rule #40):** Keep motion to clean gross-motor body language. NEVER prompt fine finger/tool mechanics (no writing text with fountain pens, no pressing rubber stamps, no rapid keyboard typing, no calipers).

### Rule #2 — Show Living People, Not Inert Objects
- When VO names or implies a living person → show THEM in their environment, not isolated inanimate objects.
- From behind, side profile, silhouette, through glass partitions, or Over-The-Shoulder (OTS) — but THEM, alive, in purposeful motion.
- Objects-only shots are strictly reserved for explicit ABSENCE beats or monumental macro-infrastructure (see Rule #37).

### Rule #3 — Character Descriptions in Shots
- When character is ALONE → say `"@TAG [Name/Role] alone walking..."`
- When with UNKNOWN people (not from tags) → say `"with other executives"` or `"with clinical colleagues"`
- When with LOCKED characters from tags → say `"@TAG1 with @TAG2"`
- Makes the AI generator clearly understand how many subjects appear in the frame.

### Rule #4 — Non-Locked Characters
- Describe with specific appearance details and attire: `"senior forensic auditor in charcoal suit, silver hair, 60s"`
- NEVER use `@TAG` for characters or generic locations without locked reference sheets.

---

## Camera & Cinematography Rules

### Rule #5 — Mandatory Creative Framing Archetypes (Zero Generic Coverage)
- Every chunk must incorporate at least ONE distinct creative framing archetype from `camera/angles.md`:
  - **Foreground Occlusion (Frame-within-Frame):** shooting past a doorframe, Venetian blinds, glass partition, or shelving gap
  - **Architectural Worm's-Eye:** floor-level looking sharply up (`24mm lens`)
  - **God's-Eye Perpendicular (90° Bird's-Eye):** straight-down overhead view
  - **Low-Slung Surface Skimming:** skimming inches above wet asphalt, marble, or factory floors
  - **Backlit Chiaroscuro Silhouette:** stark high-contrast figure against window/threshold light
  - **Depth-Plane Macro Rack Focus:** shifting focus from foreground tactile evidence to background human reaction
  - **Low-Angle Dutch Tilt (15°):** canted horizon for psychological instability
  - **Over-The-Shoulder (OTS) Reveal:** looking past shoulder at screens, lightboxes, or dossiers
  - **Monumental Crane Rise / Pull-Back:** vertical scale reveal

### Rule #6 — Intra-Chunk & Inter-Chunk Camera Variety (The Anti-Monotony Law)
- **Within a chunk:** Minimum **3 different camera movements** across the shots. Never repeat the same camera movement in consecutive shots. Never use three static holds.
- **Across a 6-chunk batch (CRITICAL — NO COOKIE-CUTTER FORMULAS):**
  - **`SHOT 1` "Slow Push-In" Cap:** You may use `"slow push in"` in `SHOT 1` **at most ONCE per 6-chunk batch (max 1/6 chunks)**. The other 5 chunks MUST open `SHOT 1` with different camera movements (e.g., lateral tracking, crane rise, dolly out/pull-back, overhead drift, low-angle tilt up, OTS rack focus).
  - **Zero Consecutive Opening Shot Sizes:** Never start two consecutive chunks with the same shot size (e.g., do not start Chunk 1 and Chunk 2 both with `Cinematic medium shot`).
  - **Zero Recycled Shot Sequences:** Never copy-paste the same 4-shot or 6-shot movement template (`Shot 1 push in -> Shot 2 OTS -> Shot 3 lateral track -> Shot 4 50mm hold`) across multiple chunks.

### Rule #7 — Golden Ratio Shot Count (~2.5 Seconds Per Shot)
- **10-second chunks:** Generate **EXACTLY 4 shots** (`SHOT 1/4` through `SHOT 4/4`).
- **15-second chunks:** Generate **EXACTLY 6 shots** (`SHOT 1/6` through `SHOT 6/6`).
- **Short Pickup / Correction Cuts (Phase 3):**
  - 1–5 second micro-cuts → **2 or 3 shots** (`SHOT 1/2`–`2/2` or `SHOT 1/3`–`3/3`).
  - Full chunk replacements (10s / 15s) → full **4 or 6 shots**.
- Never go slower than ~2.5 seconds per shot in standard chunks; slower pacing gives the AI time to hallucinate and drift into slop.

---

## Locked Asset & Tagging Rules (Harmonized)

### Rule #8 — Tag Placement Syntax
- Tags ALWAYS go at the **VERY BEGINNING** of a line—never in the middle or end of a sentence.
  - ✅ Correct: `SHOT 3/4 @MERIWETHER John Meriwether turns slowly from the window...`
  - ❌ Wrong: `SHOT 3/4 A man @MERIWETHER turns slowly...`

### Rule #9 — Reference Sheet Prompt Header Format
- Reference sheet prompts in Phase 1 start with `@ [NAME]` on the first line (e.g., `@ [DR_KANTER]`), allowing quick search in Google Flow / Nano Banana.

### Rule #10 — Locked Characters in New Attire / Eras
- When a locked character appears outside their reference sheet outfit, specify: `@TAG same facial features as locked reference, now wearing [new outfit description]`.
- When a character spans decades (e.g., young vs. elderly), use strict chronological tags (`@Ratkoyoung` vs `@Ratkoold`) with an explicit cutoff date.

### Rule #11 — Only Lock Recurring Signature Assets
- Only use `@TAG` for locked assets defined in the episode's Phase 1 Locked Asset Register.
- Never lock generic institutional rooms (like a one-off courtroom) or generic cities/streets; describe them richly by architecture and lighting.

### Rule #12 — Harmonized Tagging Discipline: Start Frame vs. Video Prompt
1. **In the Start Frame (Image) Prompt:** Tag **ONLY** the locked assets physically visible in that initial frame (`Shot 1, Frame 0`). Do NOT tag characters or locations that only appear later in Shots 2–6 (tagging invisible assets in the image prompt forces Nano Banana to mash multiple locations/people into one frame).
2. **In the Video Prompt Header (`Use @image1 as visual anchor for start frame @TAG1 @TAG2.`):** Tag **ALL** locked assets that appear anywhere across any of the shots (`SHOT 1` through `SHOT 4/6`) in that chunk.
3. **In Individual Shot Lines (`SHOT X/Y @TAG ...`):** Place the `@TAG` at the start of every specific shot line where that asset is visible.

### Rule #13 — Do Not Re-Describe Locked Character Faces in Scene Prompts
- Once a character is locked via `@TAG`, do NOT re-describe their facial anatomy (moustache, eye color, hair cut) in Start Frame or Video Prompts—doing so causes the generator to override the reference sheet. Describe only their **action, posture, expression, framing, and lighting**.

---

## Prompt Construction & Anti-Slop Rules

### Rule #14 — Mandatory 4-Layer Build in Start Frames AND Every Video Shot
Every Start Frame AND every individual Video Shot (`SHOT 1` through `SHOT 4/6`) must contain all 4 layers:
1. **Subject & Action** (who/what in grounded gross-motor motion)
2. **Camera & Motion** (specific angle + movement from `camera/angles.md`)
3. **Lens & Light** (`24mm`/`35mm`/`50mm` lens, chiaroscuro shadows, sodium vapor, cold clinical teal, tungsten practicals)
4. **Texture & Mood** (`film grain`, `anamorphic halation`, `Fincher documentary tension`, `high-contrast grade`)
- **CRITICAL FOR SHOTS 2–6:** Because Shots 2–6 cut away from the Start Frame, you MUST include compact Lens/Light and Texture/Mood tokens (4–6 words, e.g., `35mm lens, harsh side shadows, film grain`) inside **every shot line** so Grok never loses the photographic grade and drifts into flat plastic CGI after a cut.

### Rule #15 — No Split Screens
- Always single-frame shots. Never write `"split screen"` or `"dual panel"` in any prompt. Append `split screen` to `--no` flags.

### Rule #16 — Match Script Time of Day & Chronology
- Lighting and weather must strictly match the time of day, season, and geographical setting stated in the narration.

### Rule #17 — Phase 3 Corrections = 100% Fresh Ideas
- When redoing prompts in Phase 3, never reuse failed camera angles, compositions, or staging. Invent a completely fresh visual approach.

### Rule #18 & #19 — Generator Syntax (Grok Imagine & Nano Banana 2)
- **Start Frames:** Generated in **Nano Banana 2 (Flow)**. Always include `"Cinematic"` and `--ar 16:9`.
- **Video Prompts:** Generated in **Grok Imagine**.
  - Keep every individual `SHOT` line **under 35 words** (18–28 words is the sweet spot: compact enough to prevent hallucination, rich enough to hold all 4 layers).
  - Always end the video prompt with `--ar 16:9 --no text, words, numbers, labels, watermarks, blur, split screen`.
  - **ZERO In-Clip Text Prompting:** Never ask the video or image model to render readable English sentences, headlines, or labels (e.g., never prompt `"screen reading Artificial Intelligence"` or `"paper reading United States District Court"`), as AI models render garbled alien glyphs. All readable text overlays are added in Premiere Pro.

### Rule #20 — Zero Floating Elements & Zero UI CTAs
- Never prompt papers, money, or objects floating in mid-air.
- **Strict Zero-UI CTA Rule:** In CTA chunks (Hook CTA, Midpoint CTA, Outro CTA), **NEVER** prompt subscribe buttons, notification bells, channel logos, comment sections, or phone screens showing YouTube. Always generate **moody, atmospheric, story-world scenes** (monumental architecture, rain-streaked glass, desolate highways, silent evidence rooms). The director adds brand overlays in Premiere Pro.

---

## Workflow & Pipeline Integrity Rules

### Rule #21 — Read Full Script Context Before Generating
- Understand the narrative arc of the entire act before writing chunk prompts so characters and locations stay 100% faithful to the story.

### Rule #22 — Batch Size Discipline (Always 6 Chunks Per Batch)
- Always generate and output **EXACTLY 6 chunks per batch** in chat (Chunks 1–6, 7–12, 13–18, etc.), preceded by the Pre-Generation Audit Matrix and followed by the Post-Generation Audit Summary. Wait for the director's approval (`"done"`) before generating the next batch.

### Rule #23 & #24 — Timing File (.vst / Pre-Chunked .srt) Is Sacred Ground Truth
- Never chunk a script yourself. Wait for the director's pre-chunked timing file.
- Copy-paste the exact narration text for each chunk verbatim. Never paraphrase, trim, or guess from memory.

---

## Visual Style, Realism & Anti-Slop Mandates

### Rule #25 — Anti-Sci-Fi & Grounded Documentary Realism
- Zero cyberpunk, neon blue LED glow, floating holograms, curved sci-fi consoles, or "space movie" aesthetics.
- 100% **Frontline / BBC / Fincher documentary realism**: natural daylight, standard dual-monitor office desks, whiteboards, physical paper dockets, matte steel enterprise server racks with perforated doors, and real industrial machinery.

### Rule #26 — World-Scale Visual Diversity & The 2-Chunk Location Ceiling
- **Hard Ceiling:** Never set more than **2 consecutive chunks** in the same interior room or locked location tag (e.g., never trap 10 chunks inside `@UC_MEDICAL_CENTER` or a single office).
- When narration discusses theories, investigations, or systemic impact, leave the office/lab and visually manifest the **real-world physical domain**: shipping terminals, chemical tankers, factory assembly lines, prison corridors, border bridges, courthouse archives, or tactile forensic light-table plates.

### Rule #27 & #41 — Absolute Anchor Alignment (Start Frame = Shot 1, Frame 0)
- In Grok Imagine (`@image1`), the Start Frame **IS literally Shot 1, Frame 0**.
- `SHOT 1` must match the Start Frame's exact location, subject, lighting, and initial camera framing 100%, animating it with a purposeful camera movement (not always a push-in—use lateral tracking, crane rise, dolly out, tilt, or OTS pan!).
- **No Unanchored Scale Morphs:** Never use a satellite view of Planet Earth as a Start Frame and ask Shots 1–4 to dive all the way into a street-level building gate in one clip. Any transition to a new location, scale, or angle must happen via a clean cut starting at `SHOT 2`.

### Rule #28 — Mandatory Physical Camera Geometry (The Laptop / Screen Rule)
- **NEVER** frame a person from the front facing the camera while simultaneously describing what is displayed on their laptop/monitor screen (in physical reality, the camera is looking at the back of the laptop lid, forcing the AI to hallucinate a second screen on the back of the monitor).
- **For Screens/Lightboxes:** Always use **Over-The-Shoulder (OTS)** framing.
- **For Frontal/Profile Faces:** Describe ONLY the colored ambient monitor glow reflecting on their skin and eyes.

### Rule #29 — Never Tag Human Characters With Mascot Tags
- Never place a mascot tag (`@cyberleek`) on a prompt describing a human being.

### Rule #30 — Fincher Stillness vs. Cartoon Panic
- Never prompt frantic, chaotic AI action (flailing arms, running mobs, screaming faces, knocking over boxes).
- Build suspense through **stark composition, chiaroscuro lighting contrast, deep shadows, and deliberate, unhurried human movement**.

### Rule #31 & #44 — Moderation Filter Protection & Ban on Empty-Room `--no people` Lazy Bypasses
- **Trigger Prevention:** In Grok image-to-video (`@image1`), avoid gendered nouns attached to imported faces (`female`, `woman`, `girl`), sexual/NSFW heuristics (`vigorous`, `erotic`), biological tokens (`enamel`), medical vulnerability on imported faces (`hospital bed`, `feeding tube`, `corpse`), or famous real-world surnames in prompt text (use `@TAG` or anonymous role titles like `senior diplomat`, `elderly defendant`, `chief neurologist`).
- **CRITICAL (Rule #44 — Ban on Empty-Room `--no people` Lazy Bypasses):**
  - When a chunk covers a sensitive event (a coerced confession, a trial, an arrest, or a medical crisis) where a locked real-person face tag might trigger moderation, **NEVER strip all humans out of the batch with `--no people, faces` and film empty chairs/desks for 60 seconds!**
  - Instead, keep **high-tension human presence** using moderation-safe framing:
    1. **Anonymous Silhouettes & Backlit Figures:** Frame the subject from behind in stark silhouette against stage floodlights or courtroom windows.
    2. **Over-The-Shoulder (OTS) & Partial Framing:** Shoot past the back of a dark blazer or military shoulder toward a microphone array or judicial bench.
    3. **Purposeful Gross-Motor Detail:** Frame booted feet marching in unison down a concrete corridor, or clasped hands resting on a wooden defense rail.
    4. **Active Observers:** Show international journalists, translators in glass booths, diplomats, or court stenographers reacting in tense stillness.

### Rule #32 & #37 — The Anti-Boredom Mandate (Zero Inert Objects & Document Slideshows)
- **STRICT ZERO-TOLERANCE BAN:** The camera must **NEVER wander aimlessly around stationary objects, empty desks, paper documents, binders, folders, brass lamps, coffee mugs, empty courtroom pews, or ticking clocks.**
- Every single chunk must feature either:
  1. **Living Human Beings in High-Stakes Psychological Tension & Purposeful Action**, OR
  2. **Monumental Real-World Physical Scale** (vast industrial ports, automated factories, border bridges, storm-swept oil rigs), OR
  3. **High-End Tactile Forensic Light-Table / Vox Mixed-Media Plates** (Rule #38).
- Physical documents and folders exist **ONLY as props held or reviewed by a living person in the frame**—never as a standalone still-life subject on an empty table.

### Rule #33 — Multi-Beat Narrative Mapping (Zero Single-Location Trapping)
- When a chunk's narration references multiple distinct events, places, or clauses (e.g., *"ghost cities, a suspicious divorce, and a getaway to Canada"*), map each clause sequentially across the shots:
  - Clause 1 (Event A) $\rightarrow$ `SHOT 1–2`
  - Clause 2 (Event B) $\rightarrow$ `SHOT 3–4`
  - Clause 3 (Event C) $\rightarrow$ `SHOT 5–6`
- Never trap a multi-event narration inside a single static room.

### Rule #34 & #42 — Subtext Extraction & Dynamic Story Variety (The Golden Directorial Rule)
- **Never Write Literal Captions:** Do not lazily illustrate the surface words of the script. Before writing any prompt, extract the **subtext**:
  1. What is literally stated?
  2. What is the emotional, institutional, or psychological truth underneath?
  3. What specific physical human transaction, contrast, or architectural detail shows that truth without restating the words?
  4. Which of the 12 Camera Archetypes (`camera/angles.md`) amplifies that power dynamic?
- **Banned Clichés:** Never use generic server racks with glowing blue lights, matrix binary code, world maps with glowing dots, burning dollar bills, flying papers, or generic guy-at-laptop-typing shots.

### Rule #35 — Mandatory Channel Selection Gate (Verion vs. Insolvent)
- Never assume the channel. Always ask at session start: `"Which channel are we producing for today? 1. Verion | 2. Insolvent"` and wait for confirmation before Phase 0.

### Rule #36 — Chronological Prop & Asset State (Anti-Spoiler Rule)
- Every vehicle, character, and prop must match its exact chronological state at that second of the timeline (e.g., pristine factory-stock `@VW_JETTA` in consumer hooks vs. rigged with PEMS exhaust sensors only when researchers install them in Act 2; no prison attire before arrest).

### Rule #38 — High-End Slop-Free Motion Graphics & Explainer Protocol
- When explaining a complex mechanism, flight path, financial shell network, or timeline, use one of the **Three Slop-Free Explainer Aesthetics** (never crude 3D CAD wireframes floating in space):
  1. **Tactile Forensic Light-Table:** Physical cyanotype blueprint or dark slate schematic plate lying flat on a backlit wooden drafting lightbox (`crisp white vector linework, millimeter gridlines, 35mm macro lens, top-down orthographic view, smooth macro dolly glide`).
  2. **Vox Mixed-Media Paper Collage:** Flat matte charcoal (`#0D0E11`) or parchment backdrop, halftone texture, archival photo cutouts with white paper borders, flat paper-cut silhouettes, single solid route line tracing smoothly across a flat 2D map.
  3. **Orthographic 2D Vector Infographic:** Strictly flat top-down/straight-on 2D geometry, single-axis reveal, zero 3D perspective warping.
- **Motion Graphics Commandments:** Zero in-clip text/numbers (`--no text, words, numbers, labels`), only ONE simple motion per shot (camera glide OR single line trace), and never use `3D CAD wireframe` or `isometric 3D cutaway`.

### Rule #39 — Permanent Ban on Multi-Character Physical Contact & Combat
- Never prompt wrestling, grappling, tackling, fistfights, or bodies colliding (causes merged limbs and body horror).
- Direct physical conflict strictly through **Pre-Impact Tension** (eyes locking, knuckles gripping an armrest, boots striding fast, shadow under a door) and **Post-Impact Aftermath** (overturned chair, zip-ties on floor, solitary guard in hallway).

### Rule #40 — Permanent Ban on Fine Tool Manipulation & Micro-Hand Mechanics
- **STRICT ZERO-TOLERANCE BAN:** Never prompt fingers measuring with calipers, hands holding magnifying loupes, fountain pens writing cursive text, markers drawing lines, highlighters streaking across paper, rubber stamps pressing ink, or fingers typing on keyboards.
- Video diffusion models melt fingers into tools and spawn grotesque 6-fingered hands.
- **The Documentary Fix:** Frame documents/charts **already written or highlighted** resting on the desk while the character leans over them, folds them, holds a closed dossier while walking, or looks up in realization. Frame computer scenes OTS looking at the screen while the subject's hands rest stationary on the desk edge.

### Rule #45 — The Chunk 01 Signature Hook Rule (Catchy Continuous FPV / Drone Opening)
- **The First Chunk (`00:00 - 00:15`) Must Always Be Special:** Never open an episode in Chunk 01 with a flat, ordinary room shot.
- Design **Chunk 01** around a **breathtaking continuous FPV / drone / single-take camera journey** that glides smoothly through the environment from point A to point B (e.g., gliding across the rain-slicked midnight Diamond District street down two stories through subterranean security grates straight up to the massive sealed 3.5-ton steel vault door), giving the video a high-retention theatrical opening hook.

---

### Rule #46 — Permanent Ban on Aimless Camera Wandering & Filler B-Roll (Zero Purposeless Scenery)
- **STRICT ZERO-TOLERANCE BAN (DIRECTOR MANDATE):** The camera must **NEVER wander inside a scene with no narrative purpose**.
  - **Banned Clichés & Filler Archetypes:**
    1. **Aimless street wandering:** Camera drifting down a generic city street, gazing at storefronts, asphalt, or cars passing by with zero plot relevance.
    2. **Library / Archive wandering:** Camera drifting down book aisles, gliding along empty reading tables, or staring at book spines.
    3. **Purposeless object gazing:** Camera slowly tilting or panning over a book, binder, lamp, phone, clock, coffee cup, or desk stationery while nothing happens.
- **The Golden Litmus Test:** If you freeze any shot or mute the voiceover, does the scene show a **meaningful, motivated, physical human action event or dramatic transaction**? If it just looks like generic scenic B-roll, decorative wallpaper, or a passive museum tour, it is **BANNED AI SLOP**.
- **The Action Replacement Law:** Every camera trajectory must be anchored to active human conflict:
  - Don't wander down a street $\rightarrow$ show a grim-faced executive briskly crossing the street in rain while gripping a confidential folder, or an aggressive press photographer fighting for an angle.
  - Don't gaze at a book on a shelf $\rightarrow$ show an investigative auditor violently pulling a sealed archive box down, slapping a forensic ledger open, and stabbing a finger at a falsified entry.
  - Don't drift through an empty hallway $\rightarrow$ show employees abruptly carrying banker boxes out of an office after sudden termination.

---

### Rule #47 — 100% Script-to-Screen Action Sync & Smart Visual Storytelling (Instant Comprehension Law)
- **WHAT IS SAID MUST BE INSTANTLY UNDERSTOOD AND SEEN:** The viewer should NEVER have to wonder why a visual is on screen. The visual action must immediately, smartly, and unmistakably embody the exact sentence being narrated.
  - ❌ **Disconnected / Random:** Voiceover explains *"a disastrous private equity leveraged buyout that loaded the balance sheet with debt,"* but the video shows a random camera drifting past a library window or a pedestrian walking down the sidewalk.
  - ✅ **Synced & Smart:** Show a sleek high-rise conference room where predatory private equity partners in dark suits slide an intimidating mountain of debt binders across the mahogany table toward a sweating, cornered CEO, followed by a cut to workers outside carrying cardboard boxes.
- **People in Action Events (Not Passive Mannequins):**
  - Stop making characters stare blankly out windows or sit passively around tables.
  - Put people into **dynamic, high-stakes physical action events**:
    - Abrupt, angry walkouts from high-stakes negotiations
    - Tense whispered huddles in stairwells or fire escapes
    - Sudden shockwaves across trading floors or trading desks as tickers flash red
    - Regulators or bailiffs serving legal summons at corporate reception desks
    - Aggressive press scrums swarming an executive ducking into a black town car
    - Whistleblowers passing encrypted drives or dossiers across parking garage roofs
- **Fun, Smart, High-Craft Storytelling:**
  - Tell the story with wit, irony, and sharp visual contrast.
  - Pair ironic visual juxtaposition: when the script speaks of *"invincible market dominance,"* show the opulent marble foyer, then immediately contrast it with a cut to a cramped basement server room with overheating wires and panicked technicians.
  - When the script describes algorithmic takeover, show human photographers getting shoved aside by automated robotic camera rigs or a wall of screens displacing human editors.
- **Zero Pretending / Zero Hallucination:**
  - Never write prompts that merely "sound cinematic" while ignoring the specific narrative beat of that chunk.
  - Audit every single prompt against the exact words of the narration before presenting it.

