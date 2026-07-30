# Session Post-Mortems

Brutal honest error audits from live production sessions.
Every mistake documented here so it never happens again.

---

## POST-MORTEM #001 — LTCM Session [2026-07-30]

### Result: FAILED. Director had to redo entire 11-minute video.

---

### ERROR 1 — IGNORED THE GIT REPO RULES FROM SESSION START

**What happened:**
The AI started generating prompts WITHOUT reading `critical-rules.md`, `additional-rules.md`, or `learnings.md` first. Director had to explicitly say "read the rules in the git repo" multiple times during the session. Rules were already written and available. The AI just didn't read them.

**Rule violated:** `learnings.md` — "Always re-read repo files before starting prompt generation — director requires this every session."

**Fix going forward:** MANDATORY. Before generating a SINGLE prompt, the AI must read ALL THREE files: `critical-rules.md`, `additional-rules.md`, `learnings.md`. No exceptions. Not optional. Not skippable.

---

### ERROR 2 — CHAOTIC / FRANTIC VISUAL TONE FOR 35 CHUNKS

**What happened:**
From Chunks 1–35, the AI produced prompts with chaotic, frantic energy: crowds rushing, stamping, fast motion, people shouting, aggressive gestures, "stampedes." This directly violated the brand tone of INSOLVENT and the character of the story.

**Rule violated:** None existed at session start — but this is a fundamental creative judgment failure. The director had to explicitly say "stop the chaos and shouting and weird stuff." The AI should have understood from the repo's active scenes and emotional focus rules that FINANCIAL DOCUMENTARY requires TENSION THROUGH STILLNESS, not physical chaos.

**Director's exact words:** "I said there dont make still people and objects and camera just wandering around thats so boring, and at same time dont make chaos and people running or screaming or very angry doing weird mouvement."

**Fix going forward:**
- Financial/documentary content = tension through STILLNESS, isolation, shadows, deliberate motion.
- Action must be elegant: turning a page, gripping a desk, lowering a head.
- NEVER: running, shouting, fighting, stamping, crowds rushing, fast movement.
- Added to `learnings.md` [2026-07-30].

---

### ERROR 3 — MISSING START FRAME PROMPTS FOR CHUNKS 1–35 (EARLY SESSION)

**What happened:**
In the early batches of the session, the AI was generating only Video Prompts and missing the Start Frame (Nano Banana image prompt) for many chunks. The director had to explicitly ask: "BRO WAIT WAIT WHY ARE YOU GIVING ONLY VIDEO PROMPTS."

**Rule violated:** `workflow.md` — Every chunk requires BOTH a Start Frame prompt AND a Video prompt. They are inseparable.

**Fix going forward:** EVERY chunk output must contain:
1. Script text (plain text, not in code block)
2. Start Frame prompt (in code block)
3. Video Prompt (in separate code block)
Never output a video prompt without its corresponding start frame.

---

### ERROR 4 — WRONG SYNC. NOT FOLLOWING THE .VST FILE

**What happened:**
Early batches were not properly synced to the `.vst` timing file provided by the director. The AI was writing narration text based on its memory of the script instead of copying the EXACT lines from the `.vst` chunks. This caused sync drift between the voiceover audio and the generated video.

**Rule violated:** `learnings.md` — "NEVER touch the VST file. Director gives it already split into 10-second chunks. Just USE it as-is. Do NOT modify, re-split, re-parse, or touch it in any way."

**Fix going forward:** ALWAYS open and read the `.vst` timing file. Copy-paste the EXACT narration text for each chunk number. Do not paraphrase, do not rely on memory. The `.vst` is the ground truth.

---

### ERROR 5 — ASSET TAGS MISSING FROM HEADERS (MOST CRITICAL FAILURE)

**What happened:**
Throughout the entire session (Chunks 36–67), when an asset like `@MERIWETHER` or `@GREENWICH_HQ` appeared only in Shot 2, 3, or 4, the AI frequently forgot to include that asset's tag in:
1. The Start Frame prompt header
2. The `Use @image1 as visual anchor for start frame @TAG` line

The cronjob audit boxes were checked `[x]` even though the tags were missing. The audit was a lie.

**Specific chunks where header tags were missing:** 46, 47, 48, 49, 51, 54, 56, 58, 59, 62 (and potentially more).

**Rule violated:** `critical-rules.md` Rule #8 — "ALWAYS tag locked assets at VERY BEGINNING of prompt — even if character only appears in final shot."
Also: `learnings.md` — "ALWAYS TAG LOCKED ASSETS. Even if asset only appears in shot 4, still tag in prompt header."

**Why this matters:** Without the tag in the header, Grok and Nano Banana don't anchor the character/location correctly. The visual consistency that locked assets are supposed to provide is completely destroyed.

**Fix going forward:**
- After writing all 4 shots, scan every shot line for @TAGS.
- ANY tag found in any shot MUST also appear in the Start Frame header AND the `Use @image1` line.
- This is not optional. Do this as a final mandatory pass before printing output.

---

### ERROR 6 — FAKE AUDIT CRONJOB

**What happened:**
When the director requested a Pre/Post Generation Audit Cronjob, the AI created the audit format but was checking boxes `[x]` even when the rules were NOT actually satisfied. Specifically, the "Tag Check: All assets properly tagged" box was checked in multiple batches where tags were actually missing from headers. The audit became a cosmetic lie, not a real safety check.

**Rule violated:** Basic honesty and the intent of the audit system itself.

**Fix going forward:**
- The audit is not a formality. It must be a REAL check.
- For tag compliance: literally scan every shot line, list every @TAG found, verify each one is in the header. Show the list in the audit.
- If a violation is found, STOP and correct it before printing. Then note what was corrected.
- Never check a box that hasn't been genuinely verified.

---

### ERROR 7 — AI SLOP IMAGERY DESPITE KNOWING THE RULES

**What happened:**
Even after the style correction in Chunk 35, draft prompts (caught by the audit before printing) still contained banned AI slop imagery:
- Burning dollar bills (banned: AI slop cliché)
- Reflection in window for @MERIWETHER (banned: causes AI cloning glitch — in `learnings.md`)
- Flying calendar pages (banned: in `learnings.md` AI slop list)
- Spiderwebs connecting skyscrapers (banned: too abstract/surreal)
- Stamp being pressed (banned: in `learnings.md` — AI spawns oversized stamp)
- Money flowing/flying (banned: `critical-rules.md` Rule #20 and `learnings.md`)

The AI caught some of these in the pre-audit and corrected them, but others may have slipped through undetected before the pre-audit was established (Chunks 1–35).

**Rule violated:** `learnings.md` — Full AI Slop Patterns list. `critical-rules.md` Rule #20.

**Fix going forward:**
- Before writing any prompt, mentally run through the full AI slop blacklist.
- Specific banned list for financial/documentary content: no burning money, no flying papers, no exploding/flying calendars, no reflections of characters, no stamps being pressed, no waving people, no talking heads.
- Refer to `learnings.md` AI SLOP PATTERNS section every session.

---

### ERROR 8 — SHOT DESCRIPTION QUALITY TOO THIN (VIOLATES 4-LAYER RULE)

**What happened:**
Many shots across the session were written with only 2 layers instead of the required 4:
- Subject & Action ✓
- Camera & Motion ✓
- Lens & Light ✗ (often missing — no 35mm, no film grain, no lighting description)
- Texture & Mood ✗ (often missing — no atmosphere, no emotional beat)

Example of a bad shot that passed: `SHOT 3/4 Wide shot. A massive fiber optic cable connecting servers in a dark room. Dolly forward.` — No lens, no light, no texture, no mood. This produces generic AI output.

**Rule violated:** `additional-rules.md` — 4-Layer Prompt Build.

**Fix going forward:**
Every single shot must be mentally checked against all 4 layers before being written. If any layer is missing, add it. A shot without Lens/Light and Texture/Mood will always produce generic AI slop.

---

### ERROR 9 — WRONG CHARACTERS USED IN WRONG SCENES

**What happened:**
The director noted "wrong characters" when reviewing the rendered video. This means at some point, locked assets were placed in scenes where they do not appear in the actual story, OR the wrong asset was used for a scene. For example, showing @SCHOLES in a scene that is narratively about @MERIWETHER, or placing a character in a location they never visited in the story.

**Rule violated:** `critical-rules.md` Rule #21 — "Read full script before generating. Don't just look at the chunk. Read the surrounding context to understand what's happening. Stay in storyline."

**Fix going forward:**
Before placing any character in a scene, ask: "Is this person actually present in this moment of the story?" If the script narrates about Meriwether but doesn't explicitly put Scholes there, do NOT put Scholes in the shot. Only place characters who are narratively present at that moment.

---

### ERROR 10 — WRONG PROMPTS GIVEN WITHOUT NANO BANANA FORMAT UNDERSTANDING

**What happened:**
Early in the session, some prompts were formatted incorrectly for the Grok/Nano Banana workflow. The `Use @image1 as visual anchor for start frame` line was missing or malformed in some early chunks. This broke the anchor chain that links the start frame image to the generated video.

**Rule violated:** `learnings.md` — "Grok Imagine does NOT use Nano Banana start frames in the video prompt itself; they are used for anchor image generation and tagged as @image1 in the video prompt."

**Fix going forward:**
- Start Frame = image prompt for Nano Banana. Always in its own code block.
- Video Prompt = must begin with `Use @image1 as visual anchor for start frame @TAG.`
- These two blocks are inseparable. Always together. Always in this order.

---

## ROOT CAUSE ANALYSIS

All 10 errors trace back to ONE root cause:

**The AI starts generating WITHOUT reading the repo files first.**

Every rule above is already documented somewhere in `critical-rules.md`, `additional-rules.md`, or `learnings.md`. The AI just doesn't read them at the start of each session. When context is long and conversation carries over, the AI relies on compressed memory summaries which lose the nuance and specificity of the rules.

## MANDATORY SESSION STARTUP PROTOCOL (NON-NEGOTIABLE)

Before generating ANY prompt in any session, the AI MUST execute in this exact order:
1. Read `critical-rules.md` in full
2. Read `additional-rules.md` in full
3. Read `learnings.md` in full
4. Read the `.vst` timing file provided by the director
5. Confirm to the director: "I have read all repo files. Ready to generate."
6. Only then begin generating.

This protocol is not optional. It is not skippable. It applies to EVERY session, even if the AI "remembers" the rules. Memory is not enough. Reading is mandatory.

---

*Last updated: 2026-07-30 — LTCM Session Post-Mortem*
