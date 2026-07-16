# Structured Output Format

Every chunk produces machine-readable metadata. Not pretty text. Structured data.

---

## Per-Chunk Metadata Schema

```yaml
chunk: <number>
narration: "<exact narration text>"
duration: <seconds>s
word_count: <number>
visual_type: <CINEMATIC|ACTION|EXPLAINER|MONTAGE|ARCHIVAL|EMOTIONAL|TRANSITION|TEXT_FOCUS|HYBRID>
generator: <seedance|gemini|default>
confidence: <0-100>%
reason:
  - <reason 1>
  - <reason 2>
  - <reason 3>
camera_complexity: <LOW|MEDIUM|HIGH>
visual_style: <cinematic|documentary|animation|archival|mixed>
requires_split: <true|false>
split_segments: <null|list of segments>
tags: <locked character/location tags>
priority: <NORMAL|HIGH>
notes: <any additional context>
```

---

## Example: Character Moment

```yaml
chunk: 01
narration: "In the mid-1970s, a young pharmacist named Bavaguthu Raghuram Shetty arrived in Abu Dhabi from a small town in southern India, reportedly with only a few dollars to his name."
duration: 10s
word_count: 31
visual_type: CINEMATIC
generator: default
confidence: 95%
reason:
  - "Character origin story — narrative, not explanatory"
  - "No diagrams or data visualization needed"
  - "Establishing shot of arrival in new city"
camera_complexity: LOW
visual_style: documentary
requires_split: false
split_segments: null
tags: []
priority: NORMAL
notes: "1970s Abu Dhabi setting, grainy film look"
```

---

## Example: Data Visualization

```yaml
chunk: 44
narration: "And that its public financial statements had misled investors by understating the company's debt by as much as four billion dollars."
duration: 10s
word_count: 20
visual_type: EXPLAINER
generator: gemini
confidence: 92%
reason:
  - "Core fraud visualization — $4B gap between reported and actual debt"
  - "Requires animated comparison: public filings vs internal records"
  - "Best shown as data visualization, not cinematic footage"
camera_complexity: MEDIUM
visual_style: animation
requires_split: false
split_segments: null
tags: []
priority: HIGH
notes: "Two ledger books side by side, showing gap"
```

---

## Example: Action Scene

```yaml
chunk: 50
narration: "On April 9th, 2020, following an application by NMC's largest creditor, Abu Dhabi Commercial Bank, which was owed roughly nine hundred sixty-three million dollars, a UK High Court judge placed NMC Health into administration."
duration: 10s
word_count: 42
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Institutional action — judge making ruling"
  - "Courtroom drama, not physical action"
  - "No chase, explosion, or fast movement"
camera_complexity: MEDIUM
visual_style: documentary
requires_split: false
split_segments: null
tags: []
priority: HIGH
notes: "Courtroom setting, judge speaking, dramatic weight"
```

---

## Routing Summary Format

After all chunks are classified, produce a summary:

```yaml
# ROUTING SUMMARY

total_chunks: 92
total_duration: ~15 minutes
total_words: 1400

generators:
  seedance:
    chunks: 0
    percentage: 0%
  gemini:
    chunks: 12
    percentage: 13%
  default:
    chunks: 80
    percentage: 87%

visual_types:
  CINEMATIC: 61
  ACTION: 0
  EXPLAINER: 12
  MONTAGE: 5
  ARCHIVAL: 2
  EMOTIONAL: 4
  TRANSITION: 3
  TEXT_FOCUS: 3
  HYBRID: 2

high_priority_chunks:
  - chunk: 07
    reason: "Core fraud reveal"
  - chunk: 44
    reason: "$4B gap visualization"
  - chunk: 50
    reason: "Administration moment"

chunk_map:
  - { chunk: 01, generator: default, visual_type: CINEMATIC }
  - { chunk: 02, generator: default, visual_type: CINEMATIC }
  - { chunk: 03, generator: default, visual_type: CINEMATIC }
  - { chunk: 04, generator: default, visual_type: CINEMATIC }
  - { chunk: 05, generator: default, visual_type: CINEMATIC }
  - { chunk: 06, generator: default, visual_type: CINEMATIC }
  - { chunk: 07, generator: gemini, visual_type: EXPLAINER }
  - { chunk: 08, generator: default, visual_type: CINEMATIC }
  - { chunk: 09, generator: default, visual_type: CINEMATIC }
  - { chunk: 10, generator: default, visual_type: CINEMATIC }
  # ... etc
```

---

## Pipeline Integration

Every downstream agent reads this metadata:

1. **Prompt Generator** reads `generator` and `visual_type` to determine which tool to use
2. **Camera Planner** reads `camera_complexity` and `visual_style` for angle decisions
3. **Quality Checker** reads `confidence` and `reason` to validate routing
4. **Director Dashboard** reads `chunk_map` for instant visibility

The metadata IS the routing decision. Pretty text is documentation only.
