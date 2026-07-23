---
artifact: phase-0.75-routing.md
status: approved
version: 1.0
total_chunks: 58
total_duration: 538.3s
total_words: 1358
source: phase-0.6-chunks.md
created_by: pipeline
downstream_valid: true
routing_method: visual_intent_classification
---

# Phase 0.75 — Intelligent Scene Routing
## 1MDB Episode — INSOLVENT

---

## Routing Summary

```yaml
total_chunks: 58
total_duration: ~9 minutes
total_words: 1358

generators:
  seedance:
    chunks: 0
    percentage: 0%
  gemini:
    chunks: 4
    percentage: 7%
  default:
    chunks: 54
    percentage: 93%

visual_types:
  CINEMATIC: 38
  ACTION: 0
  EXPLAINER: 4
  MONTAGE: 3
  ARCHIVAL: 8
  EMOTIONAL: 3
  TRANSITION: 1
  TEXT_FOCUS: 1
  HYBRID: 0

high_priority_chunks:
  - chunk: 26
    reason: "Good Star Limited shell company reveal"
  - chunk: 29
    reason: "Goldman Sachs $6B bond fees"
  - chunk: 53
    reason: "$4.5B misappropriation visualization"
  - chunk: 54
    reason: "$1B into Najib's accounts"
```

---

## Chunk Map

### CHUNK 1 — 00:00:00 – 00:00:09 (9.4s, 33 words)
```yaml
chunk: 1
narration: "In 2013, a movie about greed, fraud, and Wall Street excess hit theaters worldwide. It starred Leonardo DiCaprio. It was nominated for five Oscars. It was called The Wolf of Wall Street."
duration: 9.4s
word_count: 33
visual_type: ARCHIVAL
generator: default
confidence: 95%
reason:
  - "Wolf of Wall Street is real film — use actual trailer clips or poster"
  - "Archival footage of movie premiere/release"
  - "DiCaprio as recognizable figure"
camera_complexity: LOW
visual_style: archival
requires_split: false
priority: NORMAL
notes: "Fair use/commentary for Wolf of Wall Street clips"
```

### CHUNK 2 — 00:00:10 – 00:00:19 (9.8s, 31 words)
```yaml
chunk: 2
narration: "Here's what almost nobody knew. A huge chunk of the money used to make that movie was allegedly stolen. Not from a bank, from an entire country."
duration: 9.8s
word_count: 31
visual_type: EMOTIONAL
generator: default
confidence: 90%
reason:
  - "Reveal moment — dramatic emphasis"
  - "Tension building through contrast"
  - "Atmospheric shot of Malaysia/country"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: HIGH
notes: "Dramatic pause, shift in tone"
```

### CHUNK 3 — 00:00:20 – 00:00:29 (9.4s, 24 words)
```yaml
chunk: 3
narration: "A young financier siphoned billions out of a government fund meant to build hospitals, schools, and"
duration: 9.4s
word_count: 24
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Character introduction — young financier"
  - "Government fund setting"
  - "Narrative storytelling"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Establishing shot of Malaysia, government buildings"
```

### CHUNK 4 — 00:00:29 – 00:00:39 (9.4s, 23 words)
```yaml
chunk: 4
narration: "infrastructure for millions, and used it to bankroll super yachts, a private jet, jewelry for supermodels,"
duration: 9.4s
word_count: 23
visual_type: CINEMATIC
generator: default
confidence: 92%
reason:
  - "Contrast between public purpose and private excess"
  - "Visual storytelling of luxury items"
  - "Cinematic montage of wealth"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Superyachts, private jets, jewelry — stock footage or recreation"
```

### CHUNK 5 — 00:00:39 – 00:00:48 (9.2s, 31 words)
```yaml
chunk: 5
narration: "parties with A-list celebrities, and yes, a movie about financial fraud, paid for with the proceeds of financial fraud."
duration: 9.2s
word_count: 31
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "Irony emphasis — movie about fraud funded by fraud"
  - "Celebrity party scenes"
  - "Narrative climax of hook"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Party scenes, celebrity cameos, ironic juxtaposition"
```

### CHUNK 6 — 00:00:48 – 00:00:57 (9.2s, 24 words)
```yaml
chunk: 6
narration: "The prime minister at the center of it all has been sentenced to prison twice. The man who orchestrated"
duration: 9.2s
word_count: 24
visual_type: ARCHIVAL
generator: default
confidence: 94%
reason:
  - "Prime Minister Najib Razak — real person"
  - "Courtroom/prison footage exists"
  - "Archival news footage of sentencing"
camera_complexity: LOW
visual_style: archival
requires_split: false
priority: NORMAL
notes: "Najib Razak courtroom photos, prison footage"
```

### CHUNK 7 — 00:00:57 – 00:01:07 (9.8s, 31 words)
```yaml
chunk: 7
narration: "the scheme has been missing for years, and nobody, not the FBI, not Interpol, has been able to find him."
duration: 9.8s
word_count: 31
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Manhunt narrative — Jho Low missing"
  - "International investigation drama"
  - "Mystery/suspense atmosphere"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Interpol notices, wanted posters, mystery atmosphere"
```

### CHUNK 8 — 00:01:07 – 00:01:15 (8.4s, 26 words)
```yaml
chunk: 8
narration: "This is the story of 1MDB, one of the largest financial heists in world history. And it starts with"
duration: 8.4s
word_count: 26
visual_type: CINEMATIC
generator: default
confidence: 92%
reason:
  - "Title card/establishing shot"
  - "1MDB logo/branding"
  - "Dramatic opening statement"
camera_complexity: LOW
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "1MDB establishing shot, dramatic title"
```

### CHUNK 9 — 00:01:16 – 00:01:25 (9s, 25 words)
```yaml
chunk: 9
narration: "two teenagers at a private school in England. Before we go any"
duration: 9s
word_count: 25
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "Harrow school setting — elite boarding school"
  - "Character origin story"
  - "England location establishing"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Harrow School, England, 1990s period setting"
```

### CHUNK 10 — 00:01:25 – 00:01:35 (10s, 25 words)
```yaml
chunk: 10
narration: "further, this channel exists to dig up stories exactly like this one,"
duration: 10s
word_count: 25
visual_type: TRANSITION
generator: default
confidence: 85%
reason:
  - "Subscribe CTA — channel branding"
  - "Visual break from narrative"
  - "Transition to subscribe prompt"
camera_complexity: LOW
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Channel branding, subscribe animation"
```

### CHUNK 11 — 00:01:35 – 00:01:44 (8.3s, 19 words)
```yaml
chunk: 11
narration: "the massive collapses nobody fully explains. If that's your kind"
duration: 8.3s
word_count: 19
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Channel pitch — value proposition"
  - "Montage of past episodes/collapses"
  - "Visual variety"
camera_complexity: LOW
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Quick cuts of past episodes, dramatic moments"
```

### CHUNK 12 — 00:01:44 – 00:01:53 (8.9s, 13 words)
```yaml
chunk: 12
narration: "of story, hit subscribe right now so you"
duration: 8.9s
word_count: 13
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "Subscribe CTA continuation"
  - "Visual call-to-action"
  - "Simple, direct"
camera_complexity: LOW
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Subscribe button animation, simple visual"
```

### CHUNK 13 — 00:01:53 – 00:02:00 (7.4s, 24 words)
```yaml
chunk: 13
narration: "don't lose this channel. Okay, back to Malaysia. In the late 1990s,"
duration: 7.4s
word_count: 24
visual_type: CINEMATIC
generator: default
confidence: 92%
reason:
  - "Transition back to story"
  - "Malaysia establishing shot"
  - "1990s period setting"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Kuala Lumpur skyline, 1990s era"
```

### CHUNK 14 — 00:02:00 – 00:02:10 (9.7s, 22 words)
```yaml
chunk: 14
narration: "a Malaysian teenager named Joe Low was sent to Harrow, one of"
duration: 9.7s
word_count: 22
visual_type: CINEMATIC
generator: default
confidence: 94%
reason:
  - "Character introduction — Jho Low"
  - "Young person at school"
  - "Origin story"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Teenager, school setting, period piece"
```

### CHUNK 15 — 00:02:10 – 00:02:19 (8.4s, 24 words)
```yaml
chunk: 15
narration: "Britain's most elite boarding schools. There, he became close"
duration: 8.4s
word_count: 24
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "Harrow School establishing"
  - "Elite British education setting"
  - "Atmospheric location"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Harrow School campus, traditional British architecture"
```

### CHUNK 16 — 00:02:19 – 00:02:27 (8.5s, 19 words)
```yaml
chunk: 16
narration: "friends with Riza Aziz, stepson of a rising"
duration: 8.5s
word_count: 19
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Character relationship introduction"
  - "Riza Aziz — real person"
  - "Friendship dynamic"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Two teenagers meeting, friendship formation"
```

### CHUNK 17 — 00:02:28 – 00:02:37 (9.1s, 21 words)
```yaml
chunk: 17
narration: "Malaysian politician named Najib Razak. That friendship would eventually"
duration: 9.1s
word_count: 21
visual_type: ARCHIVAL
generator: default
confidence: 92%
reason:
  - "Najib Razak — real politician"
  - "Archival footage of young Najib"
  - "Political career establishing"
camera_complexity: LOW
visual_style: archival
requires_split: false
priority: NORMAL
notes: "Najib Razak archival photos/footage"
```

### CHUNK 18 — 00:02:38 – 00:02:47 (9.6s, 22 words)
```yaml
chunk: 18
narration: "help move billions out of a country. Fast forward to 2009."
duration: 9.6s
word_count: 22
visual_type: MONTAGE
generator: default
confidence: 88%
reason:
  - "Time jump — late 1990s to 2009"
  - "Years passing montage"
  - "Transition between eras"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Time-lapse, years ticking, Malaysia development"
```

### CHUNK 19 — 00:02:47 – 00:02:57 (9.6s, 28 words)
```yaml
chunk: 19
narration: "Najib becomes prime minister. Almost immediately, he sets up one Malaysia development"
duration: 9.6s
word_count: 28
visual_type: CINEMATIC
generator: default
confidence: 92%
reason:
  - "Political milestone — PM inauguration"
  - "Government announcement"
  - "Institutional moment"
camera_complexity: MEDIUM
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Najib becoming PM, official ceremony"
```

### CHUNK 20 — 00:02:57 – 00:03:07 (9.7s, 25 words)
```yaml
chunk: 20
narration: "burhad, 1MDB. On paper, attract foreign investment, fund infrastructure."
duration: 9.7s
word_count: 25
visual_type: EXPLAINER
generator: gemini
confidence: 85%
reason:
  - "1MDB mission statement — on paper vs reality"
  - "Animated diagram of fund purpose"
  - "Infrastructure visualization"
camera_complexity: MEDIUM
visual_style: animation
requires_split: false
priority: NORMAL
notes: "1MDB logo, infrastructure graphics, investment flow"
```

### CHUNK 21 — 00:03:08 – 00:03:17 (9.4s, 23 words)
```yaml
chunk: 21
narration: "In reality, prosecutors would later say it became a personal piggy bank"
duration: 9.4s
word_count: 23
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "Reveal moment — contrast between stated purpose and reality"
  - "Dramatic emphasis"
  - "Atmospheric shift"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: HIGH
notes: "Tone shift, darker lighting, dramatic pause"
```

### CHUNK 22 — 00:03:17 – 00:03:26 (8.1s, 20 words)
```yaml
chunk: 22
narration: "run with the help of Joe Low, who"
duration: 8.1s
word_count: 20
visual_type: CINEMATIC
generator: default
confidence: 92%
reason:
  - "Jho Low as shadow operator"
  - "Character introduction深化"
  - "Behind-the-scenes figure"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Jho Low portrait, mysterious figure"
```

### CHUNK 23 — 00:03:27 – 00:03:35 (8.5s, 23 words)
```yaml
chunk: 23
narration: "never held any official position inside the fund. In 2009, 1MDB entered"
duration: 8.5s
word_count: 23
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Ironic reveal — no official position"
  - "Narrative emphasis"
  - "Transition to scheme details"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Jho Low working behind scenes, no title"
```

### CHUNK 24 — 00:03:36 – 00:03:44 (8.6s, 20 words)
```yaml
chunk: 24
narration: "a joint venture with a Saudi oil company. The fund put in"
duration: 8.6s
word_count: 20
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "Business deal — Saudi oil company"
  - "Joint venture establishing"
  - "Corporate setting"
camera_complexity: MEDIUM
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Saudi Arabia, oil company, business meeting"
```

### CHUNK 25 — 00:03:45 – 00:03:54 (9s, 22 words)
```yaml
chunk: 25
narration: "$1 billion. Almost immediately, around 700 million was rerouted into"
duration: 9s
word_count: 22
visual_type: EXPLAINER
generator: gemini
confidence: 92%
reason:
  - "Money flow visualization — $1B → $700M rerouted"
  - "Animated diagram of fund movement"
  - "Shell company mechanism"
camera_complexity: MEDIUM
visual_style: animation
requires_split: false
priority: HIGH
notes: "Animated money flow, arrows, shell company diagram"
```

### CHUNK 26 — 00:03:54 – 00:04:03 (9.3s, 17 words)
```yaml
chunk: 26
narration: "a shell company called Goodstar Limited. Its function?"
duration: 9.3s
word_count: 17
visual_type: EXPLAINER
generator: gemini
confidence: 94%
reason:
  - "Shell company reveal — Good Star Limited"
  - "Animated corporate structure"
  - "How the fraud worked"
camera_complexity: MEDIUM
visual_style: animation
requires_split: false
priority: HIGH
notes: "Good Star Limited logo, shell company diagram"
```

### CHUNK 27 — 00:04:03 – 00:04:13 (9.6s, 26 words)
```yaml
chunk: 27
narration: "Move stolen money where it couldn't be traced. Over the next few"
duration: 9.6s
word_count: 26
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Mechanism explanation — money movement"
  - "Visual storytelling of fraud"
  - "Narrative flow"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Money movement, international routing"
```

### CHUNK 28 — 00:04:13 – 00:04:22 (9.3s, 23 words)
```yaml
chunk: 28
narration: "years, 1MDB kept raising money through massive bond"
duration: 9.3s
word_count: 23
visual_type: MONTAGE
generator: default
confidence: 85%
reason:
  - "Time compression — years of fundraising"
  - "Repeated bond sales"
  - "Montage of financial activity"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Bond certificates, financial documents, time passing"
```

### CHUNK 29 — 00:04:23 – 00:04:32 (9.6s, 28 words)
```yaml
chunk: 29
narration: "sales arranged with Goldman Sachs. Goldman helped raise over"
duration: 9.6s
word_count: 28
visual_type: ARCHIVAL
generator: default
confidence: 92%
reason:
  - "Goldman Sachs — real institution"
  - "Archival footage of Goldman offices"
  - "Wall Street establishing"
camera_complexity: LOW
visual_style: archival
requires_split: false
priority: HIGH
notes: "Goldman Sachs building, Wall Street, financial district"
```

### CHUNK 30 — 00:04:32 – 00:04:41 (9.2s, 31 words)
```yaml
chunk: 30
narration: "$6 billion. The fees were dramatically higher than typical."
duration: 9.2s
word_count: 31
visual_type: EXPLAINER
generator: gemini
confidence: 90%
reason:
  - "Fee comparison — typical vs Goldman fees"
  - "Animated chart/graph"
  - "Data visualization of unusual fees"
camera_complexity: MEDIUM
visual_style: animation
requires_split: false
priority: HIGH
notes: "Bar chart comparison, fee visualization"
```

### CHUNK 31 — 00:04:42 – 00:04:51 (9.2s, 18 words)
```yaml
chunk: 31
narration: "So unusually large, they became central evidence against"
duration: 9.2s
word_count: 18
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Dramatic emphasis — evidence reveal"
  - "Legal/investigation tone"
  - "Narrative weight"
camera_complexity: MEDIUM
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Courtroom, legal documents, investigation"
```

### CHUNK 32 — 00:04:51 – 00:04:59 (8.2s, 19 words)
```yaml
chunk: 32
narration: "the bank. Billions flowed through 1MDB."
duration: 8.2s
word_count: 19
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "Goldman Sachs conclusion"
  - "Scale emphasis — billions"
  - "Narrative transition"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Goldman Sachs, financial scale"
```

### CHUNK 33 — 00:05:00 – 00:05:09 (8.8s, 18 words)
```yaml
chunk: 33
narration: "Billions flowed into shell"
duration: 8.8s
word_count: 18
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Money flow narrative"
  - "Visual storytelling"
  - "Shell company emphasis"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Money movement, international routing"
```

### CHUNK 34 — 00:05:09 – 00:05:18 (9.7s, 25 words)
```yaml
chunk: 34
narration: "companies, private accounts, and a global spending spree"
duration: 9.7s
word_count: 25
visual_type: MONTAGE
generator: default
confidence: 90%
reason:
  - "Global spending spree — montage"
  - "Multiple locations"
  - "Time compression of excess"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Luxury lifestyle, international locations"
```

### CHUNK 35 — 00:05:19 – 00:05:29 (9.6s, 23 words)
```yaml
chunk: 35
narration: "nobody in Malaysia knew was happening. Joe Low became a"
duration: 9.6s
word_count: 23
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Public ignorance reveal"
  - "Jho Low transformation"
  - "Character development"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Malaysian public, Jho Low lifestyle change"
```

### CHUNK 36 — 00:05:29 – 00:05:38 (9s, 22 words)
```yaml
chunk: 36
narration: "legend on the party circuit. Hundreds of thousands on"
duration: 9s
word_count: 22
visual_type: CINEMATIC
generator: default
confidence: 92%
reason:
  - "Party lifestyle — nightclub scenes"
  - "Champagne excess"
  - "Celebrity party atmosphere"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Nightclub, champagne, VIP section"
```

### CHUNK 37 — 00:05:38 – 00:05:47 (9.5s, 26 words)
```yaml
chunk: 37
narration: "champagne in a single night. He partied with Paris"
duration: 9.5s
word_count: 26
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "Celebrity party — Paris Hilton"
  - "Excess lifestyle"
  - "A-list social circle"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Paris Hilton, celebrity parties, VIP"
```

### CHUNK 38 — 00:05:47 – 00:05:56 (9.2s, 25 words)
```yaml
chunk: 38
narration: "Hilton. He gifted a Picasso and a Basquiat worth"
duration: 9.2s
word_count: 25
visual_type: CINEMATIC
generator: default
confidence: 92%
reason:
  - "Art gifts — Picasso, Basquiat"
  - "Luxury excess"
  - "Visual wealth display"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Art pieces, gallery, luxury gifts"
```

### CHUNK 39 — 00:05:56 – 00:06:05 (8.7s, 24 words)
```yaml
chunk: 39
narration: "millions. He chartered super yachts. He bought real estate"
duration: 8.7s
word_count: 24
visual_type: CINEMATIC
generator: default
confidence: 94%
reason:
  - "Superyachts, real estate"
  - "Luxury assets"
  - "Visual wealth montage"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Superyacht, Beverly Hills property, London flat"
```

### CHUNK 40 — 00:06:06 – 00:06:16 (9.7s, 23 words)
```yaml
chunk: 40
narration: "in Beverly Hills, New York, and London. And in 2012, he"
duration: 9.7s
word_count: 23
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "International real estate — multiple cities"
  - "Location montage"
  - "Global footprint"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Beverly Hills, NYC, London skylines"
```

### CHUNK 41 — 00:06:16 – 00:06:25 (9s, 20 words)
```yaml
chunk: 41
narration: "helped finance a Martin Scorsese film. Riza Aziz started a"
duration: 9s
word_count: 20
visual_type: ARCHIVAL
generator: default
confidence: 92%
reason:
  - "Martin Scorsese — real filmmaker"
  - "Hollywood connection"
  - "Archival film references"
camera_complexity: LOW
visual_style: archival
requires_split: false
priority: NORMAL
notes: "Scorsese, Hollywood, film production"
```

### CHUNK 42 — 00:06:25 – 00:06:33 (7.9s, 20 words)
```yaml
chunk: 42
narration: "Hollywood production company called Red Granite Pictures."
duration: 7.9s
word_count: 20
visual_type: ARCHIVAL
generator: default
confidence: 94%
reason:
  - "Red Granite Pictures — real company"
  - "Hollywood production establishing"
  - "Archival company footage"
camera_complexity: LOW
visual_style: archival
requires_split: false
priority: NORMAL
notes: "Red Granite Pictures logo, Hollywood offices"
```

### CHUNK 43 — 00:06:33 – 00:06:42 (8.7s, 14 words)
```yaml
chunk: 43
narration: "In 2013, that company produced The Wolf of"
duration: 8.7s
word_count: 14
visual_type: ARCHIVAL
generator: default
confidence: 96%
reason:
  - "Wolf of Wall Street production"
  - "Film premiere/release"
  - "Archival movie footage"
camera_complexity: LOW
visual_style: archival
requires_split: false
priority: NORMAL
notes: "Wolf of Wall Street poster, premiere, DiCaprio"
```

### CHUNK 44 — 00:06:42 – 00:06:51 (8.8s, 23 words)
```yaml
chunk: 44
narration: "Wall Street, starring Leonardo DiCaprio. Prosecutors later alleged a"
duration: 8.8s
word_count: 23
visual_type: ARCHIVAL
generator: default
confidence: 92%
reason:
  - "DiCaprio starring role"
  - "Film clips — fair use"
  - "Archival movie footage"
camera_complexity: LOW
visual_style: archival
requires_split: false
priority: NORMAL
notes: "DiCaprio in character, film scenes"
```

### CHUNK 45 — 00:06:51 – 00:07:00 (9.2s, 17 words)
```yaml
chunk: 45
narration: "significant share of that film's budget can be"
duration: 9.2s
word_count: 17
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Prosecution allegation"
  - "Legal/investigation tone"
  - "Narrative weight"
camera_complexity: MEDIUM
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Courtroom, legal documents, investigation"
```

### CHUNK 46 — 00:07:00 – 00:07:09 (9.4s, 25 words)
```yaml
chunk: 46
narration: "traced back to money diverted from 1MDB. DiCaprio was never accused"
duration: 9.4s
word_count: 25
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "DiCaprio exoneration"
  - "Character moment — fair treatment"
  - "Narrative justice"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "DiCaprio cooperating, returning gifts"
```

### CHUNK 47 — 00:07:10 – 00:07:19 (9.2s, 20 words)
```yaml
chunk: 47
narration: "of knowingly taking part in the fraud. He cooperated with investigators,"
duration: 9.2s
word_count: 20
visual_type: CINEMATIC
generator: default
confidence: 92%
reason:
  - "DiCaprio cooperation"
  - "Legal process"
  - "Character integrity"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "DiCaprio returning items, cooperating"
```

### CHUNK 48 — 00:07:20 – 00:07:29 (9.6s, 25 words)
```yaml
chunk: 48
narration: "and both he and his foundation returned gifts,"
duration: 9.6s
word_count: 25
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "Gift return — Brando Oscar, art"
  - "Visual items"
  - "Narrative resolution"
camera_complexity: MEDIUM
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Brando Oscar statuette, art pieces"
```

### CHUNK 49 — 00:07:30 – 00:07:39 (9.3s, 23 words)
```yaml
chunk: 49
narration: "including a Marlon Brando Oscar statuette and pieces"
duration: 9.3s
word_count: 23
visual_type: CINEMATIC
generator: default
confidence: 94%
reason:
  - "Specific items — Oscar, art"
  - "Visual display of returned gifts"
  - "Narrative detail"
camera_complexity: MEDIUM
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Oscar statuette, art pieces, gallery"
```

### CHUNK 50 — 00:07:39 – 00:07:48 (8.9s, 14 words)
```yaml
chunk: 50
narration: "of art tied to 1MDB money."
duration: 8.9s
word_count: 14
visual_type: CINEMATIC
generator: default
confidence: 92%
reason:
  - "1MDB money connection"
  - "Ironic emphasis"
  - "Narrative conclusion"
camera_complexity: LOW
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Art pieces, 1MDB connection"
```

### CHUNK 51 — 00:07:48 – 00:07:57 (9.4s, 21 words)
```yaml
chunk: 51
narration: "The irony is hard to overstate. A movie warning about"
duration: 9.4s
word_count: 21
visual_type: EMOTIONAL
generator: default
confidence: 90%
reason:
  - "Ironic emphasis — movie about fraud"
  - "Dramatic irony"
  - "Atmospheric weight"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: HIGH
notes: "Dramatic pause, ironic juxtaposition"
```

### CHUNK 52 — 00:07:58 – 00:08:07 (9.3s, 26 words)
```yaml
chunk: 52
narration: "financial fraud was allegedly partly paid for with the actual proceeds of"
duration: 9.3s
word_count: 26
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Irony payoff"
  - "Narrative climax"
  - "Thematic resolution"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Wolf of Wall Street poster, ironic juxtaposition"
```

### CHUNK 53 — 00:08:07 – 00:08:17 (9.5s, 23 words)
```yaml
chunk: 53
narration: "financial fraud. By the early 2000s, roughly $4.5 billion"
duration: 9.5s
word_count: 23
visual_type: EXPLAINER
generator: gemini
confidence: 94%
reason:
  - "Scale visualization — $4.5B total"
  - "Animated counter/visualization"
  - "Data emphasis"
camera_complexity: MEDIUM
visual_style: animation
requires_split: false
priority: HIGH
notes: "$4.5 billion counter, scale visualization"
```

### CHUNK 54 — 00:08:17 – 00:08:26 (9.2s, 23 words)
```yaml
chunk: 54
narration: "had allegedly been misappropriated from 1MDB. Investigators say around a"
duration: 9.2s
word_count: 23
visual_type: CINEMATIC
generator: default
confidence: 88%
reason:
  - "Investigation narrative"
  - "Scale emphasis"
  - "Narrative weight"
camera_complexity: MEDIUM
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Investigators, evidence, scale"
```

### CHUNK 55 — 00:08:26 – 00:08:36 (9.7s, 25 words)
```yaml
chunk: 55
narration: "billion flowed into Najib's personal bank accounts. For years, almost nobody"
duration: 9.7s
word_count: 25
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "Najib's personal accounts"
  - "Secret/hidden money"
  - "Narrative revelation"
camera_complexity: MEDIUM
visual_style: documentary
requires_split: false
priority: NORMAL
notes: "Bank accounts, hidden money, secrecy"
```

### CHUNK 56 — 00:08:36 – 00:08:45 (9.7s, 25 words)
```yaml
chunk: 56
narration: "knew. This is the point in the story where"
duration: 9.7s
word_count: 25
visual_type: EMOTIONAL
generator: default
confidence: 88%
reason:
  - "Dramatic pause — everything about to change"
  - "Tension building"
  - "Atmospheric shift"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: HIGH
notes: "Dramatic pause, anticipation, tension"
```

### CHUNK 57 — 00:08:45 – 00:08:55 (9.3s, 30 words)
```yaml
chunk: 57
narration: "everything's about to blow wide open. And trust me, what happens next involves a"
duration: 9.3s
word_count: 30
visual_type: CINEMATIC
generator: default
confidence: 92%
reason:
  - "Teaser for what's next"
  - "Dramatic promise"
  - "Narrative hook"
camera_complexity: MEDIUM
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Anticipation, upcoming drama"
```

### CHUNK 58 — 00:08:55 – 00:08:58 (2.8s, 10 words)
```yaml
chunk: 58
narration: "fearless journalist, a stolen election."
duration: 2.8s
word_count: 10
visual_type: CINEMATIC
generator: default
confidence: 90%
reason:
  - "Teaser elements — journalist, election"
  - "Dramatic preview"
  - "Narrative cliffhanger"
camera_complexity: LOW
visual_style: cinematic
requires_split: false
priority: NORMAL
notes: "Journalist, election, preview of next section"
```

---

## High Priority Chunks

| Chunk | Visual Type | Generator | Reason |
|-------|-------------|-----------|--------|
| 2 | EMOTIONAL | default | Reveal moment — dramatic emphasis |
| 20 | EXPLAINER | gemini | 1MDB mission statement visualization |
| 25 | EXPLAINER | gemini | $1B → $700M money flow |
| 26 | EXPLAINER | gemini | Good Star Limited shell company |
| 29 | ARCHIVAL | default | Goldman Sachs establishing |
| 30 | EXPLAINER | gemini | Fee comparison visualization |
| 51 | EMOTIONAL | default | Ironic emphasis — movie about fraud |
| 53 | EXPLAINER | gemini | $4.5B total visualization |
| 56 | EMOTIONAL | default | Dramatic pause — everything changes |

---

## Generator Distribution

| Generator | Chunks | Percentage |
|-----------|--------|------------|
| Default (Grok/Kling) | 54 | 93% |
| Gemini OmniFlash | 4 | 7% |
| Seedance 2.0 | 0 | 0% |

## Visual Type Distribution

| Visual Type | Chunks | Percentage |
|-------------|--------|------------|
| CINEMATIC | 38 | 66% |
| ARCHIVAL | 8 | 14% |
| EXPLAINER | 4 | 7% |
| EMOTIONAL | 3 | 5% |
| MONTAGE | 3 | 5% |
| TRANSITION | 1 | 2% |
| TEXT_FOCUS | 1 | 2% |
| ACTION | 0 | 0% |
| HYBRID | 0 | 0% |

---

## Locked Assets (Required for Consistency)

| Asset | Type | First Appearance |
|-------|------|------------------|
| JHO LOW | Character | Chunk 14 |
| NAJIB RAZAK | Character | Chunk 17 |
| RIZA AZIZ | Character | Chunk 16 |
| 1MDB | Location/Brand | Chunk 8 |
| HARROW SCHOOL | Location | Chunk 9 |
| GOLDMAN SACHS | Location/Brand | Chunk 29 |
| RED GRANITE PICTURES | Location/Brand | Chunk 42 |

---

## Next Steps

- Phase 1: Pre-Production (asset scan, boards, clip math, scene map, energy map, music prompt)
- Phase 2: Generation (start frame → video prompt → self-review → director approval)

Ready to proceed with Phase 1?
