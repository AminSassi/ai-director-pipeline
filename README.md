# AI Director Pipeline

Persistent knowledge base for AI-generated documentary/film production.

## How to use

1. Push this folder to GitHub
2. Start a MiMo session
3. Say: "Load my AI director pipeline from [github-url]"
4. MiMo reads AGENTS.md + knowledge/learnings.md + style/ + camera/
5. Start working — corrections get auto-captured to knowledge/

## Structure

```
ai-director-pipeline/
├── AGENTS.md          # System instructions (loaded every session)
├── prompts/           # Reusable prompt templates
│   └── quality-checklist.md
├── camera/            # Camera angles & movements reference
│   └── angles.md
├── scripts/           # Script templates
│   └── template.md
├── knowledge/         # Auto-learned corrections
│   └── learnings.md
├── style/             # Visual style rules
│   └── rules.md
└── output/            # Generated scripts & shot lists
```

## AI-Corrects-AI Pipeline

Every prompt goes through:
1. Generate initial version
2. Self-review against style/rules.md + camera/angles.md
3. Refine and present final version
4. Director correction → auto-capture to knowledge/

## Adding knowledge

Just tell MiMo during any session:
- "Note: wide shots work better for establishing scenes"
- "Remember: Grok needs 'cinematic' in every prompt"
- "Always use Dutch angle for tension scenes"

MiMo writes it to knowledge/learnings.md automatically.
