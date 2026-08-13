# Cinematography & AI Generation Rules

These rules represent the accumulated knowledge for generating high-quality, slop-free cinematic video using AI tools (like Nano Banana, Kling, Grok) and must be applied by all agents acting as AI Directors.

## 1. SUBTEXT EXTRACTION (THE GOLDEN RULE)
When generating visual prompts based on a script, **DO NOT write literal captions**. 
If the script says a character is "stressed," do not prompt "a stressed character." 
A director never illustrates the sentence — they find the physical detail or camera choice that carries the feeling.

**Mandatory Interpretation Step:**
Before writing a prompt, silently answer:
1. What is literally stated?
2. What is the emotional/narrative truth underneath?
3. What single physical action, object, or environmental detail shows that truth without restating the words?
4. What camera/lens technique amplifies it?

*Silent Test:* If someone saw the image with no audio, would they feel the emotional truth, or just see a literal caption of the words?

## 2. PREVENTING AI SLOP (CRITICAL)
AI video models hallucinate wildly when overloaded with complex physics or unanchored elements.
- **No Complex Physics:** Never prompt hands manipulating complex objects (e.g., "violently yanking cables"). Keep human motion simple (walking, turning, staring).
- **No Metaphorical Physics:** Do not prompt things "shattering," "melting," or "glitching into blackness." Keep actions literal and basic.
- **UI Macros Must Be Static:** When prompting for extreme close-ups of digital UI, ALWAYS use "Static locked frame" for the camera. Panning/zooming on UI elements melts them into slop.
- **No Text Transformations:** Do not ask the AI to change text/UI colors mid-shot (e.g., "red turns green"). Keep UI states static or use binary actions like a blinking cursor.

## 3. NO UNANCHORED ELEMENTS & ENVIRONMENTS
Do not introduce new objects, people, or entirely new environments in the video prompt that were not explicitly established in the start frame anchor image. 
- If the anchor image is a macro close-up, do NOT ask for a wide shot of a room in the video prompt. 
- If you need a specific environment, establish it in the start frame first.

## 4. ASSET & BACKGROUND CONSISTENCY
- Always cross-reference scene descriptions with locked asset reference sheets. Do not invent new architectural features.
- **Background Hallucinations:** AI generators love duplicating monitors in hacker scenes. Explicitly describe the background to prevent this (e.g., "The wall behind him is plain drywall, absolutely no monitors behind him").

## 5. EDIT-LEVEL TECHNIQUES (MATCH CUTS)
Editing techniques live in post-production (Premiere), not inside a single AI generation. You control them by designing start frames and shot endings to set up the match.
- **Graphic Match:** Mirror the shape/silhouette between Clip A's last frame and Clip B's first frame.
- **Color Match:** Make Clip B's start frame echo the color palette of Clip A's closing frame.
- **Positional Match:** The same subject/object sits in the exact same spot on screen across two unrelated shots.
- **Action Match / J-Cuts / Whip Pans:** Set up the continuity or motion in the prompts, but execute the cut in the edit timeline.
