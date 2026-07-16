# Changelog

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
