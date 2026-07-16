# Regression Tests

These tests validate agent behavior. Run after any prompt change.

---

## Test 1: "Paste script"

**User:**
Paste the script.

**Expected:**
- Agent reads existing artifact (phase-0.4-elevenlabs.md)
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
- Responds: "This reopens Phase [X]. Confirm you want to regenerate Phase [X] and invalidate downstream artifacts."
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
- If phase is complete, asks for next input (e.g., .vst file)

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
- Starts Phase 0 with new script
- Does not use old artifact

**Forbidden:**
- Mixes old and new scripts
- Skips Phase 0
- Assumes old artifact is still valid

---

## Test 5: "Fully load my AI Director"

**User:**
Fully load my AI Director
https://github.com/AminSassi/ai-director-pipeline

**Expected:**
- Agent reads all 6 core files
- Responds with confirmation:
```
AI Director loaded.

Core modules:
✓ critical-rules
✓ additional-rules
✓ learnings
✓ camera
✓ style
✓ quality-checklist

Status: Ready.

What are we working on today?
```

**Forbidden:**
- Skips files
- Summarizes instead of reading
- Continues without confirmation

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
- Warns: "This reopens Phase 0.1. Confirm you want to regenerate Phase 0.1 and invalidate Phases 0.2–0.4."
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
- If not: "Routing not complete. Need Phase 0.6 (chunks) and Phase 0.75 (routing) first."
- Does not proceed

**Forbidden:**
- Generates shots without routing
- Skips phases
- Makes up chunk data

---

## Test 9: "What phase are we on?"

**User:**
What phase are we on?

**Expected:**
- Agent reports current phase
- Lists completed phases
- Lists what's needed next

**Forbidden:**
- Guesses
- Makes assumptions
- Reports wrong phase

---

## Test 10: Conflicting instruction

**User:**
Skip chunking, just route the full script.

**Expected:**
- Agent detects this violates pipeline rules
- Responds: "Routing requires synchronized chunks from Phase 0.6. Cannot route full script. Please provide .vst timing file first."
- Does not proceed

**Forbidden:**
- Complies with invalid request
- Routes full script
- Skips mandatory phases
