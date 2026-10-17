# Regression Tests

These tests validate agent behavior across both pipeline execution and creative anti-slop rules. Run after any prompt or rule change.

---

## Test 1: "Paste script"

**User:**
Paste the script.

**Expected:**
- Agent reads existing artifact (`phase-0.4-elevenlabs.md`)
- Pastes contents
- Pipeline state unchanged

**Forbidden:**
- Regenerates script
- Rewrites content
- Reopens any phase

---

## Test 2: "Rewrite the intro"

**User:**
Rewrite the intro.

**Expected:**
- Agent detects this modifies a completed artifact
- Responds: `"This reopens Phase [X]. Confirm you want to regenerate Phase [X] and invalidate downstream artifacts."`
- Waits for confirmation

**Forbidden:**
- Silently regenerates
- Continues without confirmation
- Invalidates downstream silently

---

## Test 3: "Continue"

**User:**
Continue.

**Expected:**
- Agent checks current phase
- Continues current phase if in progress
- If phase is complete, asks for next input (e.g., `.vst` file)

**Forbidden:**
- Restarts workflow from beginning
- Skips to a later phase
- Makes assumptions about what "continue" means

---

## Test 4: "Paste script" after new script provided

**User:**
[Provides new raw script]

**Expected:**
- Agent recognizes new input
- Starts Phase 0 with new script (after Mandatory Channel Gate is satisfied)
- Does not use old artifact

**Forbidden:**
- Mixes old and new scripts
- Skips Phase 0
- Assumes old artifact is still valid

---

## Test 5: "Fully load my AI Director"

**User:**
Fully load my AI Director

**Expected:**
- Agent reads all 8 core modules in `AGENTS.md`
- Responds with confirmation and the **Mandatory Channel Gate**:
```
AI Director loaded.

Core modules:
✓ critical-rules
✓ additional-rules
✓ learnings
✓ session-postmortems
✓ camera
✓ style
✓ quality-checklist
✓ golden-references

Status: Ready.

🔴 MANDATORY CHANNEL GATE:
Which channel are we producing for today?
1. Verion
2. Insolvent

(Awaiting your selection before proceeding to script processing or any pipeline phase)
```

**Forbidden:**
- Skips files
- Defaults to Insolvent or Verion without asking
- Proceeds to Phase 0 before channel selection

---

## Test 6: "How many words?"

**User:**
How many words?

**Expected:**
- Agent reads current artifact
- Reports word count
- Pipeline state unchanged

**Forbidden:**
- Reopens any phase
- Regenerates content
- Modifies artifact

---

## Test 7: "Change the CTA"

**User:**
Change the CTA to say "subscribe now".

**Expected:**
- Agent detects this modifies Phase 0.1
- Warns: `"This reopens Phase 0.1. Confirm you want to regenerate Phase 0.1 and invalidate Phases 0.2–0.45."`
- Waits for confirmation

**Forbidden:**
- Silently edits
- Only updates Phase 0.1 without invalidating downstream
- Continues using stale downstream artifacts

---

## Test 8: "Generate shot list" without routing

**User:**
Generate shot list.

**Expected:**
- Agent checks if routing is complete
- If not: `"Routing not complete. Need Phase 0.5 (.vst timing chunks) and Phase 0.75 (routing) first."`
- Does not proceed

**Forbidden:**
- Generates shots without routing
- Skips phases
- Makes up chunk data

---

## Test 9: Batch Camera Variety & Anti-Slop Gate (Phase 2)

**User:**
Generate Chunks 1–6.

**Expected:**
- Agent prints the **Mandatory 6-Chunk Pre-Generation Audit Matrix** table BEFORE printing the prompts.
- Across Chunks 1–6:
  - `"slow push in"` appears in `SHOT 1` **at most ONCE (max 1/6 chunks)**.
  - **Zero consecutive chunks** open with `Cinematic medium shot`.
  - **No interior room or `@LOCATION`** is used for more than **2 consecutive chunks** (Rule #26).
  - **Every single shot (`SHOT 1` through `SHOT 4/6`)** includes a compact 4–6 word Lens/Light + Texture/Mood token (`24mm`/`35mm`/`50mm` lens, chiaroscuro lighting, `film grain`) and stays within **18–34 words** (Rule #14).
  - **Start Frame** tags ONLY assets visible in `Shot 1, Frame 0`, while **Video Header (`Use @image1...`)** tags ALL locked assets appearing in any shot of the chunk (Rule #8 & #12).
  - **Zero fine hand mechanics** (no pens writing, no highlighters streaking, no stamps pressing, no fingers typing) and **zero multi-person physical contact** (Rules #39 & #40).

**Forbidden:**
- Opening 2+ chunks in a batch with `SHOT 1 slow push in`
- Dropping lens or `film grain` tokens in `SHOT 2`, `SHOT 3`, or `SHOT 4`
- Staying in the same room for 3+ consecutive chunks
- Using `--no people, faces` on human drama chunks instead of silhouettes/OTS framing (Rule #44)

---

## Test 10: Conflicting instruction

**User:**
Skip chunking, just route the full script.

**Expected:**
- Agent detects this violates pipeline rules
- Responds: `"Routing requires synchronized chunks from Phase 0.5 (.vst timing file). Cannot route full script. Please provide the .vst timing file first."`
- Does not proceed

**Forbidden:**
- Complies with invalid request
- Routes full script
- Skips mandatory phases
