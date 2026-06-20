# Production Workflow

Locked order. No exceptions.

## Phase 1 — Pre-Production (before any generation)
1. Receive script
2. Full asset scan (every recurring asset, named AND anonymous)
3. Build ALL boards upfront in one block
4. Clip math
5. Scene map
6. Energy map
7. Suno music prompt

## Phase 2 — Generation (per scene, locked order)
1. START FRAME → Flow Nano Banana 2 ONLY (never Grok, never Kling)
2. GROK VIDEO → Grok Imagine — always 10 seconds
3. KLING VIDEO → Kling VIDEO 3.0 — always 15 seconds

## AI-Corrects-AI (Built Into One Session)
Every prompt I generate goes through self-review before presenting:
1. Generate start frame + video prompt
2. Check against critical-rules.md (6 broken rules)
3. Check against quality-checklist.md
4. Check shot count matches word count
5. Check camera angle variety (no repeats, minimum 30° rotation)
6. Check character is mid-action, not posed
7. Check VO-to-visual mapping (every word represented)
8. Fix anything wrong, then present final version

No second session needed. Director can always override or correct, and corrections get saved to knowledge/learnings.md.

## Director's Timeline Workflow
- Director watches Premiere Pro timeline in real time
- Passes 10 seconds on the timeline, then gives that 10-second chunk of script
- MiMo generates for that specific 10-second segment:
  - 1x START FRAME image prompt (Nano Banana 2)
  - 1x VIDEO prompt (Grok, 10 seconds)
- Keeps shots coherent with script AND synced to timeline
- Do NOT wait for "DONE" or give 2 prompts at a time
- Director controls the pace — gives script chunk when ready

## Clip Math
- Grok clip = 10 seconds generated
- Kling clip = 15 seconds generated
- Average cut in Premiere = 5–7 seconds
- Formula: Script length (seconds) ÷ Average cut length = Clips needed

## VO-to-Visual Mapping
Map every VO sentence to a specific visual beat BEFORE writing any shot.
- No shot exists unless it directly illustrates a specific VO sentence
- Generic b-roll = failure
- Objects when VO names a person = failure

## Platform Differences
| Rule | Grok | Kling |
|---|---|---|
| Negatives | --no flags at end | Separate Negative Prompt field |
| Duration | 10s always | 15s always |
| Multi-shot | Automatic | Multi-Shot ON + Custom Multi-Shot ON |
| Aspect ratio | --ar 16:9 in prompt | Set in UI only |
| Start frames | Not used | Not used — Nano Banana 2 only |
