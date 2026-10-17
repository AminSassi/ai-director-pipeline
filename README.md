# AI Director Pipeline

**Pipeline Version:** 2.0.0

Persistent knowledge base and production engine for AI-generated documentary filmmaking (**Verion** & **Insolvent**).

## How to Use

1. Start an AI Director session
2. Say: **"Fully load my AI Director"**
3. Agent reads `AGENTS.md` → loads all 8 core modules → presents the **Mandatory Channel Gate (`1. Verion` / `2. Insolvent`)**
4. Select your channel to begin the pipeline

## Structure

```
ai-director-pipeline/
├── AGENTS.md                        # Bootstrap command, channel gate, rules, workflow
├── SKILL.md                         # Full AI Director skill specification
├── DESIGN.md                        # Repository philosophy & invariants
├── CHANGELOG.md                     # Version history
├── knowledge/
│   ├── critical-rules.md            # Rules #1–#44 from live production
│   ├── additional-rules.md          # 3-plane depth, transitions, and batch gates
│   ├── learnings.md                 # Harmonized production insights
│   ├── session-postmortems.md       # Forensic post-mortems (#001–#004)
│   ├── golden-reference-mladic.md   # Gold standard production benchmark (Mladic)
│   ├── golden-reference-aurora.md   # Gold standard production benchmark (Aurora)
│   ├── suno-prompt-template.md      # Suno documentary score templates
│   └── workflow.md                  # Phase contracts, state guard, invalidation
├── camera/
│   └── angles.md                    # 12 Documentary Framing Archetypes & Anti-Monotony Caps
├── style/
│   └── rules.md                     # Domain color palettes & 4-layer shot persistence
├── prompts/
│   └── quality-checklist.md         # Mandatory 6-Chunk Pre-Generation Audit Matrix
├── routing/
│   ├── README.md                    # Phase 0.75 Intelligent Scene Routing overview
│   ├── classification-rules.md      # 7 Documentary Visual Archetypes
│   ├── model-recommendations.md     # Generator & SHOT 1 archetype mapping
│   └── output-format.md             # Structured YAML routing schema
├── scripts/
│   └── template.md                  # Script template
├── tests/
│   └── regression-tests.md          # Behavioral & anti-slop validation tests
└── output/                          # Generated scripts & shot lists
```

## Pipeline Overview

```
Channel Gate (Verion vs Insolvent) → Raw Script → Expand (1600-1900w) → Insert CTAs → Verify Facts → Compress (1400w) → ElevenLabs → Suno Prompt → [WAIT FOR .vst] → Routing (Phase 0.75) → Asset Scan (Phase 1) → Prompts (Phase 2)
```

### Phase 0 — Script Expansion
Expand raw script to 1,600–1,900 words. Preserve structure, pacing, emotion, accuracy. Never open the hook with a dry calendar date.

### Phase 0.1 — Insert CTAs
Add 3 brand-matched CTAs (after hook, midpoint, outro) for the selected channel (**Verion** or **Insolvent**). No other changes.

### Phase 0.2 — Fact Verification
Verify all facts against source material. No rewriting.

### Phase 0.3 — Compression
Compress to 1,400 ±25 words using the 5-pass deterministic editing algorithm.

### Phase 0.4 — Final VO
Format for ElevenLabs copy-paste and paste directly in chat.

### Phase 0.45 — Suno Music Prompt
Generate Suno music prompt based on episode tone. Max 200 words, ending with `[Instrumental]`.

### Phase 0.5 — Import VST
Director provides `.vst` file pre-split into 10-second / 15-second chunks. Use verbatim as-is. Never touch, reformat, or re-split.

### Phase 0.75 — Intelligent Scene Routing
Classify chunks into the **7 Documentary Visual Archetypes**, enforce the **2-Chunk Location Ceiling (Rule #26)**, and pre-assign **`SHOT 1` Framing Archetypes (`camera/angles.md`)**.

### Phase 1 — Pre-Production
Full asset scan (`@CHARACTER`, `@LOCATION`) and reference sheet generation.

### Phase 2 — Generation (6 Chunks Per Batch)
Print the **Mandatory 6-Chunk Pre-Generation Audit Matrix** → output Start Frame + Grok Video prompts (with 4-layer persistence across `SHOT 1` through `SHOT 4/6`) → print Post-Generation Audit summary.
