# Learnings

Accumulated corrections and discoveries from sessions. Updated automatically when the director shares insights.

**Note:** This file contains INSIGHTS only. Hard rules are in `critical-rules.md`. Workflow rules are in `additional-rules.md`.

---

## New entries are appended below this line

- [2026-06-25] INSIGHT: Reflection shots in screens/laptops cause AI to generate weird cloned/duplicated person effects. NEVER use "reflection visible in screen" or similar reflection descriptions. Avoid any shot where character appears inside a reflective surface.

- [2026-06-25] INSIGHT: No super fast camera motion — causes AI artifacts and breaks generation.

- [2026-06-25] INSIGHT: Plastic/humanoid looking characters — specify skin texture, hair detail, clothing wrinkles for realism.

- [2026-06-25] INSIGHT: Before EVERY prompt generation, re-read the full GitHub repo rules even after long breaks. User requires this.

- [2026-06-25] INSIGHT: "Stamp being pressed" causes AI to spawn stamp from nowhere, oversized. AVOID stamp/stamping actions — use signing, writing, or other hand actions instead.

- [2026-06-25] INSIGHT: When describing hacker at screens, specify "figure facing screens, back to camera" or "figure's back visible, screens ahead" — otherwise AI puts screens facing viewer instead of character.

- [2026-06-25] INSIGHT: Doors in AI video are unreliable — they open/close spontaneously, multiply, or behave weirdly. AVOID door shots entirely or use extreme close-up of handle only.

- [2026-06-25] INSIGHT: Over-describing details in video prompts causes Grok to hallucinate trying to follow everything. Keep video prompts SHORT with only essential realism and story details. Less is more.

- [2026-06-25] INSIGHT: "Torn paper style" — when user asks for this, use: Aged paper texture background, black and white photograph style, bold typewriter font, aged sepia and greyscale tones, film grain texture, high contrast shadows, investigative documentary thumbnail style, 4K, --ar 16:9, --no blur --no watermark --no artifacts --no distortion --no photorealism. Photo should look like printed article clipping with white border around image.

- [2026-07-23] INSIGHT: YouTube Thumbnail Style — Documentary Collage Aesthetic:
  1. Black and white photograph of main subject (person)
  2. Red color accent on clothing or design elements
  3. Bold typography — title in large text
  4. Subtitle/description text below title
  5. Collage elements in background (related imagery)
  6. Red geometric shapes/lines as design overlays
  7. Aged paper/document texture background
  8. Grid patterns, handwritten elements
  9. Circular design elements
  10. Gritty, investigative documentary feel

- [2026-06-25] INSIGHT: Locked Assets Workflow — Before generating prompts, identify ALL recurring characters, locations, objects that appear more than once. Create reference sheet prompts for each FIRST. Generate and lock them. Then use them in all future prompts as "same [character/location/object]". Ensures visual consistency throughout.

## LOCKED ASSET TEMPLATES (USE THESE)

### CHARACTER REFERENCE SHEET TEMPLATE
```
@ [CHARACTER NAME]
Professional character reference sheet, technical model turnaround style, clean neutral plain background, photorealistic. [CHARACTER DESCRIPTION]. Two horizontal rows. Top row: four full-body standing views — front view, left profile view facing left, right profile view facing right, back view. Bottom row: three close-up portraits — front portrait, left profile portrait facing left, right profile portrait facing right. Relaxed A-pose, consistent scale, accurate anatomy, clear silhouette, even spacing, uniform framing, consistent head height and facial scale across all panels. Same direction intensity and softness lighting across all panels, natural controlled shadows. Canon SL3, 17-85mm lens, fine pores, DSLR photography look, no airbrush, no CGI retouch, no text overlays. Landscape 16:9 -no white background or white bars
```

### LOCATION REFERENCE SHEET TEMPLATE
```
@ [LOCATION NAME]
Professional location reference sheet, full-frame photographs, no borders, no margins. Arrange into a grid of six views filling entire image: top row — wide establishing shot of [LOCATION 1], medium shot of [LOCATION 2], close detail of [LOCATION 3]. Bottom row — aerial view of [LOCATION 4], [LOCATION 5], [LOCATION 6]. Each photo fills its panel completely, no white space, no grey background. [LOCATION IDENTITY DESCRIPTION]. Natural lighting, photorealistic, Canon SL3, 17-85mm lens. No text overlays. Landscape 16:9
```

- [2026-06-25] INSIGHT: Video prompts use SHOT 1/2/3/4 format. Each shot = 1 camera angle + 1 action. No more than 4 shots per 10-second clip.

- [2026-06-25] INSIGHT: Grok "expand video" feature extends from last frame — use for scene transitions. Start frame + expand = seamless continuation.

- [2026-06-25] INSIGHT: YouTube workflow — 1 long video + 3 shorts. Long video gets 3 title options for A/B testing + description + tags. Each short gets its own title, all shorts share same description and tags.

- [2026-06-25] INSIGHT: Image prompts can be more detailed than video prompts. Video prompts should be SHORT to avoid hallucination. Image = detailed scene setting, Video = simple action beats.

- [2026-06-25] INSIGHT: Brand names (iPhone, Sony, Google, Facebook, etc.) can get flagged by AI generators — describe concepts without naming brands when possible.

- [2026-06-25] INSIGHT: Thumbnail prompts with "dark room", "film grain", "harsh lighting" can make user's photo look too dark and unclear. For personal photos/video stills, use "bright", "well-lit", "natural lighting", "clear face visible" to keep subject bright while black space stays dark.

- [2026-07-17] INSIGHT: NEVER use generic noir tropes (rain-soaked streets, silhouettes at windows, detective aesthetics) — stay grounded in the ACTUAL story setting.

- [2026-07-17] INSIGHT: NEVER do same first frame, same plan, same angle, same idea across chunks. Always introduce new visual approaches. Repetition kills creativity and wastes credits.

- [2026-07-17] INSIGHT: "Open parentheses" = Seedance 2.0 mode. "Close parentheses" = Grok/Kling mode. Switch between them as director instructs.

- [2026-07-17] INSIGHT: Always include script text before each chunk prompt so director can verify sync.

- [2026-07-17] INSIGHT: Always re-read repo files before starting prompt generation — director requires this every session.

- [2026-07-17] INSIGHT: Push changes to GitHub immediately after saving to learnings.md — director uses multiple PCs and needs synced repo.

- [2026-07-23] INSIGHT: Leonardo DiCaprio — Not locked as asset, but user uses his online pictures. Tag as @DICAPRIO when he appears in shots.

- [2026-07-23] AI SLOP PATTERNS — NEVER do these again:
  1. "papers flying through air" — Papers should be stacked, held, on desks, or being read. Never flying.
  2. "papers exploding outward from desk" — Never exploding. Papers stay on surfaces.
  3. "calendar pages flying off" — Calendar should be static, hand-flipping, or Ken Burns on static. Never pages flying.
  4. "money flying through fingers" — Money should be in counting machines, stacks, or hands. Never flying through fingers.
  5. "money flowing across screen" — Money stays physical. Counting machines, stacks, hands. Not digital flowing.
  6. "person waving goodbye" — For closing, use graphics/logo. Never person waving.
  7. "person talking/saying subscribe" — CTAs use graphics, phone screens, logos. Never people speaking.
  8. "Talking head for narrator moments" — Use atmospheric visuals, not person looking at camera.

- [2026-07-23] CRITICAL: MiMo UI has rendering bug where text appears without spaces. NEVER type long text (descriptions, tags, metadata) directly in chat. ALWAYS write to file on Desktop first, then tell user to copy-paste from file. This is permanent — no fix possible from our side.

- [2026-07-24] STYLE: ElevenLabs VO target is 1400 words — NOT the compressed script. The 1400-word target applies to the spoken narration text only (Phase 0.4), not the full script with visual directions (Phase 0.3). Always verify word count of ElevenLabs version specifically.

- [2026-07-24] STYLE: Self-Review After Every Prompt — After generating each prompt, review against these checks:
  1. Are characters MID-ACTION (never posed)?
  2. Is there at least ONE creative angle?
  3. Are there at least 3 different camera movements across the 4 shots?
  4. Is every word of narration visually represented?
  5. Are scenes ALIVE with action (not camera wandering)?
  6. Is there visual variety (no repeated angles/movements)?
  7. Does each shot have Subject & Action, Camera & Motion, Lens & Light, Texture & Mood?
  8. Are characters caught mid-action (not static)?
  9. Is scene composition interesting (behind objects, in crowd, environmental activity)?
   10. Would you freeze this frame and see implied motion? If yes = correct.

- [2026-07-25] INSIGHT: ALWAYS paste the final ElevenLabs script (Phase 0.4) directly in chat for the director after creating it. Never just save to file. Director needs it copy-paste ready immediately. This is a permanent workflow rule.

- [2026-07-25] INSIGHT: Pipeline order is: ElevenLabs → Suno Prompt → [WAIT FOR .vst] → Chunks. Suno prompt comes AFTER ElevenLabs but BEFORE the VST timing file. Never skip Suno prompt.

- [2026-07-25] INSIGHT: Suno prompt for Danske Bank — user said first version sounded like "someone crashing something and annoying high hertz noise at start with nothing special." Avoid: high-pitched tones, chaotic crashes, glitchy interference at opening. Keep it clean, cinematic, slow-building tension.

- [2026-07-25] CRITICAL: NEVER touch the VST file. Director gives it already split into 10-second chunks. Just USE it as-is. Do NOT modify, re-split, re-parse, or touch it in any way. No separate chunks file needed. VST IS the chunks. This is permanent.

- [2026-07-25] CRITICAL: ONLY use Grok Imagine for video generation. We no longer use Kling. Remove all Kling references from workflow. Grok = 10 seconds always.

- [2026-07-25] CRITICAL: ALWAYS TAG LOCKED ASSETS. In start frame prompt — tag if asset appears. In video prompt — tag at beginning of prompt AND at start of shot line. Example: "Use @image1 as visual anchor for start frame @AIVAR_REHE." and "SHOT 1/1 @AIVAR_REHE same character walking..." NEVER FORGET THIS.

- [2026-07-25] CRITICAL: ALWAYS 4 SHOTS PER CHUNK. Every 10-second chunk gets 4 shots in the video prompt. Format: SHOT 1/4, SHOT 2/4, SHOT 3/4, SHOT 4/Each shot = 1 camera angle + 1 action. NEVER do less than 4 shots.

- [2026-07-25] CRITICAL: TAG FORMAT RULES:
  1. Start frame: "@TAG description of scene..."
  2. Video prompt header: "Use @image1 as visual anchor for start frame @TAG."
  3. Each shot line: "SHOT X/4 @TAG description..."
  4. Tag goes FIRST in every line where asset appears
  5. Never put tag in middle of description
  6. Even if asset only appears in shot 4, still tag in prompt header- [2026-07-26] CRITICAL UI OVERRIDE: User prefers prompts pasted DIRECTLY IN CHAT, not in files. Format exactly like this: Script text in plain text. START FRAME prompt in its own code block. VIDEO PROMPT in its own separate code block. Do NOT put the script text in a code block.
- [2026-07-26] CRITICAL HALLUCINATION PREVENTION: If a script or file is truncated due to a long conversation, NEVER try to guess, invent, or hallucinate the missing script text based on context. If you do not have the exact script text for the chunks you are currently working on, you MUST stop immediately and ask the user to provide the script again or read it from a saved file.

- [2026-07-30] INSIGHT: VISUAL TONE & VIBE. NEVER make chaotic scenes with people running, fighting, screaming, or frantic crowds. "Weird/special" angles should mean BEAUTIFUL, ELEGANT, visually stunning cinematography. Build tension through absolute stillness, isolation, deep shadows, and stark composition. Scenes should be alive with deliberate, elegant action (typing, turning a page, adjusting a tie), not wandering cameras and not chaotic slop.

- [2026-07-30] INSIGHT: PRE-GENERATION AUDIT CRONJOB. Before outputting any batch of prompts to the director, the AI MUST explicitly print a "Pre-Generation Audit Cronjob" block. The AI must draft the prompts in memory, review them against the Creativity & Beauty rules, CORRECT any clichés or bad angles, and document what it changed in the chat *before* printing the final prompts. A Post-Generation Audit summary must also be printed after the batch.

- [2026-07-31] CRITICAL: NEVER use the generate_image tool. Director wants PROMPTS ONLY — always plain text prompts ready to copy-paste into Grok/Nano Banana. Never auto-generate anything. This is permanent.

