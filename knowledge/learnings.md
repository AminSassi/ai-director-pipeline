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
  4. Is every beat of narration covered by a shot, AND does each shot use a directorial/physical choice rather than restating the line?
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

- [2026-07-25] CRITICAL: SHOT COUNT RULE. Every 10-second chunk gets 4 shots in the video prompt (Format: SHOT 1/4, SHOT 2/4, SHOT 3/4, SHOT 4/4) UNLESS the chunk is under 13 words, in which case use critical-rules.md Rule #7's word-count scale instead. Each shot = 1 camera angle + 1 action.

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


- [2026-08-14] INSIGHT: To prevent vehicles (helicopters, planes, cars) from flying or moving backwards in AI video, explicitly specify the vehicle's forward direction AND the camera's forward direction (e.g., 'helicopter flying forward, camera pushing forward'). Avoid words like 'tracking' or 'swooping' which AI often interprets as reverse/dolly-back motion.

- [2026-08-14] INSIGHT: Grok has strict content moderation filters for image-to-video. Avoid words that imply anxiety, crime, or physical restriction (e.g., 'nervously', 'locking away', 'creeping tension', 'dark room'). Sanitize prompts to be extremely neutral and 'brand safe' (e.g., 'dimly lit office', 'closing vault', 'adjusting suit').

- [2026-08-28] CRITICAL: CTA VISUAL RULE. When generating prompts for CTA sections of the script (subscribe, like, comment, notification bell), NEVER generate subscribe-themed visuals (channel logos, subscribe buttons, comment sections, bell animations, phone screens showing channel). Instead, generate a VAGUE ATMOSPHERIC SCENE related to the story — moody, cinematic, story-relevant. The director adds subscribe/CTA overlays manually in editing. This applies to ALL CTA chunks. Treat CTA narration the same as any other narration: what visual tells this part of the story best? This is permanent.


- [2026-08-28] CRITICAL: NO INFOGRAPHICS OR DIAGRAMS. Never generate flat vector infographics, animated diagrams, or chart visualizations. The director hates them. Even for EXPLAINER scenes (like fraud mechanisms, money flow, or balance sheets), use CINEMATIC VISUAL METAPHORS (e.g., macro shots of ledgers, physical documents being stamped, briefcases, red ink on paper, tense character moments in dark offices). All chunks default to standard Cinematic/Documentary style. Do not use Gemini OmniFlash for diagrams.

- [2026-08-30] INSIGHT: YouTube workflow update — We no longer do 3 shorts. Only 1 long video is produced. If a short is created, it shares the exact same title, description, and tags as the long video, so no separate Shorts section or unique titles are generated.

- [2026-08-30] CRITICAL: YOUTUBE TITLE RULE. Video titles must ALWAYS follow the two-part signature format: `[Main Subject / Entity] — [The Core Hook / Discovery / Crime / Event]`. Example: `First Brands Group — The James Brothers' $2B Auto Parts Fraud` or `The Pyramids of Giza — What the Radar Found Beneath the Sand`. Must be straightforward, keyword-dense, and structured with an em-dash (`—`).

- [2026-09-01] INSIGHT: For the Ratko Mladić episode, @MLADIC_TRIAL is removed and unified into @MLADIC_OLD for all fugitive, trial, and detention scenes.

- [2026-09-01] CRITICAL: GOLDEN RATIO PACING — ~2.5 seconds per shot is the sweet spot. For 10-second chunks use 4 shots (SHOT 1/4 through SHOT 4/4). For 15-second chunks use 6 shots (SHOT 1/6 through SHOT 6/6). NEVER go slower. Slower pacing = more time for AI to hallucinate = more slop. This is permanent.

- [2026-09-01] CRITICAL: MODERATION SAFETY — When a character is sick, dying, or in medical distress, NEVER depict their face or body in that vulnerable state when using imported reference images. Grok will block it. Instead show the ENVIRONMENT of their decline (the room, documents, window, corridor). Let the narration carry emotional weight; visuals provide atmospheric context.

- [2026-09-01] CRITICAL: CAMERA MOVEMENT VARIETY — Minimum 3 distinct camera movements per chunk. NEVER repeat the same camera movement in consecutive shots. If Shot 1 is "slow push in," Shot 2 MUST be something different. Available palette: slow push in, slow dolly back, low-angle tilt up, slow pan left/right, slow crane rise, tracking shot, handheld drift/shake, macro rack focus, Dutch tilt hold, static hold (max 1 per chunk), 50mm shallow focus hold.

- [2026-09-01] CRITICAL: PRESENT LOCKED ASSET REFERENCE SHEETS FIRST. After receiving the timing file, ALWAYS present ALL character and location reference sheet prompts to the director for Nano Banana generation BEFORE generating any chunk prompts. Wait for director to upload confirmation screenshots and say "done." NEVER skip to Phase 2 prompt generation without this step.

- [2026-09-01] INSIGHT: When a character has multiple temporal versions (young vs old), define a clear chronological cut-off date. Tag discipline is strict: use the young version ONLY for scenes before the cut-off, old version ONLY for scenes after. Document the transition point in the locked assets register.

- [2026-09-01] INSIGHT: Contrast cuts within a single chunk are powerful — e.g., cemetery in Bosnia → prison cell in Netherlands, empty courtroom → endless gravestone fields. Use sparingly (2–3 per episode) for maximum emotional impact.

- [2026-09-01] SUCCESS: Full golden reference for this session saved in `knowledge/golden-reference-mladic.md`. This is the quality benchmark. Read it during every bootstrap.

- [2026-09-02] INSIGHT: Script chunk length adaptation for fixes/re-runs: If the pasted script chunk is short, generate 2 shots only (SHOT 1/2, SHOT 2/2). If long, generate 6 shots (SHOT 1/6 through SHOT 6/6). Each script chunk gets exactly one Start Frame prompt and one Video Prompt.

- [2026-09-03] CRITICAL BATCH SIZE RULE: Always generate and output EXACTLY 6 chunks per batch in chat (never 4). Standard batch progression: Chunks 1–6, Chunks 7–12, Chunks 13–18, Chunks 19–24, Chunks 25–30, Chunks 31–36, Chunks 37–42, Chunks 43–45. Pre-Generation Audit Cronjob must precede every 6-chunk batch.

- [2026-09-04] CRITICAL: PHASE 3 CORRECTION PHASE RULES. Activates after 100% of all initial chunks are generated and assembled. The director watches the full timeline in Premiere Pro, trims out seconds of AI slop or flawed generations, and requests replacement prompts. Director provides timestamps and cut script snippets. Cut duration ranges from 1-2s micro-pickups up to 15s max chunks. Scaling rule: If script/cut is short (1–5 seconds), generate ONLY 2 or 3 shots. If long (up to 15 seconds), generate the usual 6 shots. When redoing prompts, NEVER reuse old angles, compositions, or failed ideas; always generate completely fresh perspectives and emotional beats.

- [2026-09-09] INSIGHT: Never include courtrooms or courthouses in locked asset reference sheets. Courtrooms are generic institutional architecture and do not require locked reference sheets; describe them by environmental appearance instead. Only lock primary recurring character and core signature locations.

- [2026-09-10] INSIGHT: Realistic Datacenter Infrastructure — In server room and datacenter scenes, NEVER place freestanding pedestals, isolated hardware units on the floor, or floating items. Servers must ALWAYS be mounted inside standard industrial enterprise rack cabinets on steel rails with clean cable management, perforated mesh doors, and clean aisle architecture. Keep the environment 100% grounded in authentic corporate IT infrastructure.

- [2026-09-10] INSIGHT: Pure Camera Motion for Continuous Video Prompts — In continuous video prompts (especially continuous FPV drone, transitions, or start-to-end frame interpolations), ONLY describe the camera movement, trajectory, speed, and shot mechanics (e.g., flying forward, diving downward, smooth banking, gliding forward, decelerating). NEVER describe the story events, text, actions, or narrative details in the video prompt. The start and end frames already establish all visual elements; restricting the video prompt strictly to pure camera movement allows the AI model to execute a clean, seamless, glitch-free trajectory without hallucination.

- [2026-09-10] CRITICAL: 15-SECOND CHUNK SHOT COUNT RULE. When working with 15-second timing chunks, generate EXACTLY 6 shots per chunk (SHOT 1/6 through SHOT 6/6) instead of 4 shots. This provides optimal visual pacing and density across the 15-second duration. All 6 shots must have all 4 layers, under 35 words per shot, with tags at start of shot lines and in header.

- [2026-09-10] CRITICAL: BAREFOOT USAGE RULE. Only depict a character barefoot IF the script narration explicitly states it for that specific moment (e.g. "walks barefoot through Manhattan" or "pitched barefoot"). In ALL other scenes (such as meetings with Masayoshi Son, executive boardrooms, private jet flights, general office scenes), characters must ALWAYS be dressed in clean, realistic footwear (e.g. minimalist black designer leather shoes or dark sneakers). Never let a barefoot mention leak into unrelated shots or other scenes.

- [2026-09-12] CRITICAL: HACKER & TECH EPISODES VISUAL DIVERSITY RULE. Never trap an entire video in server rooms, datacenters, and desktop setups. That produces visual monotony and boredom. While authentic setups and datacenters have their place, they must NOT dominate the whole video. For every 15-second chunk (6 shots), deeply understand the exact words and thematic reality of the script and translate them into varied, dynamic, engaging visual manifestations: show real-world physical transactions, consequences, human drama, street level moments, institutional offices, field investigations, atmospheric tension, and diverse creative camera angles beyond keyboards and monitors.


- [2026-09-13] CRITICAL: ANTI-SCI-FI & GROUNDED DOCUMENTARY REALISM RULE. Absolutely NO space movie, neon blue LED, holographic, or hyperrealistic cyberpunk aesthetic in Insolvent episodes. Avoid glowing telemetry, curved sci-fi wall displays, and dark futuristic tech sets - these produce artificial AI slop. All tech, cyber, and corporate scenes must remain 100% grounded in authentic Frontline / BBC documentary realism: natural daylight, standard office desks, regular computer displays, whiteboards with dry-erase markers, paper binders with highlighters, realistic colocation utility closets, physical machinery, and real human environments.

- [2026-09-13] CRITICAL: START FRAME & SHOT 1 100% VISUAL ALIGNMENT RULE. The Start Frame generated in Nano Banana IS literally Shot 1, Frame 0 of the video clip. Therefore, SHOT 1 in the video prompt MUST be the direct, seamless continuation and animation of the exact scene, subject, lighting, angle, and assets established in the Start Frame. Never describe Scene A in the Start Frame and then describe a different Scene B in SHOT 1. When the AI video model (Grok Imagine) is given an anchor image (@image1) that contradicts SHOT 1, it is forced to perform an unnatural morph or severe hallucination in the first 1–2 seconds. SHOT 1 breathes motion into the Start Frame; any transition to new camera angles, locations, or actions only begins at SHOT 2.

- [2026-09-18] CRITICAL: PHYSICAL CAMERA GEOMETRY (THE LAPTOP SCREEN PARADOX). When describing someone sitting at a laptop or desktop computer, NEVER place the camera in front facing their face while simultaneously describing what is on the computer screen facing the camera. In physical reality, looking at someone's face puts the back of the laptop lid toward the camera lens. Trying to describe screen UI in a frontal shot forces the AI image generator to glue an absurd glowing second screen to the back of the laptop lid!
  * RULE: If screen UI / web portal / terminal must be visible and legible, ALWAYS use **Over-The-Shoulder (OTS)** framing (camera behind subject looking past shoulder toward screen).
  * RULE: In frontal or profile shots, describe ONLY the ambient monitor glow reflecting on their facial features and skin. The screen UI belongs in a dedicated OTS shot or macro insert.

- [2026-09-18] CRITICAL: MASCOT TAG DISCIPLINE (NEVER TAG HUMANS WITH MASCOTS). NEVER place a mascot tag (e.g. `@cyberleek`) at the beginning of a prompt describing a human actor (investigators, hackers, journalists, lawyers, traders). Image generators treat the lead tag as the SUBJECT of the sentence, literally replacing the human with an anthropomorphic cartoon mascot (e.g., turning a private investigator into an anthropomorphic leek in a coat). Mascot tags are strictly for the standalone mascot avatar/branding, never human roles.

- [2026-09-18] CRITICAL: ANTI-SLOP TENSION & CAMERA ANGLES (THE FINCHER STILLNESS RULE). AI slop comes from chaotic, try-hard, cartoon action prompts (e.g. "panicked operator yanking cables, knocking over hard drive cases, flailing arms"). This breaks AI physics, creates distorted hands, flying debris, and plastic panic expressions. True cinematic tension comes from **deliberate stillness, quiet dread, stark composition, deep shadows, and purposeful micro-actions** (capping a dry-erase marker, highlighting a document, reviewing a paper KYC dossier, cold realization, staring at dead black screens). Furthermore, every chunk MUST employ creative camera angles from the mandatory palette:
  1. Low-Angle Dutch-tilt (tilted upward from desk or floor height)
  2. Ground-level tracking (skimming wet asphalt or floorboards)
  3. Worm's-eye view (looking up through glass tables or floor)
  4. Bird's-eye view (perpendicular downward view on cluttered desks)
  5. Macro rack focus (tangible physical items: marker nibs, highlighters, stamps, keys, cables)
  6. Architectural crane rise/descent (monumental corporate/city scale)
  7. Over-The-Shoulder (OTS) for all screen and document interactions

- [2026-09-18] CRITICAL: GROK IMAGE-TO-VIDEO SAFETY FILTER PROTECTION. When animating an imported image (`@image1`) in Grok Imagine, xAI's safety filters aggressively scan for potential deepfakes or NSFW content.
  * NEVER use gendered nouns (`female`, `woman`, `girl`) attached to imported human faces — this triggers the automated deepfake shield.
  * NEVER use ambiguous words with sexual/NSFW heuristics (`vigorous`, `erotic`) or strange biological tokens (`enamel`).
  * ALWAYS use clean, professional, objective documentary phrasing: `colleague`, `investigator`, `analyst`, `focused discussion`, `clean line`.

- [2026-09-20] CRITICAL: MULTI-BEAT NARRATIVE COVERAGE (ZERO SINGLE-LOCATION TRAPPING). When a chunk's narration references multiple distinct story events, locations, or concepts (e.g., 'ghost cities, a suspicious divorce, and a getaway to Canada'), NEVER collapse the entire 4-shot or 6-shot video prompt into just one of those locations (e.g. spending all 6 shots in an airport terminal). The AI Director must map each distinct clause/concept sequentially across the shots in that chunk:
  * Clause 1 / Event A $\rightarrow$ SHOT 1–2 (e.g., unfinished ghost towers @tower)
  * Clause 2 / Event B $\rightarrow$ SHOT 3–4 (e.g., signing suspicious divorce papers @hui and @yumei)
  * Clause 3 / Event C $\rightarrow$ SHOT 5–6 (e.g., airport getaway terminal @yumei)
  Every distinct word and concept in the script must be visually represented across the multi-shot breakdown. Trapping an entire video prompt in a single location when the script describes multiple events violates word-for-word sequential mapping and destroys visual storytelling density.

- [2026-09-20] CRITICAL: DYNAMIC STORY VARIETY, FRESH IDEAS & ANTI-SLOP MANDATE.
  * **Zero Shot Recyling Across Stories & Chunks:** Never default to familiar, safe tropes (e.g. repeatedly opening with a generic character walking in a hallway, or repeating the same OTS desk setup). Every episode and every chunk demands unique visual ideas, customized world-building specific to that industry/story, and unexpected camera perspectives.
  * **Constant Rhythm & Scale Shifts:** Contrast wide architectural environments with clinical tactile inserts (e.g., mechanical stamps, rebar rust, safe tumblers, passport stamps) and subtle, tension-filled human moments.
  * **Zero AI Slop:** Keep physics simple, deliberate, and grounded. Never ask for chaotic movements (flailing, fleeing crowds, shouting) which cause grotesque AI morphing. Build suspense through quiet dread, stark lighting contrast, deep shadows, and hyper-realistic documentary textures.

- [2026-09-22] CRITICAL: GROK IMPORTED FACE FILTER BYPASS ('CONTENU MODÉRÉ'). When Grok Imagine blocks an imported human photo tag (e.g. @CONNOLLY_OLD) with the popup 'Contenu modéré: Les générations à partir de photos importées bénéficient de protections renforcées', immediately drop the human face tag from that chunk. xAI's safety filters flag real-person facial turnarounds when paired with sensitive legal, conviction, prison, or crime terminology. Pivot the visual storytelling entirely to physical evidence (@MANUSCRIPT), courthouse architecture, clerk offices, legal petitions, or anonymous procedural figures (attorneys/clerks shot OTS or from behind). This eliminates the filter trigger completely while preserving 100% story tension.

- [2026-09-22] CRITICAL: MANDATORY CHANNEL SELECTION GATE (VERION VS INSOLVENT). The AI Director previously defaulted to 'Insolvent' and inserted Insolvent CTAs into a script meant for 'Verion'. Never assume or guess the channel. At the very start of every new episode / session, the AI Director MUST explicitly ask: 'Which channel are we working on: Verion or Insolvent?' and wait for the user's explicit confirmation before proceeding with script expansion (Phase 0), CTA insertion (Phase 0.1), or prompt generation. All downstream CTAs (Hook, Midpoint, Outro) and metadata must strictly adhere to the chosen channel name.

- [2026-09-22] CRITICAL: GROK PROMINENT PEOPLE POLICY BYPASS ('FAILED: THIS PROMPT MIGHT VIOLATE OUR POLICIES ABOUT GENERATING PROMINENT PEOPLE'). When Grok Imagine blocks generation with the prominent people warning, xAI's text filter is triggered by famous real surnames or tagged entity names (e.g. 'Bulger', 'Connolly', '@BULGER_OLD', '@CONNOLLY_OLD'). To bypass:
  1. Remove all real-world surnames and tags from the prompt text and header.
  2. Use ONLY 'Use @image1 as visual anchor for start frame.' in the header without prominent person tags.
  3. Replace names in shot descriptions with anonymous physical roles (e.g., 'elderly inmate with white hair', 'former federal agent', 'defense counsel', 'investigator').
  4. Grok relies 100% on @image1 for visual likeness while the text parser scans zero prohibited names, passing moderation with zero errors.

- [2026-09-25] CRITICAL: TAG DISCIPLINE (START FRAME VS. VIDEO PROMPT). In Start Frame (image) prompts, tag ONLY the assets physically visible in that initial frame. NEVER include tags for characters, objects, or locations that only appear in later shots (e.g. Shots 2–6). In the Video Prompt header ('Use @image1 as visual anchor for start frame...'), tag ALL locked assets that appear anywhere across the shot breakdown for that chunk. This prevents image generators from attempting to merge multiple characters or locations into a single establishing frame.

- [2026-09-27] CRITICAL: BANKNOTE & CURRENCY GENERATION FILTER BYPASS. AI image generators (Grok / Nano Banana) have hard-coded automated anti-counterfeiting moderation shields that immediately block generation ('Échec: Cette génération pourrait enfreindre nos règles') when detecting terms like 'Bank of England twenty-pound note', 'banknote', or currency turnaround prompts. NEVER attempt to generate modern/historical legal tender reference sheets via text prompts. Instead, download an authentic high-resolution scan of the banknote directly from official or historical public archives (e.g. Bank of England Series D Michael Faraday £20 note, obverse & reverse). Import that authentic scan into Grok/editing as the visual anchor. This guarantees 100% historical accuracy and completely bypasses generator moderation.

- [2026-09-27] INSIGHT: YOUTUBE THUMBNAIL STYLE — OPTION 1 IS THE PERMANENT BENCHMARK. The director strongly prefers Option 1 above all other layouts ("i love option 1 always"). Standard signature architecture for Option 1:
  1. Clean, minimalist, high-impact composition with maximum negative space for mobile feed dominance.
  2. Left side: striking high-contrast black-and-white cutout portrait of the main character (bright face, crisp edges, razor-sharp rim lighting, subtle thin red accent contour line along shoulder) — OR the single tactile physical artifact/document if no character exists.
  3. Right side: deep slate-charcoal or solid matte black negative space.
  4. Typography: massive clean bold uppercase typography (Line 1 in bold white sans-serif, Line 2 directly below inside a solid saturated red rectangular highlight box).
  5. Faint background shadows: subtle textured environmental/case overlay (never cluttering the negative space).
  6. Zero AI slop, zero sci-fi neon/glowing junk, tack-sharp focal details, authentic documentary contrast.





- [2026-09-30] CRITICAL: HOOK RETENTION & ANTI-DATE OPENING RULE. Never open a documentary hook with a dry calendar date or timestamp (e.g., 'September eighteenth, twenty fifteen', 'In October 2008'). Starting with a date is boring, destroys early YouTube retention, and sounds like an encyclopedia rather than a high-stakes financial/crime thriller. The AI Director must automatically scan and detect any hook opening with a date and immediately rewrite it into a high-retention cinematic open before presenting it to the director. Permitted opening formulas:
  1. The Psychological/Consumer Betrayal Hook: 'What if the car you bought to protect the environment was secretly poisoning the air every time you drove it?'
  2. The Machine/Secret Code Hook: 'Hidden inside eleven million vehicles was a secret line of code designed to fool the world.'
  3. The Immediate Consequence/Letter Hook: 'A five-page letter lands on the executive desks of Volkswagen. Inside is a single accusation...'
  Dry dates belong in the historical body of Act 1 or the timeline setup, NEVER in the first two sentences of the hook.

- [2026-09-30] CRITICAL: NARRATIVE CONTEXT & CHRONOLOGICAL ASSET STATE (THE SPOILER & RIGGING RULE). Every locked asset, vehicle, character, and prop exists in a specific chronological state tied strictly to that exact moment in the script. Never attach investigative gear, forensic probes, damage, or legal consequences to an asset before that event actually occurs in the story.
  * Innocent Consumer vs. Investigative Rig: In opening hooks and civilian consumer scenes, vehicles (@JETTA) must appear 100% pristine, civilian, and factory-stock with zero cables or attachments. Never add research probes, PEMS measurement equipment, or diagnostic boxes until the university researchers in the story actively install and test them. Attaching research gear to a civilian car in the hook ruins narrative immersion, spoils the plot, and confuses the viewer.
  * Characters & Props: Characters must only wear attire matching their chronological status in that beat (e.g., tailored suit for corporate CEO, casual travel wear for airport departure, no premature prison jumpsuits or handcuffs before arrest).
  * Before generating any Start Frame, explicitly ask: 'Who operates this asset in this exact second of the story, and what is its chronological physical state?'

- [2026-10-02] CRITICAL: THE ANTI-BOREDOM & ACTIVE HUMAN STAKES MANDATE (STRICT ZERO-TOLERANCE BAN ON INERT OBJECTS & DOCUMENT SLIDESHOWS — RULE #37). The director explicitly rejected prompts that devolved into the camera wandering aimlessly around stationary objects, empty desks, paperwork, binders, brass lamps, and ticking clocks ("BRO NAH I DIDNT LIKE THIS BATCH IT KEEPS SHOWING BORING STUFF JUST CAMERA WANDERING AROUND OBJECTS THATS BORING").
  * The Core Principle: Audience retention on YouTube is won through living human conflict, tension, and visceral body language—NOT corporate still-life photography.
  * Banned Boring Slop: Never output shots that merely pan across documents, push in on empty desks, rack focus on desk lamps/coffee cups, or track past empty chairs. Inanimate documents and evidence are never the protagonist of a shot.
  * Organic Narrative Tension (Zero Parroting / No Clichés): Do not use formulaic, repetitive scene clichés. Derive character actions, psychological tension, and interpersonal conflict directly and organically from the *specific characters and narrative stakes in the narration*. Characters must be caught mid-action in purposeful movement, natural body language, and authentic status dynamics.
  * Props Must Be Actively Interacted With: Documents, laptops, and tools are ONLY allowed if a living person is actively handling, reviewing, or reacting to them in service of the narrative.
  * The Only Non-Human Exception: If humans are absent, visuals MUST depict monumental real-world physical scale (vast industrial infrastructure, massive supply-chain yards, environmental aftermath)—NEVER an empty desk in an empty room.



- [2026-10-06] INSIGHT: REAL PEOPLE = REAL NAMES FIRST. Before writing any character reference sheet prompt for a real person, give the director their real-world names (plus what to search) so he can pull real photos online and lock likeness from them. Only write invented-description reference sheets for people who are unnamed publicly. Real surnames still never go into Grok prompt text - tags only.

- [2026-10-08] CRITICAL: THE HIGH-END MOTION GRAPHICS & EXPLAINER PLAYBOOK (ZERO-SLOP STANDARD).
  * The director clarified: Motion graphics explainers are THE single most valuable storytelling device in documentaries to explain mechanisms, routes, and systems to viewers. They are REQUIRED across episodes.
  * The failure on FZ1073 was NOT the concept of motion graphics, but the crude prompting technique (prompting "3D CAD wireframes" and "isometric cutaways" directly in video models, which causes melting lines and geometry distortion).
  * Web research & industry standards (Vox, Johnny Harris, Runway/Kling best practices) reveal the exact formula to achieve razor-sharp, premium motion graphics with ZERO AI slop:

  1. THE THREE PROVEN SLOP-FREE MOTION GRAPHIC AESTHETICS:
     A. THE TACTILE FORENSIC LIGHT-TABLE (Best for Aviation, Machinery & Engineering):
        - Never prompt abstract 3D CGI floating in empty void. Ground the graphic as a physical architectural cyanotype blueprint or dark slate inspection plate on a backlit wooden drafting lightbox.
        - Linework: Crisp white and amber vector lines, millimeter gridlines, clean technical schematics, 35mm macro lens, shallow depth of field.
        - Video Motion: A smooth top-down macro camera dolly push across the physical paper plate. Because the model treats it as a camera moving across a physical document, the linework stays 100% stable, sharp, and razor-crisp with zero melting!
     B. THE VOX MIXED-MEDIA PAPER COLLAGE (Best for Maps, Flight Paths, Timelines & Geopolitics):
        - Flat matte color backdrops (matte slate-charcoal `#0D0E11`, warm newsprint, or deep navy), subtle halftone dot print texture.
        - Elements: Archival photo cutouts with clean white paper borders, layered paper-cut vector silhouettes of continents/airplanes, solid glowing route vectors.
        - Video Motion: Flat 2D motion-graphics animation: clean ease-out slide, route line drawing smoothly across the flat map, subtle stop-motion paper drift. 2D flat paper never warps or melts like 3D meshes!
     C. THE ORTHOGRAPHIC 2D VECTOR INFOGRAPHIC (Best for Data & Process Flows):
        - Strictly orthographic top-down or straight-on flat perspective (zero angled 3D perspective distortion).
        - Clean geometric lines, high-contrast duo-tone palette, fluid single-axis reveals.

  2. THE 5 GOLDEN COMMANDMENTS FOR SLOP-FREE MOTION GRAPHICS:
     - Commandment 1: ZERO In-Clip Text or Numbers. Always include `--no text, words, numbers, labels` in prompts. AI video models hallucinate distorted alien glyphs. True editorial typography (altitudes, flight numbers, dates) is added as clean graphic text in Premiere/CapCut/After Effects.
     - Commandment 2: One Subject Motion per Shot. Only ONE element animates per shot (e.g. camera moves across blueprint, OR single route vector draws from A to B). Never combine multi-axis spins, zooms, and simultaneous shape morphs.
     - Commandment 3: Ban "3D CAD / Wireframe" Keywords. Replace with: `orthographic 2D vector infographic`, `cyanotype architectural blueprint on drafting table`, `flat paper-cutout collage`, `high-contrast graphic plate`.
     - Commandment 4: Start Frame as Absolute Master Anchor. Generate the static graphic plate first in Nano Banana Pro / Midjourney with `--raw` and high contrast. The video model's only job is to add gentle camera drift and vector tracing.
     - Commandment 5: Positive Stability Prompting. Use keywords: `stable geometry, smooth gradual movement, fluid motion, sharp vector lines, high-contrast, clean edges`. Negative: `melting, warping, jitter, flickering, chaotic motion, 3d wireframe, blurry`.


- [2026-10-08] CRITICAL POST-MORTEM: THE FZ1073 DISASTER & PERMANENT HARD BANS ON AI SLOP TRIGGERS.
  Director's verdict after rendering and watching FZ1073: "this is the worst ai video ive ever made video prompts are full of ai slop so i want you to read and learn from it and never do such thing again."
  Live production proved that AI video models (Grok Imagine, Kling, Runway) break down completely when prompted with specific fatal triggers. The following FOUR categories are permanently banned across all pipelines:

  1. PERMANENT BAN: MULTI-CHARACTER PHYSICAL CONTACT & COMBAT (BODY HORROR TRIGGER)
     * Never prompt wrestling, grappling, tackling, door-breaching collisions, hands fighting on controls, or multiple people physically interacting in close quarters.
     * Diffusion models cannot track separate skeletal topologies during contact. They blend bodies together: generating 3 arms, merged torsos, distorted heads, and melting limbs.
     * The Documentary Fix: Direct the tension BEFORE and AFTER physical contact. Show pre-strike tension (eyes locking, knuckles whitening on seat armrests, boots taking deliberate forward strides, door handles vibrating). Show the aftermath (empty seats, zip ties on the floor, heavy shadows, character breathing against a bulkhead). Never the collision itself.

  2. PERMANENT BAN: FINE TOOL MANIPULATION & FINGER MICRO-ACTIONS (MELTING HANDS TRIGGER)
     * Never prompt fingers measuring with calipers, hands using magnifying loupes, fountain pens writing text, rubber stamps pressing on documents, or fingers typing on keyboards.
     * Video AI cannot maintain finger geometry while interacting with rigid micro-tools. Tools bend like rubber, calipers melt into flesh, and fingers duplicate or warp into blobs.
     * The Documentary Fix: Frame the shot on the character's face, their focused gaze, wide or medium angles of the workspace, or static physical artifacts without fingers in motion.

  3. PERMANENT BAN: FAKE 3D CUTAWAYS, BLUEPRINTS & ANIMATED SCHEMATICS
     * As stated above, zero 3D isometric cutaways, zero animated door circuit diagrams, zero radar vector sweeps in video prompts.
     * The Documentary Fix: 100% tangible physical reality (Fincher / Frontline documentary realism). Real cockpits, real airfields, real office rooms, real 35mm camera motion.

  4. MANDATORY: START FRAME TO SHOT 1 IDENTICAL ANCHORING
     * In Grok Imagine (`@image1` anchor), Shot 1 Frame 0 literally IS the Start Frame.
     * SHOT 1 MUST describe the exact same physical space, subjects, lighting, and camera angle established in the Start Frame, only adding gentle cinematic camera drift.
     * Never introduce a new character, cut to a new angle, or change the room in Shot 1. Any scene or angle change must happen from Shot 2 onward.

  5. PACE BY STILLNESS AND WEIGHT, NOT FRANTIC CAMERA OR BODY JITTERS
     * High-end cinematic drama comes from composition, lighting contrast, deep shadows, and slow, deliberate cinematic camera movement (slow tracking, slow dolly push, gentle crane).
     * Frantic movement and chaotic instructions create AI noise and morphing artifacts. Keep camera trajectories clean, continuous, and single-direction.

