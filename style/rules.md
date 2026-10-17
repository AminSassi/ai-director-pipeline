# Visual Style & Aesthetic Rules

Core visual direction rules for **Verion** and **Insolvent** documentary productions.

---

## 1. Signature Documentary Aesthetic (Frontline / Fincher Realism)

- **Grounded 35mm / 50mm Photorealism:** Natural architectural lighting, practical tungsten lamps, sodium vapor street/harbor lights, overcast daylight, and clinical fluorescent interiors.
- **Zero Sci-Fi / Cyberpunk Slop (Rule #25):** Strictly NO neon blue LED ambient glow, floating holograms, curved sci-fi command consoles, or futuristic sets. Server rooms must be matte-black steel enterprise racks with perforated mesh doors.
- **Domain-Specific Color Palettes:**
  - *Corporate / Financial Fraud:* Cold slate blue, deep walnut shadows, warm brass practical lamps, muted monochrome contrast.
  - *Industrial / Maritime / Automotive:* Sodium-vapor amber, damp asphalt charcoal, high-bay metal halide industrial lighting, cold coastal mist.
  - *Geopolitical / State Secrecy / Medical:* Austere concrete greys, muted seafoam green corridors, high-contrast chiaroscuro shadows, clinical teal.
- **Film Texture:** Subtle 35mm analog film grain, natural optical depth of field, zero plastic airbrushing.

---

## 2. The 4-Layer Shot Architecture (Grok Imagine & Nano Banana 2)

Every Start Frame AND every individual Video Shot line (`SHOT 1` through `SHOT 4/6`) must contain all 4 layers:

1. **Subject & Action:** Living character in grounded gross-motor motion (or monumental real-world infrastructure). *Never posed, never using fine hand tools/pens/stamps/keyboards.*
2. **Camera & Motion:** Explicit framing archetype + movement from `camera/angles.md`.
3. **Lens & Light:** Focal length (`24mm`/`35mm`/`50mm`) + lighting direction/contrast.
4. **Texture & Mood:** Film grain, atmospheric haze, emotional tension.

> **CRITICAL FOR SHOTS 2–6:** Because Shots 2–6 cut away from the Start Frame (`@image1`), every shot line must retain a compact 4–6 word style anchor (e.g., `35mm lens, chiaroscuro shadows, film grain`) so Grok never drops the photographic grade into flat CGI on cuts.

---

## 3. High-End Slop-Free Motion Graphics & Explainers (Rule #38)

When visualizing mechanisms, flight paths, shell company networks, or timelines, strictly use one of the **Three Slop-Free Aesthetics**:

1. **Tactile Forensic Light-Table:** Physical cyanotype blueprint or dark slate schematic plate lying flat on a backlit wooden drafting lightbox (`crisp white vector linework, millimeter gridlines, 35mm macro lens, top-down orthographic view, smooth macro dolly push`).
2. **Vox Mixed-Media Paper Collage:** Flat matte charcoal (`#0D0E11`) or parchment backdrop, halftone print texture, archival cutouts with clean white paper borders, flat 2D vector route line tracing smoothly.
3. **Orthographic 2D Vector Infographic:** Strictly flat top-down/straight-on 2D geometry, single-axis fluid reveal, zero 3D perspective warping.

**Hard Bans for Explainers:**
- NEVER use `3D CAD wireframe` or `isometric 3D cutaway` keywords.
- NEVER request readable text, words, or numbers inside the clip (all typography is added in Premiere Pro).
- Only ONE simple motion per shot (camera glide OR single vector line trace).

---

## 4. Technical Syntax & Negative Flags

- **Word Count Limit:** Under **35 words per `SHOT` line** (18–28 words optimal).
- **Start Frame Suffix:** `--ar 16:9` (and `--no blur --no watermark --no artifacts --no distortion` when appropriate).
- **Video Prompt Suffix:** Always end with:
  `--ar 16:9 --no text, words, numbers, labels, watermarks, blur, split screen`
- **Zero In-Clip Text:** Never prompt a screen, paper, or sign to display specific English phrases inside a video prompt while passing `--no text`.
