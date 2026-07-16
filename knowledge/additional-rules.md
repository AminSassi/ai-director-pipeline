# Additional Production Rules

From director's live production experience. These supplement the rules in `AGENTS.md`.

## Short VO Integration
- If VO is short, integrate it into another prompt. Don't create a single frame/prompt for it.
- Example: "walking to kitchen, opening fridge, eating ice cream, leaving it on table" = ONE prompt with multiple shots describing the action.

## Active Scenes
- People doing things, not camera wandering around a room
- Every scene needs action, people, varied camera angles
- Make it feel alive like a movie, not random floating objects

## Visual Variety
- Change visual setting occasionally even if current location fits the VO
- Never repeat camera movements, body movements, scenes, or locations (except essential story locations like a house)
- Always introduce new angles and movements to catch viewer attention

## Emotional Focus
- During significant narrative moments, focus on the character's face, devastation, surprise
- Convey the weight of the situation through expression and reaction

## Creative Transitions
- End one prompt with character walking → start next with different character in different location using same camera angle/position
- Creates visual continuity across cuts

## Scene Composition
- Don't just show character walking in street
- Place camera behind a shop, integrate into crowd, add environmental activity
- Make it look like a movie, not a surveillance feed

## Pacing Mix
- Balance slower documentary scenes (zooming on person) with exciting moments
- Viewer stays engaged, story doesn't feel like random objects

## Cinematic Realism (4-Layer Prompt Build)
1. Subject & Action
2. Camera & Motion
3. Lens & Light
4. Texture & Mood

### The Problem
- Locked-off tripod = looks like a render
- Real cameras "breathe"

### The Toolkit
- Motion: handheld shake, slow sway, push-in
- Lens: 35–50mm, shallow depth of field
- Light: golden hour, practical glow, haze
- Texture: film grain, halation, soft grade

### Technique
- "Shoulder Rig" look (handheld gentle drift) adds weight and human intent

## Timing Calculation
- 27 words or 145 characters (including spaces) = 10 seconds of video

## Pipeline Engineer Approach
- Act as strict shot-by-shot pipeline engineer
- Do NOT summarize or group narrative
- Map script sequentially, word-for-word
- Every distinct action or phrase = at least one unique visual shot
- Output "Clip Math & VO Breakdown" before generating prompts

## Motion Constraints
- Include action but avoid very fast motion
- Fast motion causes AI model to break and create artifacts

## Platform Choice
- Ask director whether to use Kling or Grok for video generation
- Do not generate anything until script is provided
- Ensure every word in script is visually represented

## Character/Location Presentation
- Characters: front angle, head to toe, white background
- Locations: angle where everything is visible

## Locking Rules
- Lock characters, locations, special objects that appear more than once
- Tag locked elements at very beginning of prompt
- Even if they only appear in the final shot

## Prompt Format
- All prompts as plain text ready to copy-paste
- Character faces visible in character sheets

## Drone Continuous Shots
- Last frame of video N = start frame of video N+1
- Chain: FIRST FRAME → video prompt 1 → LAST FRAME → LAST FRAME becomes START FRAME → video prompt 2 → LAST FRAME
- Creates seamless drone/continuous shot effect
- Both start frame and end frame needed for each clip
