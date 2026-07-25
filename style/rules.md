# Visual Style Rules

Core rules for visual consistency across all generated content.

## Documentary style

- Cinematic lighting, natural tones
- Film grain for archival/recreation scenes
- Consistent color palette per story segment
- Aspect ratio: 16:9 for YouTube (unless vertical content)

## Prompt structure (Grok Imagine - video)

Each 10-second clip prompt should include:
1. **Subject**: What/who is in the scene
2. **Action**: What is happening
3. **Camera**: Angle and movement
4. **Lighting**: Time of day, mood
5. **Style**: Film look, color grading
6. **Duration cue**: Implied pacing (slow/fast)

## Rules

- Under 35 words for best results (complex prompts cause hallucination)
- `--no` flags at end for negatives (Grok syntax only)
- `--ar 16:9` for aspect ratio
- Always specify camera movement for video clips
- Include "cinematic" or "film" in every prompt
- Specify aspect ratio explicitly
