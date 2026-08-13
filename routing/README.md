# Intelligent Scene Routing — Visual Intent System

Routes each narration chunk to the optimal AI generator based on visual intent, not keywords.

---

## Core Principle

The router asks one question:

**"What kind of visual is required to tell this part of the story in the best possible way?"**

It does NOT ask:
- "What words appear in the narration?"
- "Is there a number in this sentence?"
- "Does this contain 'statistics' or 'running'?"

---

## Visual Types

| Type | Description | Generator |
|------|-------------|-----------|
| CINEMATIC | Character moments, narrative, establishing shots | Default |
| ACTION | Chase, explosion, fast physical motion | Seedance 2.0 |
| EXPLAINER | Diagrams, charts, maps, data visualization | Grok Imagine (Diagram Style) |
| MONTAGE | Time passing, growth sequences | Default |
| ARCHIVAL | Real footage, photographs, documents | Default |
| EMOTIONAL | Close-ups, atmosphere, mood | Default |
| TRANSITION | Scene connections, time jumps | Default |
| TEXT FOCUS | Headlines, documents, on-screen text | Grok Imagine (Diagram Style) |
| HYBRID | Multiple approaches needed | Split or Default |

---

## Why Visual Intent, Not Keywords

### Bad routing (keyword-based):
```
Narration: "born in 1942 in Udupi"
Keyword detected: date → EXPLAINER
Result: Grok Imagine (Diagram Style) ← WRONG
```

This is a biography. It's cinematic storytelling.

### Good routing (visual intent):
```
Narration: "born in 1942 in Udupi"
Question: What visual tells this story best?
Answer: Character arriving in new city, establishing shot
Visual type: CINEMATIC
Generator: Default ← CORRECT
```

---

## Generator Assignment

| Visual Type | Generator | When |
|-------------|-----------|------|
| ACTION | Seedance 2.0 | Only for high physical motion |
| EXPLAINER | Grok Imagine (Diagram Style) | Only when diagrams/animations needed |
| TEXT FOCUS | Grok Imagine (Diagram Style) | When text must appear on screen |
| Everything else | Default (Grok Imagine) | Standard cinematic pipeline |

---

## Structured Output

Every chunk produces machine-readable metadata:

```yaml
chunk: 07
narration: "the company had been keeping two different sets of accounting records"
duration: 10s
visual_type: EXPLAINER
generator: grok
confidence: 94%
reason:
  - "Core fraud mechanism — two parallel ledgers"
  - "Best shown as animated diagram, not cinematic footage"
camera_complexity: MEDIUM
visual_style: animation
priority: HIGH
```

---

## Routing Summary

After classification, produce instant visibility:

```
TOTAL: 92 chunks

Seedance 2.0: 0 chunks (0%)
Grok Imagine (Diagram Style): 12 chunks (13%)
Default Cinematic: 80 chunks (87%)

HIGH PRIORITY:
- Chunk 07: Core fraud reveal (EXPLAINER)
- Chunk 44: $4B gap visualization (EXPLAINER)
```

---

## Adding New Visual Types

1. Add type definition to `classification-rules.md`
2. Add generator mapping to `model-recommendations.md`
3. Update this README
4. Update metadata schema in `output-format.md`

The system is modular: new types and generators can be added without rewriting existing logic.

---

## Files

| File | Purpose |
|------|---------|
| `classification-rules.md` | Visual type definitions and classification logic |
| `model-recommendations.md` | Generator mapping for each visual type |
| `output-format.md` | Structured metadata schema |
| `README.md` | This file |
