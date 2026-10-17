# Changelog

## v2.0.0 — 2026-10-17 (Forensic Anti-Slop & Cinematography Upgrade)

### Added
- **12 Signature Documentary Framing Archetypes (`camera/angles.md`):** Replaced the 34-line stub with a full cinematography playbook (Foreground Occlusion, `24mm` Architectural Worm's-Eye, `90°` God's-Eye Perpendicular, Low-Slung Surface Skimming, OTS Screen/Evidence Reveal, Backlit Chiaroscuro Silhouette, Parallel Steadicam Glide, Depth-Plane Macro Rack Focus, `15°` Low-Angle Dutch Tilt, Monumental Crane Pull-Back, Threshold Pull-Back, and Tactile Light-Table / Vox 2D Collage Glide).
- **Batch-Level Anti-Monotony Mandate (Rule #6):** Capped `"slow push in"` in `SHOT 1` to **at most 1 per 6-chunk batch (max 16.7%)** and banned consecutive chunks from opening with `Cinematic medium shot`.
- **The 2-Chunk Location Ceiling (Rule #26):** Banned staying in the same interior room or `@LOCATION` tag for more than 2 consecutive chunks; mandated pivoting on Chunk 3 to exterior infrastructure scale or a Rule #38 Explainer.
- **Moderation-Safe Human Presence (Rule #44):** Banned lazy `--no people, faces` empty-room slideshows on sensitive human-drama chunks; mandated backlit silhouettes, OTS framing past suit jackets, low-angle marching boots, and courtroom observers in shadow.
- **Mandatory 6-Chunk Pre-Generation Audit Matrix (`prompts/quality-checklist.md`, `SKILL.md`):** Replaced rubber-stamped checkboxes with a verifiable 8-column batch audit table.
- **Post-Mortem #004 (`knowledge/session-postmortems.md`):** Documented the root-cause analysis and fixes from the 55-chunk *Otto Warmbier* forensic audit.

### Fixed
- **4-Layer Persistence in Shots 2–6 (Rule #14, `golden-reference-mladic.md`, `style/rules.md`):** Closed the loophole that dropped lighting and texture layers after `SHOT 1`. Every individual `SHOT` line (`SHOT 1` through `SHOT 4/6`) now requires a compact 4–6 word Lens/Light + Texture/Mood token (`24mm`/`35mm`/`50mm` lens, chiaroscuro lighting, `film grain`) within 18–34 words.
- **Contradictory Hand & Tool Mechanics Purged (`additional-rules.md`, `learnings.md`, `workflow.md`, `golden-reference-aurora.md`, plugin `cinematography.md`):** Removed all legacy instructions recommending fountain pens writing, highlighters drawing, rubber stamps pressing, fingers typing, or calipers/loupes (strictly enforcing Rule #40).
- **Harmonized Start Frame vs. Video Header Tagging (Rule #8 & #12):** Clarified across all files that Start Frames tag ONLY assets physically visible in `Shot 1, Frame 0`, while Video Headers (`Use @image1...`) tag ALL locked assets appearing across `SHOT 1` through `SHOT 4/6`.
- **Harmonized CTA Rules (`SKILL.md` Rule #20):** Removed legacy `@channellogo`, subscribe button animation, and phone screen instructions at the bottom of `SKILL.md` to enforce pure atmospheric story continuity during CTAs.
- **Upgraded Phase 0.75 Scene Routing (`routing/`):** Replaced legacy `ACTION` (running/fighting/crowd panic) and `TEXT FOCUS` (on-screen readable text) routing categories with the **7 Documentary Visual Archetypes** (`HUMAN_CONFLICT`, `INFRASTRUCTURE_SCALE`, `EXPLAINER_LIGHT_TABLE`, `EXPLAINER_VOX_COLLAGE`, `ARCHIVAL_TABLEAU`, `MONTAGE_TIME_COMPRESSION`, `ATMOSPHERIC_TRANSITION`).

---

## v1.0.0 — 2026-07-16

### Added
- "Fully load my AI Director" bootstrap command
- Pipeline version number (1.0.0)
- Immutable artifact system (phase-0 through phase-0.4)
- Compression algorithm (5-pass deterministic editing)
- State guard logic
- Artifact invalidation rules
- Artifact metadata (status, version, word_count, ctas, source)
- Intelligent scene routing (routing/ directory)
- Visual intent classification (CINEMATIC, ACTION, EXPLAINER, etc.)
- Structured metadata output format
- Grok prompt rules (under 35 words)
- Kling prompt rules (separate negative field)
- Regression test suite (tests/regression-tests.md)

### Fixed
- AGENTS.md references to non-existent files (master-rules.md, filmmaking.md)
- Grok prompt length contradiction (80 words → 35 words)
- Negative prompt guidance inconsistency
- Shot count rule duplication (learnings.md → cross-reference)
- ULTIMATE_SKILL legacy references
- README.md phase numbering (added Phase 0.5, 0.6)
- README.md word count (1,600-1,900 for Phase 0)
- Duplicate content in AGENTS.md
- Dead workflow/state-machine.md (folded into knowledge/workflow.md)

### Removed
- workflow/state-machine.md (dead file, content folded into knowledge/workflow.md)
- Duplicate file structure listing from AGENTS.md

## v0.9.0 — Pre-release

### Added
- Initial repository structure
- knowledge/ module
- camera/ module
- style/ module
- prompts/ module
- scripts/ module
- routing/ module (scene classification, model recommendations)
