# Generator Mapping

Visual type determines the generator. Not keywords. Not word count. Not content detection.

---

## Generator Assignment

| Visual Type | Generator | Why |
|-------------|-----------|-----|
| **ACTION** | Seedance 2.0 | Handles fast motion, complex physics, multiple moving subjects |
| **EXPLAINER** | Grok Imagine (Diagram Style) | Animation, diagrams, data visualization, infographic generation |
| **CINEMATIC** | Default (Grok Imagine) | Standard narrative, character moments, establishing shots |
| **MONTAGE** | Default (Grok Imagine) | Time compression works fine with standard generation |
| **ARCHIVAL** | Default (Grok Imagine) | Real footage/photographs, minimal generation needed |
| **EMOTIONAL** | Default (Grok Imagine) | Close-ups, atmosphere, mood — standard cinematic |
| **TRANSITION** | Default (Grok Imagine) | Visual bridges, simple generation |
| **TEXT FOCUS** | Grok Imagine (Diagram Style) | Text overlay, document rendering, headline animation |
| **HYBRID** | Split or Default | Either split chunk or use default with multiple approaches |

---

## Generator Details

### Seedance 2.0
**Best for:** ACTION scenes only

**Use when:**
- Chase sequences
- Explosions, combat
- Fast camera movement (crash zoom, handheld at speed)
- Multiple moving subjects simultaneously
- Destruction, collapse
- Intense physical movement

**Avoid when:**
- Any non-action scene (overkill)
- Data visualization
- Character moments
- Standard narrative

---

### Grok Imagine (Diagram Style)
**Best for:** EXPLAINER and TEXT FOCUS scenes only

**Use when:**
- Diagrams need animation
- Charts and graphs need visualization
- Maps with data overlays
- Corporate structure breakdowns
- Money flow animation
- Timeline visualization
- Document text on screen
- Headlines appearing
- "How this worked" explanations

**Avoid when:**
- Character moments
- Narrative storytelling
- Physical action
- Emotional atmosphere

---

### Default Cinematic (Grok Imagine / Kling)
**Best for:** Everything else

**Use when:**
- Character moments
- Establishing shots
- Emotional beats
- Narrative dialogue
- Time passage (montage)
- Archival footage integration
- Scene transitions
- Mood and atmosphere

**Grok Imagine is the exclusive video generator for cinematic scenes.**
---

## Decision Tree

```
What is the best visual to tell this part of the story?
│
├── Diagram/chart/map/animation needed?
│   └── YES → EXPLAINER or TEXT FOCUS → Grok Imagine (Diagram Style)
│
├── High physical action/chase/explosion?
│   └── YES → ACTION → Seedance 2.0
│
├── Multiple visual types needed?
│   └── YES → HYBRID → Split or Default
│
└── Otherwise → CINEMATIC/MONTAGE/ARCHIVAL/EMOTIONAL/TRANSITION → Default
```

---

## Chunk Splitting

When a chunk requires HYBRID treatment:

1. Identify the split point in narration
2. Route each segment to its optimal generator
3. Ensure visual continuity across split (same tags, lighting, color)
4. Mark as HYBRID in metadata

**Example:**
```
Original: "Apple acquired Beats for $3 billion. Steve Jobs had built the foundation."
Split:
  - Segment A: "Apple acquired Beats for $3 billion" → EXPLAINER → grok
  - Segment B: "Steve Jobs had built the foundation" → CINEMATIC → Default
```

