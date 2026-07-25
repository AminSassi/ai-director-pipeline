# Production Workflow

Locked order. No exceptions.

---

## CRITICAL RULES — NEVER VIOLATE

### Rule 1: Never Chunk Until Timing Exists
Script must NOT be chunked immediately after expansion.
Chunk boundaries are determined by narration timing from .vst file.
If timing file is required, pipeline MUST stop and wait.

### Rule 2: Never Guess Timing
Do not estimate chunk durations.
Do not invent 10-second chunks.
Do not split by paragraph or sentence count.
Wait for the narration timing file.

### Rule 3: Timing Is Source of Truth
Once .vst timing file is available:
- Align every narration sentence with timestamps
- Create chunks from actual narration timing
- Preserve synchronization exactly
- Never rewrite chunk boundaries afterward

### Rule 4: Routing Happens After Chunking
Routing analyzes synchronized chunks only, not full script.
Never perform routing before chunking.

### Rule 5: Prompt Generation Is Final Stage
Prompt generation is forbidden until:
- ✓ Script expanded
- ✓ Narration approved
- ✓ Timing file loaded
- ✓ Synchronized chunks created
- ✓ Routing completed

### Rule 6: Hard Stop Policy
If any required input is missing, stop immediately.
Do not continue automatically.
Do not make assumptions.
Do not fabricate intermediate outputs.

### Rule 7: Human Approval Gates
Pipeline requires explicit approval before next phase.

### Rule 8: AI Is Executor, Not Decision Maker
AI must never assume user wants to continue.
If next required asset not provided, pause and ask for it.
Never "helpfully" continue by estimating or inventing data.

### Rule 9: Workflow Integrity
Agents NEVER restart an earlier phase unless explicitly instructed.

User requests such as:
- "paste it"
- "show me"
- "explain"
- "count words"
- "summarize"
- "review"

DO NOT reopen previous phases. Use the existing artifact.

Only these commands reopen a phase:
- "rewrite"
- "regenerate"
- "redo"
- "start over"
- "change"
- "edit"

### Rule 10: Compression Is Editing, Not Writing
Compression performs deterministic edits on existing text.
Never regenerate. Never rewrite. Never invent sentences.

---

## State Guard

Before doing anything, check the current state.

```
Current Phase: [X]

User Request: "[request]"

State Check:
✓ Request can be satisfied from existing artifact
✗ Request requires phase transition

Action:
[read artifact / require confirmation]
```

If the request would require reopening a phase:

```
Response: "This reopens Phase [X]. Confirm you want to regenerate 
Phase [X] and invalidate downstream artifacts."
```

---

## Artifact Invalidation

Changing a phase invalidates every downstream phase.

```
Edit Phase 0     → Delete validity of 0.1–0.45
Edit Phase 0.1   → Delete validity of 0.2–0.45
Edit Phase 0.2   → Delete validity of 0.3–0.45
Edit Phase 0.3   → Delete validity of 0.4–0.45
Edit Phase 0.4   → Delete validity of 0.45
```

The agent must never silently continue using stale artifacts.

---

## Artifact Metadata

Each artifact stores metadata alongside content.

```yaml
artifact: phase-0.4-elevenlabs.md
status: approved | draft | stale
version: 1.0
word_count: 1416
ctas: 3
source: phase-0.3-compressed.md
created_by: pipeline
downstream_valid: true
```

Downstream phases check `downstream_valid` before operating.

---

## Immutable Artifacts

Each phase produces a file. No phase recreates earlier artifacts.

```
phase-0-script.md           → Raw expanded script (1600-1900 words)
phase-0.1-script-with-ctas.md → CTAs inserted, nothing else changed
phase-0.2-verified.md       → Facts verified, no rewriting
phase-0.3-compressed.md     → Compressed to 1400 ±25 words
phase-0.4-elevenlabs.md     → Final VO ready for copy-paste
```

Each phase reads the previous artifact and writes a new one.
No phase is allowed to recreate an earlier artifact from memory.

---

## Phase Contracts

### Phase 0 — Script Expansion

**Input:** Raw script from user
**Output:** phase-0-script.md
**Allowed:**
- Expand sentences for narration flow
- Add natural transitions
- Preserve all facts and dates
**Forbidden:**
- Delete factual events
- Change the story structure
- Add CTAs
- Modify existing facts
**Exit condition:** 1600-1900 word script produced

---

### Phase 0.1 — Insert CTAs

**Input:** phase-0-script.md
**Output:** phase-0.1-script-with-ctas.md
**Allowed:**
- Insert 3 CTAs at designated positions
- Fix punctuation around CTAs
**Forbidden:**
- Rewrite paragraphs
- Add new facts
- Remove facts
- Change structure
- Modify any existing text
**Exit condition:** 3 CTAs inserted, no other changes

---

### Phase 0.2 — Fact Verification

**Input:** phase-0.1-script-with-ctas.md
**Output:** phase-0.2-verified.md
**Allowed:**
- Verify facts against source material
- Mark verified facts
**Forbidden:**
- Rewrite paragraphs
- Add new facts
- Remove facts
- Change structure
- Modify any text
**Exit condition:** All facts verified against sources

---

### Phase 0.3 — Compression

**Input:** phase-0.2-verified.md
**Output:** phase-0.3-compressed.md
**Allowed:**
- Remove repetition
- Remove adjectives
- Merge paragraphs
- Delete filler words
- Shorten quotes
- Delete low-impact context
**Forbidden:**
- Rewrite sections
- Reorder story
- Delete factual events
- Add new sentences
- Modify hook, timeline, numbers, dates, CTAs
**Exit condition:** 1400 ±25 words reached

**Compression Order:**
Pass 1 — Delete filler ("actually", "simply", "widely known", "roughly", "the kind of", repeated explanations)
Pass 2 — Merge consecutive sentences
Pass 3 — Remove secondary details
Pass 4 — Shorten quotes
Pass 5 — Delete low-impact context

---

### Phase 0.4 — Final VO

**Input:** phase-0.3-compressed.md
**Output:** phase-0.4-elevenlabs.md
**Allowed:**
- Fix formatting
- Normalize punctuation
- Preserve wording
- Preserve CTAs
**Forbidden:**
- Rewrite paragraphs
- Add new facts
- Remove facts
- Change structure
- Reopen previous phases
**Exit condition:** ElevenLabs-ready script produced

---

### Phase 0.45 — Suno Music Prompt

**Input:** phase-0.4-elevenlabs.md
**Output:** phase-0.45-suno.md
**Allowed:**
- Generate Suno music prompt based on episode tone
- Use `knowledge/suno-prompt-template.md` as reference
- Match energy arc to episode structure
**Forbidden:**
- Exceed 200 words in prompt
- Skip this phase
- Modify ElevenLabs script
**Exit condition:** Suno music prompt produced

---

### Phase 0.5 — Import VST

**Input:** .vst file from director (already split into 10-second chunks)
**Output:** None — use VST as-is
**Allowed:**
- Read VST chunks
- Reference chunk timestamps
**Forbidden:**
- Touch, reformat, or re-split the VST
- Create a separate chunks file
- Estimate durations
- Guess timing
**Exit condition:** VST received, chunks available as-is

---

### Phase 0.75 — Intelligent Scene Routing

**Input:** phase-0.6-chunks.md
**Output:** phase-0.75-routing.md
**Allowed:**
- Classify visual intent per chunk
- Assign generator
- Generate metadata
**Forbidden:**
- Route before chunking
- Estimate timing
- Modify chunks
**Exit condition:** All chunks routed with metadata

---

## Compression Algorithm

**Rules:**
- Remove repetition
- Remove adjectives
- Merge paragraphs
- Never invent sentences
- Never rewrite sections
- Never reorder story
- Never delete factual events
- Delete least important material first
- Stop immediately once target reached

**Compression Order:**

Pass 1 — Delete filler words:
- "actually", "simply", "widely known", "roughly", "the kind of"
- Repeated explanations

Pass 2 — Merge consecutive sentences

Pass 3 — Remove secondary details

Pass 4 — Shorten quotes

Pass 5 — Delete low-impact context

**NEVER TOUCH:**
- Hook
- Timeline
- Main facts
- Numbers
- Dates
- CTAs

---

## Phase 1 — Pre-Production
1. Full asset scan (every recurring asset, named AND anonymous)
2. Build ALL boards upfront in one block
3. Scene map
4. Energy map

## Phase 2 — Generation
1. START FRAME → Flow Nano Banana 2 ONLY
2. GROK VIDEO → Grok Imagine — always 10 seconds
3. KLING VIDEO → Kling VIDEO 3.0 — always 15 seconds

## AI-Corrects-AI
Every prompt goes through self-review before presenting.

## Director's Timeline Workflow
- Director watches Premiere Pro timeline in real time
- Passes timing, then gives that chunk of script
- MiMo generates for that specific segment
- Director controls the pace

## Platform Differences
| Rule | Grok | Kling |
|---|---|---|
| Negatives | --no flags at end | Separate Negative Prompt field |
| Duration | 10s always | 15s always |
| Multi-shot | Automatic | Multi-Shot ON + Custom ON |
| Aspect ratio | --ar 16:9 in prompt | Set in UI only |
| Start frames | Not used | Nano Banana 2 only |

---

## Example Flows

### Flow 1: User asks "paste the script"

```
Current Phase: 0.5
User Request: "paste the script"

State Check:
✓ Request can be satisfied from phase-0.4-elevenlabs.md
✓ No phase transition required

Action:
Read artifact.
Paste contents.
Pipeline state unchanged.
```

### Flow 2: User asks "rewrite the intro"

```
Current Phase: 0.5
User Request: "rewrite the intro"

State Check:
✗ Request modifies a completed artifact

Response:
"This reopens Phase 0.4. Confirm you want to regenerate 
Phase 0.4 and invalidate downstream artifacts."
```

### Flow 3: User provides .vst file

```
Current Phase: 0.4
User Request: [provides .vst file]

State Check:
✓ Request advances pipeline to Phase 0.5
✓ Required input provided

Action:
Load timing data.
Create phase-0.5-timing.md.
Transition to Phase 0.5.
```
