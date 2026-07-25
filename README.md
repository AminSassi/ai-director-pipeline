# AI Director Pipeline

**Pipeline Version:** 1.0.0

Persistent knowledge base for AI-generated documentary/film production.

## How to Use

1. Push this folder to GitHub
2. Start a MiMo session
3. Say: **"Fully load my AI Director"** followed by the repo URL
4. Agent reads AGENTS.md → follows bootstrap → loads required modules
5. Confirm loaded modules before starting work

## Structure

```
ai-director-pipeline/
├── AGENTS.md                    # Bootstrap command, rules, workflow
├── DESIGN.md                    # Repository philosophy
├── CHANGELOG.md                 # Version history
├── knowledge/
│   ├── critical-rules.md        # Broken rules from live production
│   ├── additional-rules.md      # Director's production rules
│   ├── learnings.md             # Accumulated corrections (auto-updated)
│   └── workflow.md              # Phase contracts, state guard, invalidation
├── camera/
│   └── angles.md                # Shot types, movements, reference
├── style/
│   └── rules.md                 # Visual style rules
├── prompts/
│   └── quality-checklist.md     # Prompt review checklist
├── routing/
│   ├── README.md                # Why routing exists, how to extend
│   ├── classification-rules.md  # Visual type definitions
│   ├── model-recommendations.md # Generator mapping
│   └── output-format.md         # Structured metadata schema
├── scripts/
│   └── template.md              # Script template
├── tests/
│   └── regression-tests.md      # Behavioral validation tests
└── output/                      # Generated scripts & shot lists
```

## Pipeline Overview

```
Raw Script → Expand (1600-1900w) → Insert CTAs → Verify Facts → Compress (1400w) → ElevenLabs → Suno Prompt → [WAIT FOR .vst] → Chunks → Routing → Prompts
```

### Phase 0 — Script Expansion
Expand raw script to 1,600–1,900 words. Preserve structure, pacing, emotion, accuracy.

### Phase 0.1 — Insert CTAs
Add 3 CTAs: after hook, midpoint, outro. No other changes.

### Phase 0.2 — Fact Verification
Verify all facts against source material. No rewriting.

### Phase 0.3 — Compression
Compress to 1,400 ±25 words. Deterministic editing, not rewriting.

### Phase 0.4 — Final VO
Format for ElevenLabs copy-paste. Ready for narration.

### Phase 0.45 — Suno Music Prompt
Generate Suno music prompt based on episode tone. Max 200 words.

### Phase 0.5 — Import Timing File
Load .vst narration timing. Do not chunk before this.

### Phase 0.6 — Synchronized Chunking
Create chunks from actual timing. Never estimate durations.

### Phase 0.75 — Intelligent Scene Routing
Classify chunks by visual intent. Assign generators.

### Phase 1 — Pre-Production
Asset scan, boards, clip math, scene map, energy map, music prompt.

### Phase 2 — Generation
Start frame → Video prompt → Self-review → Director approval.

## AI-Corrects-AI Pipeline

Every prompt goes through:
1. Generate initial version
2. Self-review against `style/rules.md`, `camera/angles.md`, `prompts/quality-checklist.md`
3. Refine and present final version
4. Director correction → auto-capture to `knowledge/learnings.md`

## Adding Knowledge

Just tell MiMo during any session:
- "Note: wide shots work better for establishing scenes"
- "Remember: Grok needs 'cinematic' in every prompt"
- "Always use Dutch angle for tension scenes"

MiMo writes it to `knowledge/learnings.md` automatically.

## Adding New Routing Rules

1. Edit `routing/classification-rules.md` — add new visual type definitions
2. Edit `routing/model-recommendations.md` — map types to generators
3. Update `routing/README.md` if adding new generator options

The system is modular: new types and generators can be added without rewriting existing logic.

## Compatibility

Validated on:
- MiMo Code (mimo-auto)
- ChatGPT GPT-4+
- Claude 3.5+

Behavior may differ on other models. Prompt behavior isn't identical across all LLMs.
