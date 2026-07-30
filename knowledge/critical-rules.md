# Critical Rules

Hard-learned rules from live production. NEVER VIOLATE. Single source of truth.

---

## ⚠️ MANDATORY SESSION STARTUP PROTOCOL — EXECUTE BEFORE ANYTHING ELSE

Before generating ANY prompt, you MUST do ALL of the following IN ORDER:

1. Read `critical-rules.md` in full ← you are reading this now
2. Read `additional-rules.md` in full
3. Read `learnings.md` in full
4. Read `session-postmortems.md` to know what mistakes were made before
5. Open and read the `.vst` timing file provided by the director
6. Confirm to director: "I have read all repo files. Ready to generate."

**This is not optional. Not skippable. Not replaceable by memory or context summaries.**
Every session starts with this protocol. Every single time.

---

## Character Rules

### Rule #1 — Characters NEVER posed
- Characters are NEVER posed. Always caught mid-action.
- Not "standing" but "one foot crossing the threshold, one still outside"
- Test: could you freeze this frame and have implied motion? Yes = correct.

### Rule #2 — Show person, not objects
- When VO names a living person → show THEM, not their objects
- From behind, side, silhouette, through glass — but THEM, alive, in motion
- Objects-only = only for ABSENCE scenes (person is gone)

### Rule #3 — Character descriptions in shots
- When character is ALONE → say "Clanton alone walking" etc.
- When with UNKNOWN people (not from tags) → say "with other inmates" or "with other people"
- When with LOCKED characters from tags → say "Clanton with James" or "with Briley brothers"
- Makes AI generator understand who appears in shot

### Rule #4 — Non-locked characters
- Describe with appearance details: "African American man, short hair, prison uniform"
- Don't use @TAG for characters without reference sheets

---

## Camera Rules

### Rule #5 — Creative angles required
- Every scene must have at least ONE creative angle (worm's eye, dutch tilt, through-glass, macro, bird's eye, ground-level tracking, first-person POV, reverse angle, orbital arc)
- Never two push-ins in a row. Never three static holds.
- Reference `camera/angles.md` before every prompt generation

### Rule #6 — Visual variety
- Never repeat camera movements, body movements, scenes, or locations
- Always introduce new angles and movements to catch viewer attention
- Minimum 3 different camera movements across 4 shots

### Rule #7 — Shot count by word count
- 2–5 words → 2 shots ONLY
- 6–12 words → 3 shots
- 13–20 words → 4 shots
- 20–30+ words → SPLIT into 2 scenes, 4 shots each

---

## Prompt Rules

### Rule #8 — Locked asset tags at beginning
- ALWAYS tag locked assets at VERY BEGINNING of prompt — even if character only appears in final shot
- NEVER put tags in middle of prompt
- Tag placement: @TAG1 @TAG2 at start, then description
- Example: "@BRILEY_JAMES African American man walking..." NOT "African American man @BRILEY_JAMES walking..."

### Rule #9 — Locked asset prompts start with "@ [NAME]"
- Format: "@ Mecklenburg Prison Exterior\n[actual prompt]"
- Allows searching by name in Google Flow and other tools

### Rule #10 — Locked characters outside prison
- When using locked characters in non-prison scenes, describe new outfit + reference facial features
- Format: "@TAG same facial features as locked reference, now wearing [new outfit]"

### Rule #11 — Locations as tags
- Only use @TAG for LOCKED locations (@MECKLENBURG, @DEATHROW, @GATEHOUSE)
- Don't use @TAG for generic locations (Vermont, Warrenton, community)

### Rule #12 — Tag where asset appears
- If character/location is NOT visible in start frame, do NOT tag them in start frame
- Only tag in the specific SHOT where they actually appear
- Start frame tags = only assets visible in that image

---

## Video Prompt Format

### Rule #13 — Tags only at beginning
- Tags ONLY at beginning + in "Use @image1 as visual anchor" line
- Do NOT add extra tag line before anchor line
- Format:
```
Use @image1 as visual anchor for start frame @TAG1 @TAG2.

SHOT 1/4 @TAG1 description...
SHOT 2/4 @TAG2 description...
```

### Rule #14 — Avoid AI slop
- Never use generic descriptions
- Each shot needs: specific visual details, lighting, atmosphere/mood, texture (grain, halation), camera movement, emotional beat
- Bad: "Wide shot FBI agents alone surrounding garage"
- Good: "Wide shot FBI tactical team surrounding garage at night, spotlights cutting through fog, tense atmosphere, harsh shadows on concrete walls, 35mm lens, deep focus, thriller mood, film grain"

### Rule #15 — No split images
- Always single-frame shots
- Split screens look like AI slop and break immersion
- Never write "split screen" in any shot description

### Rule #16 — Match script time of day
- If script says "night" or "evening", prompts MUST be set at NIGHT
- Don't default to day. Lighting must match narration.

### Rule #17 — Corrections = completely new ideas
- When redoing prompts, never reuse old angles, compositions, or ideas
- Fresh camera angles, fresh perspectives, fresh emotional beats every time

---

## Generator Rules

### Rule #18 — Kling negative prompts
- Kling: negative prompt goes in SEPARATE field in UI
- NEVER --no flags inside Kling prompt body → causes "Something went wrong"
- --no flags are Grok syntax only

### Rule #19 — Grok prompt format
- Under 35 words for best results (complex prompts cause hallucination)
- `--no` flags at end of prompt for negatives
- `--ar 16:9` for aspect ratio
- Always include "cinematic" or "film" in every prompt

### Rule #20 — No floating elements
- NEVER use floating items, floating text, floating logos, weird glowing effects
- Papers should be stacked, held, on desks — never floating in air
- Money should be in counting machines, stacks on tables, or in hands — never floating
- CTAs use graphics, phone screens, logos — never people speaking/waving

---

## Workflow Rules

### Rule #21 — Read full script before generating
- Don't just look at the chunk
- Read the surrounding context to understand what's happening
- Stay in storyline
- Many mistakes come from not understanding the full scene

### Rule #22 — Work in batches
- Work in batches of 4-6 chunks
- After each batch, wait for "done" before next batch
- User approves before continuing

### Rule #23 — User provides chunks
- Agent is BAD at chunking from SRT
- NEVER parse SRT to create chunks
- User will always provide a pre-chunked file
- If user gives you SRT, ask for the chunked file instead

### Rule #24 — Trust user corrections
- When user corrects chunk timing or narration, accept it immediately
- User knows the correct sync
- Do not argue or re-pars