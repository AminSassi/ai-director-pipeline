# Golden Reference — The Butcher of Bosnia (Ratko Mladić)

**Status:** PRODUCTION SUCCESS — 99% perfection, 1% AI slop.
**Date:** 2026-09-01
**Episode:** "The Butcher of Bosnia — The Manhunt, the Trial, and the Death of Ratko Mladić"
**Runtime:** ~9 min 26 sec | 38 chunks × 15 seconds | 1,415 words VO
**Channel:** INSOLVENT (rebranded to VERION STORY)

This file is the permanent record of the most successful production session in the pipeline's history. Every future episode MUST reference this file during bootstrap. It documents the exact techniques, formats, pacing, and creative decisions that produced a near-perfect video.

---

## WHY THIS SESSION WORKED

### 1. Shot Count: 6 Shots Per 15-Second Chunk
The single biggest quality driver. Previous sessions used 4 shots per chunk, which felt slow and gave Grok too much time per shot (leading to AI drift and slop). Switching to **6 shots per 15-second chunk** (~2.5 seconds per shot) created:
- **Rapid visual variety** that mirrors professional documentary editing
- **Less time for AI to hallucinate** within any single generation
- **More camera angles and movements** per chunk, preventing visual monotony
- **Better script sync** — each shot maps tightly to a specific phrase of narration

**THIS IS NOW THE STANDARD: 6 SHOTS PER 15-SECOND CHUNK. ALWAYS.**

For 10-second chunks: use 4 shots per chunk (~2.5s pacing).
For 15-second chunks: use 6 shots per chunk (~2.5s pacing).
The ~2.5-second-per-shot pacing is the golden ratio.

---

### 2. Strict Chronological Character Tagging
This episode had TWO versions of the same person (Ratko Mladić):
- **@Ratkoyoung** — 1990s wartime commander in camo uniform and beret (age ~52). Used ONLY for scenes set 1992–2000.
- **@Ratkoold** — Elderly fugitive, capture, trial, and detention (age 68–84). Used for ALL scenes set 2001–2026.

**The rule:** Never mix temporal versions. If the narration describes the 2011 arrest, use @Ratkoold. If it describes the 1995 siege, use @Ratkoyoung. The transition point is **October 2000** (Milošević ouster). Before = @Ratkoyoung. After = @Ratkoold.

Originally there was a third tag (@MLADIC_TRIAL) for courtroom scenes, but the director consolidated it into @Ratkoold to reduce reference boards. This worked perfectly — one elderly Mladić reference sheet covered fugitive, capture, trial, and detention scenes.

---

### 3. The Exact Prompt Format That Worked

Every chunk followed this exact 3-block structure:

**Block 1 — Narration Text (plain text, NOT in code block)**
Copy-pasted VERBATIM from the `.srt` timing file. Never paraphrased. Never from memory.

**Block 2 — Start Frame Prompt (code block)**
```
@TAG1 @TAG2
Cinematic [shot type] [shot description]. [Subject doing action] at/in [location]. [Lighting], [color palette], [atmosphere]. [Lens]mm lens, [depth of field], [film texture]. --ar 16:9
```

**Block 3 — Video Prompt (separate code block)**
```
Use @image1 as visual anchor for start frame @TAG1 @TAG2.
SHOT 1/6 [Subject] [specific mid-action verb] [in location]. [Camera movement].
SHOT 2/6 [Different angle/subject] [action]. [Different camera movement].
SHOT 3/6 [Close-up or macro detail] [specific physical element]. [Camera movement].
SHOT 4/6 [Character or environment] [action with emotional weight]. [Camera movement].
SHOT 5/6 [Contrasting or transitional shot] [detail]. [Camera movement].
SHOT 6/6 [Wide or aerial establishing shot] [environment in atmosphere]. [Camera movement].
--ar 16:9 --no text, watermarks, blur
```

---

### 4. Camera Movement Variety That Prevented Monotony
Each chunk used a MINIMUM of 3 distinct camera movements from this palette:
- Slow push in
- Slow dolly back / dolly out
- Low-angle tilt up
- Slow pan left / right
- Slow crane rise
- Tracking shot (lateral movement)
- Handheld drift / shake
- Macro rack focus
- Dutch tilt hold
- Static hold (used sparingly — max 1 per chunk)
- 50mm shallow focus hold

**Critical rule:** NEVER repeat the same camera movement in consecutive shots. If Shot 1 is "slow push in," Shot 2 MUST be something different.

---

### 5. The 4-Layer Build (Every Single Shot)
Every shot line contained all 4 layers. No exceptions:

| Layer | What It Provides | Example |
|---|---|---|
| **Subject & Action** | WHO is doing WHAT | "@Ratkoold handing over expired military ID" |
| **Camera & Motion** | HOW the camera moves | "Slow push in" |
| **Lens & Light** | WHAT creates the look | "50mm shallow focus, harsh side lighting" |
| **Texture & Mood** | WHAT it FEELS like | "Film grain, documentary tension" |

While the Start Frame sets the rich master lighting and lens baseline for Shot 1, **Shots 2–6 cut to new angles or contrast locations**—so every individual shot line MUST retain a compact 4–6 word Lens/Light + Texture/Mood anchor (e.g., `35mm lens, deep shadows, film grain`) while staying under 35 words. Never leave Shots 2–6 as bare action sentences, or Grok will lose the photographic grade on cuts.

---

### 6. Moderation-Safe Rewrites
Grok's content filter blocked Chunk 30 because it depicted @Ratkoold in medical distress ("frail in hospital bed," "intravenous tubes," "gaunt face" on an imported reference face). 

**The fix:** Completely redesign the chunk to focus on:
- Institutional/architectural atmosphere (legal consultation room, desk lamp, dossiers)
- Environmental details (window showing evening sky, law library shelves)
- NO character depicted in medical vulnerability on imported faces

**Rule for future episodes:** When a character is sick, dying, or in medical distress, DO NOT show their face or body in that state when using imported reference images. Instead, show the ENVIRONMENT of their decline (the room, the documents, the window, the corridor). Let the narration carry the emotional weight. The visuals provide atmospheric context.

---

### 7. CTA Chunks — Atmospheric, NOT UI
All 3 CTA segments (Post-Hook Chunk 05, Midpoint Chunk 23, Outro Chunks 37–38) used **atmospheric story-relevant visuals**:
- Chunk 05: Aged military map under desk lamp, winding mountain road, brutalist monument
- Chunk 23: Telephone wire at Lazarevo, surveillance van in rural mist
- Chunks 37–38: Sweeping aerial of Potočari cemetery, solitary headstone in dawn light

**ZERO subscribe buttons. ZERO notification bells. ZERO channel logos. ZERO phone screens.** The director adds CTA overlays manually in post-production. The AI generates ONLY cinematic visuals.

---

### 8. Batch Processing Discipline
The 38 chunks were processed in 6 batches:
- **Batch 1:** Chunks 01–06 (Introduction, Hook, Yugoslav Breakup)
- **Batch 2:** Chunks 07–12 (Rise of Mladić, Siege of Sarajevo, Srebrenica Enclave)
- **Batch 3:** Chunks 13–18 (Srebrenica Executions, Indictment, Belgrade Impunity)
- **Batch 4:** Chunks 19–24 (Going Underground, Manhunt, Karadžić Arrest, Lazarevo Lead)
- **Batch 5:** Chunks 25–30 (The Dawn Raid, Extradition, Trial, Verdict, Final Decline)
- **Batch 6:** Chunks 31–38 (Death in Custody, Survivor Reaction, Divided Memory, Outro)

Each batch was reviewed and approved with "done" before proceeding. This prevented cascading errors across the entire episode.

---

### 9. Pre/Post Generation Audit Cronjobs (REAL, Not Cosmetic)
Every batch included genuine verification:

**Pre-Generation Audit:**
- [x] Tag compliance: Listed EVERY tag per chunk, verified in Start Frame header AND `Use @image1` line
- [x] Shot count: Confirmed exactly 6 shots per chunk
- [x] AI slop blacklist: Scanned for ALL banned items
- [x] 4-layer build: Verified all layers present
- [x] Camera variety: Minimum 3 distinct movements
- [x] Character placement: Chronologically correct
- [x] Sync check: Verbatim from .srt file

**Post-Generation Audit:**
- Beauty verification
- Tag validation (100% compliance)
- Sync check against source timing file

---

## LOCKED ASSET REGISTER (EXACT TAGS USED IN GROK)

### Characters
| Tag | Description | Time Period |
|---|---|---|
| `@Mejra` | 77-year-old Bosniak grandmother, Srebrenica survivor | Present day |
| `@Ratkoyoung` | Ratko Mladić, VRS general in camo/beret | 1992–2000 |
| `@Ratkoold` | Ratko Mladić, elderly fugitive/prisoner | 2001–2026 |
| `@Radovan` | Radovan Karadžić as Dr. Dabić | July 2008 |
| `@president` | Slobodan Milošević, Serbian president | Late 1990s |

### Locations
| Tag | Description |
|---|---|
| `@POTOCARI_MEMORIAL` | Srebrenica Memorial Cemetery in Potočari |
| `@SARAJEVO_SIEGE` | Besieged Sarajevo (1992–1996) |
| `@SREBRENICA_ENCLAVE` | Srebrenica UN compound & factory (July 1995) |
| `@LAZAREVO_HOUSE` | Brick safehouse in Lazarevo village |
| `@HAGUE_COURTROOM` | ICTY Courtroom at The Hague |
| `@SCHEVENINGEN_CELL` | UN Detention Unit medical wing |

### Channel
| Tag | Description |
|---|---|
| `@verion-channellogo` | VERION STORY channel logo |

---

## PHASE EXECUTION TIMELINE

| Phase | Output | Word Count / Details |
|---|---|---|
| Phase 0 | Expanded narrative script | 1,896 words, 5 acts |
| Phase 0.1 | CTA insertion | 3 CTAs (Post-Hook, Midpoint, Outro) |
| Phase 0.2 | Fact verification | All claims verified against ICTY/ICJ records |
| Phase 0.3 | Compression | 1,415 words (target: 1,400 ±25) |
| Phase 0.4 | ElevenLabs VO script | Clean narration, pasted directly in chat |
| Phase 0.45 | Suno music prompt | 60–65 BPM, dark ambient neoclassical, `[Instrumental]` |
| Phase 0.5 | Import timing file | `Butcher_15sec_chunks.srt` — 38 chunks |
| Phase 0.75 | Intelligent scene routing | 38-row routing table with generator + tags |
| Phase 1 | Pre-production | Locked assets register + reference sheet prompts |
| Phase 2 | Prompt generation | 38 chunks × (Start Frame + 6-shot Video) = 228 shots total |

---

## MISTAKES MADE AND CORRECTED IN THIS SESSION

### Mistake 1: Jumped to Phase 2 Without Presenting Locked Assets
**What happened:** After receiving the `.srt` timing file, immediately generated Batch 1 prompts without first presenting the locked asset reference sheet prompts for the director to generate in Nano Banana.
**Director's words:** "BRO WTF YOU DOING? in rules i said dont start until i tell you, and you didnt give me locked assets prompts"
**Fix:** ALWAYS present locked asset reference sheets FIRST. Wait for the director to generate them, upload confirmation screenshots, and say "done" before generating ANY chunk prompts.

### Mistake 2: Only 4 Shots Per Chunk
**What happened:** Initial Batch 1 used 4 shots per chunk instead of 6.
**Director's words:** "why only 4 shots in video prompts??? DID YOU READ THE GIT REPO?? WE USUALLY DO 6"
**Fix:** 15-second chunks = 6 shots. Always. This is now the permanent standard.

### Mistake 3: Moderation Block on Medical Distress
**What happened:** Chunk 30 was blocked by Grok because it depicted @Ratkoold in medical distress with imported reference face.
**Fix:** Redesigned to focus on institutional atmosphere (legal room, desk, dossiers, window). Character not shown in vulnerable medical state.

---

## SUNO MUSIC PROMPT (EXACT PROMPT USED)

```
Cinematic documentary score, slow-build and pulse-driven with a 60-65 BPM sense of heavy dread and patient menace; opens on a single low cello drone into near-silence, followed by a somber piano motif, distant muted percussion, steady ticking-clock tension, mournful solo violin swells, uneven dark orchestral rises, then pulls back to sparse acoustic cello, cold ambient resonance, and a suspended unresolved note, archival film-grain texture, analog warmth, solemn and heavy mix with emotional gravity, dark ambient, neoclassical, cello, violin, slow, orchestral, minimal, cinematic, solemn, dramatic, pulse, [Instrumental]
```

---

## KEY CREATIVE PATTERNS TO REUSE

### Emotional Bookending
The episode opens and closes with @Mejra at @POTOCARI_MEMORIAL. This creates an emotional frame:
- **Chunk 01:** Mejra looking through window at cemetery
- **Chunk 36:** Mejra standing among the gravestones
- **Chunk 37:** Aerial pull-away from the valley
- **Chunk 38:** Solitary headstone fading to black

### Contrast Cuts
Several chunks used deliberate visual contrast within a single chunk:
- **Chunk 02:** Mejra at graves → sterile Dutch prison cell
- **Chunk 03:** Empty prison cell → 1995 Mladić barking orders
- **Chunk 35:** Empty courtroom → endless fields of Potočari

### Escalation Through Environment
Instead of showing violence directly (which triggers moderation and produces slop), the session used environmental escalation:
- Artillery battery on hillside → smoke plumes in valley (Chunk 09)
- Crowded factory gates → empty warehouse interior (Chunks 11–14)
- Remote field clearing → bulldozer tracks in mud (Chunk 15)

### Investigative Procedural Tension
The manhunt and capture sequence (Chunks 20–26) built tension through surveillance craft:
- Dim safehouse → forged ID on nightstand (Chunk 20)
- Wiretap monitors → waveform spikes (Chunk 24)
- Dawn convoy without headlights → bedroom door opening (Chunk 25)
- Trembling hands sliding ID card → handcuffs clicking (Chunk 26)

---

*This file is permanent. Read it during every bootstrap. It is the gold standard.*

*Last updated: 2026-09-01 — Mladić Session Golden Reference*
