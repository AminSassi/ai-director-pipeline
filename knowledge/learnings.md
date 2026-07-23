# Learnings

Accumulated corrections and discoveries from sessions. Updated automatically when the director shares insights.

---

## New entries are appended below this line

- [2026-06-25] INSIGHT: Reflection shots in screens/laptops cause AI to generate weird cloned/duplicated person effects. NEVER use "reflection visible in screen" or similar reflection descriptions. Avoid any shot where character appears inside a reflective surface.

- [2026-06-25] INSIGHT: Floating items, floating text, floating logos, weird glowing effects make video look AI-generated. Always use real-world grounded visuals only.

- [2026-06-25] INSIGHT: No super fast camera motion — causes AI artifacts and breaks generation.

- [2026-06-25] INSIGHT: Plastic/humanoid looking characters — specify skin texture, hair detail, clothing wrinkles for realism.

- [2026-06-25] INSIGHT: Before EVERY prompt generation, re-read the full GitHub repo rules even after long breaks. User requires this.

- [2026-06-25] INSIGHT: "Stamp being pressed" causes AI to spawn stamp from nowhere, oversized. AVOID stamp/stamping actions — use signing, writing, or other hand actions instead.

- [2026-06-25] INSIGHT: When describing hacker at screens, specify "figure facing screens, back to camera" or "figure's back visible, screens ahead" — otherwise AI puts screens facing viewer instead of character.

- [2026-06-25] INSIGHT: Doors in AI video are unreliable — they open/close spontaneously, multiply, or behave weirdly. AVOID door shots entirely or use extreme close-up of handle only.

- [2026-06-25] INSIGHT: Over-describing details in video prompts causes Grok to hallucinate trying to follow everything. Keep video prompts SHORT with only essential realism and story details. Less is more.

- [2026-06-25] INSIGHT: "Torn paper style" — when user asks for this, use: Aged paper texture background, black and white photograph style, bold typewriter font, aged sepia and greyscale tones, film grain texture, high contrast shadows, investigative documentary thumbnail style, 4K, --ar 16:9, --no blur --no watermark --no artifacts --no distortion --no photorealism. Photo should look like printed article clipping with white border around image.

- [2026-06-25] INSIGHT: YouTube Thumbnail Structure (True Crime style):
  1. Camera/Visual Style (ultrarealistic cinematic photography, 35mm anamorphic lens, film grain, etc.)
  2. "IMPORTANT: High-CTR true crime YouTube thumbnail"
  3. Pitch-black negative space on LEFT or RIGHT
  4. Subject/Scene description (what's visible)
  5. Typography in black space: WHITE top line (hook word) + BLOOD-RED bottom line (impact word)
  6. Mood description (chilling, eerie, gritty, etc.)
  7. Technical: 4k, high quality, --ar 16:9
  8. --no flags (daylight, clean aesthetic, smiling, etc.)
  Example structure: [style] + IMPORTANT: High-CTR + [black space side] + [scene] + [text: WHITE top / RED bottom] + [mood] + 4k --ar 16:9 --no flags

- [2026-06-25] INSIGHT: Locked Assets Workflow — Before generating prompts, identify ALL recurring characters, locations, objects that appear more than once. Create reference sheet prompts for each FIRST. Generate and lock them. Then use them in all future prompts as "same [character/location/object]". Ensures visual consistency throughout.

## LOCKED ASSET TEMPLATES (USE THESE)

### CHARACTER REFERENCE SHEET TEMPLATE
```
Professional character reference sheet, technical model turnaround style, clean neutral plain background, photorealistic. [CHARACTER DESCRIPTION]. Two horizontal rows. Top row: four full-body standing views — front view, left profile view facing left, right profile view facing right, back view. Bottom row: three close-up portraits — front portrait, left profile portrait facing left, right profile portrait facing right. Relaxed A-pose, consistent scale, accurate anatomy, clear silhouette, even spacing, uniform framing, consistent head height and facial scale across all panels. Same direction intensity and softness lighting across all panels, natural controlled shadows. Canon SL3, 17-85mm lens, fine pores, DSLR photography look, no airbrush, no CGI retouch, no text overlays. Landscape 16:9 -no white background or white bars
```

### LOCATION REFERENCE SHEET TEMPLATE
```
Create a professional location reference sheet. Clean neutral background, technical reference style. Arrange into a grid of six views: top row — wide establishing shot of [LOCATION 1], medium shot of [LOCATION 2], close detail of [LOCATION 3]. Bottom row — aerial view of [LOCATION 4], [LOCATION 5], [LOCATION 6]. Maintain consistent location identity across all panels — [LOCATION IDENTITY DESCRIPTION]. Lighting consistent across panels. Sharp details, photorealistic, Canon SL3, 17-85mm lens. No text overlays. Landscape 16:9 -no white background or white bars
```

- [2026-06-25] INSIGHT: Shot Count by Word Count — See `knowledge/critical-rules.md` Broken Rule #4 for the canonical table.

- [2026-06-25] INSIGHT: Video prompts use SHOT 1/2/3/4 format. Each shot = 1 camera angle + 1 action. No more than 4 shots per 10-second clip.

- [2026-06-25] INSIGHT: Grok Imagine — keep prompts SHORT and SIMPLE (under 35 words for best results). Complex prompts cause hallucination. --ar 16:9 at end. --no flags for negatives.

- [2026-06-25] INSIGHT: Grok "expand video" feature extends from last frame — use for scene transitions. Start frame + expand = seamless continuation.

- [2026-06-25] INSIGHT: YouTube workflow — 1 long video + 3 shorts. Long video gets 3 title options for A/B testing + description + tags. Each short gets its own title, all shorts share same description and tags.

- [2026-06-25] INSIGHT: Image prompts can be more detailed than video prompts. Video prompts should be SHORT to avoid hallucination. Image = detailed scene setting, Video = simple action beats.

- [2026-06-25] INSIGHT: Brand names (iPhone, Sony, Google, Facebook, etc.) can get flagged by AI generators — describe concepts without naming brands when possible.

- [2026-06-25] INSIGHT: Character reference sheets — front angle, head to toe, white background. Location reference sheets — angle where everything is visible. Lock them before starting scene prompts.

- [2026-06-25] INSIGHT: Thumbnail prompts with "dark room", "film grain", "harsh lighting" can make user's photo look too dark and unclear. For personal photos/video stills, use "bright", "well-lit", "natural lighting", "clear face visible" to keep subject bright while black space stays dark.

- [2026-07-17] INSIGHT: NEVER use split screen effects — looks like AI slop, cheap, breaks immersion. Use grounded cinematic transitions instead. NEVER write "split screen" in any shot description. If showing growth/comparison, use time-lapse, montage, or sequential shots — NOT split screen.

- [2026-07-17] INSIGHT: NEVER use generic noir tropes (rain-soaked streets, silhouettes at windows, detective aesthetics) — stay grounded in the ACTUAL story setting. NMC Health = Gulf region = warm desert tones, golden hour, Abu Dhabi architecture. Match colors/atmosphere to story location.

- [2026-07-17] INSIGHT: NEVER do same first frame, same plan, same angle, same idea across chunks. Always introduce new visual approaches. Repetition kills creativity and wastes credits.

- [2026-07-17] INSIGHT: Short VO (2-5 words) = 2 shots max. Only when correcting previously generated chunks.

- [2026-07-17] INSIGHT: ALWAYS tag locked assets at VERY BEGINNING of prompt — even if character only appears in final shot. NEVER put tags in middle of prompt. Tag placement: @TAG1 @TAG2 at start, then description. Example: "@YOUNGSHETTY @NMCCLINIC Young Indian pharmacist walking toward clinic..." NOT "Young Indian pharmacist @YOUNGSHETTY walking toward @NMCCLINIC clinic..."

- [2026-07-17] INSIGHT: "Open parentheses" = Seedance 2.0 mode. "Close parentheses" = Grok/Kling mode. Switch between them as director instructs.

- [2026-07-17] INSIGHT: Always include script text before each chunk prompt so director can verify sync.

- [2026-07-17] INSIGHT: Work in batches of 4 chunks. Wait for "done" before next batch.

- [2026-07-17] INSIGHT: When correcting chunks, can use fewer shots for short VO segments (breaks the 4-shot rule).

- [2026-07-17] INSIGHT: Locked asset reference sheets use Canon SL3, 17-85mm lens format. Character = front angle, head to toe, white background. Location = angle where everything visible.

- [2026-07-17] INSIGHT: Grok video prompts: use @image1 as visual anchor as start frame @TAGS. First frame uses Nano Banana 2. Video uses Grok.

- [2026-07-17] INSIGHT: Always re-read repo files before starting prompt generation — director requires this every session.

- [2026-07-17] INSIGHT: Push changes to GitHub immediately after saving to learnings.md — director uses multiple PCs and needs synced repo.

- [2026-07-17] CRITICAL: NEVER repeat the same action across multiple chunks. "Walking" is banned as default action. Vary actions: sitting, standing, reviewing documents, talking on phone, typing, looking out window, signing papers, pacing, gesturing, embracing, pointing, writing, dialing, hanging up, opening doors, closing doors, picking up objects, setting down objects. Minimum 3 different actions per 4-chunk batch.

- [2026-07-17] CRITICAL: MiMo UI has rendering bug where text appears without spaces. NEVER type long text (descriptions, tags, metadata) directly in chat. ALWAYS write to file on Desktop first, then tell user to copy-paste from file. This is permanent — no fix possible from our side.

- [2026-07-22] CRITICAL: Self-Review After Every Prompt — After generating each prompt, review against these checks:
  1. Are characters MID-ACTION (never posed)?
  2. Is there at least ONE creative angle (worm's eye, dutch tilt, through-glass, macro, bird's eye, ground-level tracking, first-person POV, reverse angle, orbital arc)?
  3. Are there at least 3 different camera movements across the 4 shots?
  4. Is every word of narration visually represented?
  5. Are scenes ALIVE with action (not camera wandering)?
  6. Is there visual variety (no repeated angles/movements)?
  7. Does each shot have Subject & Action, Camera & Motion, Lens & Light, Texture & Mood?
  8. Are characters caught mid-action (not static)?
  9. Is scene composition interesting (behind objects, in crowd, environmental activity)?
  10. Would you freeze this frame and see implied motion? If yes = correct.

- [2026-07-22] CRITICAL: Paste prompts directly in chat, not just save to files. User needs one-button copy-paste access.

- [2026-07-22] CRITICAL: NEVER use glowing UI elements, floating buttons, cursors, or digital overlays in video prompts. These look AI-generated and funny. Use real-world grounded visuals only — real people, real objects, real environments. Subscribe CTAs should show real people gesturing, real phone/computer screens, or cinematic text overlays — NOT floating buttons with lens flares.

- [2026-07-23] CRITICAL: USER PROVIDES CHUNKS — Agent is BAD at chunking from SRT. NEVER parse SRT to create chunks. User will always provide a pre-chunked file (VO_10s_chunks.txt or similar). Use that file as the source of truth. If user gives you SRT, ask for the chunked file instead.

- [2026-07-23] CRITICAL: Video prompts must be ONE-BUTTON COPIABLE — All prompts (start frame + video) must be written directly in chat for copy-paste. Do NOT just save to files. User needs to copy-paste directly into generators.

- [2026-07-23] CRITICAL: Tags at BEGINNING AND MIDDLE — Video prompt format:
  BEGINNING: @TAG1 @TAG2 (all locked assets for the chunk)
  MIDDLE: @TAG1 (specific asset appearing in THAT specific shot)
  Example: "@JHOLOW @NAJIBRAZAK\nSHOT 1/4 @JHOLOW Man walking...\nSHOT 2/4 @NAJIBRAZAK Man signing..."
  This helps AI understand which locked asset appears in which shot.

- [2026-07-23] CRITICAL: Trust user's manual chunk corrections — When user corrects chunk timing or narration, accept it immediately. User knows the correct sync. Do not argue or re-parse SRT.

- [2026-07-23] CRITICAL: Work in batches of 4 chunks — After each batch, wait for "done" before next batch. User approves before continuing.

- [2026-07-23] CRITICAL: Final Correction Phase — After all chunks are generated, user reviews and identifies AI slop/mistakes. User provides small clips that need regeneration. Regenerate with MAX 2-3 shots per clip. These are short correction clips, not full chunks. Wait for user to provide the problematic segments.

- [2026-07-23] CRITICAL: Read FULL script before generating prompts — Don't just look at the chunk. Read the surrounding context to understand what's happening. Many mistakes come from not understanding the full scene.

- [2026-07-23] CRITICAL: Tag EVERY shot in video prompt — Don't forget to tag the specific asset in each shot where it appears. Not just at beginning, but in each SHOT line.

- [2026-07-23] CRITICAL: Leonardo DiCaprio — Not locked as asset, but user uses his online pictures. Tag as @DICAPRIO when he appears in shots.

- [2026-07-23] CRITICAL: Subscribe/CTA reminders — NEVER show people talking, saying bye, or asking to subscribe. That looks silly. Instead use: logos, graphic animations, phone screens showing channel, comment sections scrolling, real devices. Visual graphics only for CTAs, not people speaking.

- [2026-07-23] CRITICAL: NO floating papers, floating objects, floating text — This is AI slop. Papers should be stacked, held, or on desks. Never floating in air. Money should be in counting machines, stacks on tables, or in hands — never floating.

- [2026-07-23] CRITICAL: Money shots — Use steady slow movement: money counting machines running, stacks of cash on tables, bills being counted by hand. NEVER floating money, flying bills, or chaotic money movement. Keep it grounded and realistic.

- [2026-07-23] AI SLOP PATTERNS — NEVER do these again:
  1. "papers flying through air" — Papers should be stacked, held, on desks, or being read. Never flying.
  2. "papers exploding outward from desk" — Never exploding. Papers stay on surfaces.
  3. "calendar pages flying off" — Calendar should be static, hand-flipping, or Ken Burns on static. Never pages flying.
  4. "money flying through fingers" — Money should be in counting machines, stacks, or hands. Never flying through fingers.
  5. "money flowing across screen" — Money stays physical. Counting machines, stacks, hands. Not digital flowing.
  6. "person waving goodbye" — For closing, use graphics/logo. Never person waving.
  7. "person talking/saying subscribe" — CTAs use graphics, phone screens, logos. Never people speaking.
  8. "Talking head for narrator moments" — Use atmospheric visuals, not person looking at camera.

- [2026-07-23] CRITICAL: Tag only where asset APPEARS — If character/location is NOT visible in start frame, do NOT tag them in start frame. Only tag them in the specific SHOT in video prompt where they actually appear. Start frame tags = only assets visible in that image.

- [2026-07-23] CRITICAL: Video prompt tag format — After "Use @image1 as visual anchor for start frame." list ALL tags that appear ANYWHERE in the shots. Then tag each specific asset in its SHOT line. Example: "@TAG1 @TAG2\nSHOT 1/4 @TAG1 ...\nSHOT 2/4 @TAG2 ..."

- [2026-07-23] CRITICAL: Subscribe/CTA — Use @channellogo tag for channel logo in first frame when CTA appears. User will add the logo image. Tag tells user which asset to add.

- [2026-07-21] CRITICAL: Pipeline Engineer Approach — Every video prompt MUST follow this workflow:
  1. Clip Math & VO Breakdown FIRST — map every word of narration to a visual shot
  2. Every distinct action or phrase = at least one unique visual shot
  3. Do NOT summarize or group narrative — word-by-word mapping
  4. Ensure every word in script is visually represented
  5. Use 4-Layer Prompt Build for each shot:
     - Subject & Action (what/who is happening)
     - Camera & Motion (angle, movement, handheld/dolly/pan)
     - Lens & Light (35-50mm, golden hour, practical glow, haze)
     - Texture & Mood (film grain, halation, soft grade, shoulder rig look)
  6. Active scenes only — people doing things, not camera wandering
  7. Creative transitions between chunks
  8. Visual variety — never repeat camera movements, body movements, or angles
  9. Scene composition — place camera behind objects, integrate into crowd, add environmental activity
  10. Word count to shot count: 2-5 words=2 shots, 6-12 words=3 shots, 13-20 words=4 shots, 20-30+=split into 2 scenes with 4 shots each

## MiMo Architecture (Laptop)
- Config: .config/mimocode/mimocode.json → "plugin": ["./plugins/local-workspace.js"]
- Plugin: .config/mimocode/plugins/local-workspace.js (ESM export default)
- Flow: mimo.exe → reads mimocode.json → imports plugin → registers "local" adaptor
- Workspace adaptor resolution: PU map (plugins) → Ec map (built-in) → error if not found
- Restart required after plugin changes


