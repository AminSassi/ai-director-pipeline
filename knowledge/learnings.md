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
