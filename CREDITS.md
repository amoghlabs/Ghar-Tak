# Credits & Attributions

## GHAR TAK (Loop Broken)
A 2D HTML5 Canvas endless runner where a college girl walks home through a crowded Indian street.  
Created for the game jam theme: **LOOP**

---

## Game Engine & Code

| Asset | Details | Licence |
|---|---|---|
| Game Engine | 100% original Vanilla JavaScript (ES5/ES6) + HTML5 Canvas 2D API. No external game framework used. | Original work — All rights reserved by the development team. |
| Web Audio Engine | Procedural SFX, music step sequencer, and 3D stereo panning built entirely on the native Web Audio API. | Original work — No third-party audio library used. |
| Voice & Dialogue System | Character dialogue delivered via native Web Speech API (SpeechSynthesis) using system-installed voices. Falls back to procedural blip-talk tones. | Web Speech API — W3C Community Specification. System voices are provided by the user's OS and browser; no third-party voice assets bundled. |

---

## Art & Graphics

| Asset | Details | Licence |
|---|---|---|
| All Sprites & Characters | Every character, obstacle, environment element, pickup icon, and VFX is drawn procedurally at runtime using the HTML5 Canvas 2D drawing API. No external image files are loaded or bundled. | Original work — All rights reserved by the development team. |
| UI Icons (Emoji) | Inline Unicode emoji characters used in HUD labels and tutorial illustrations. Rendered by the user's OS emoji font. | Unicode Standard — Open standard. Specific emoji artwork rendered by the OS/browser font (Noto Emoji, Apple Color Emoji, Segoe UI Emoji, etc.). No custom emoji images bundled. |
| Background / Environment Art | Indian street skyline, road, shop signs, streetlights, and scrolling props are drawn procedurally. All text in shop signs is fictional Hinglish. | Original work — All rights reserved by the development team. |

---

## Fonts & Typography

| Asset | Details | Licence |
|---|---|---|
| UI & Body Font | System font stack: `-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif`. No external font files loaded. | System fonts — Each font is owned by its respective vendor (Apple, Microsoft, Google, etc.) and is pre-installed on the user's device. No licencing required for use via CSS system font stack. |
| Canvas Text Rendering | In-game labels, subtitles, score display, and dialogue text use `ctx.font` with the same system font stack rendered directly onto the Canvas. | Same as above — No external font files. |

---

## Audio & Sound

| Asset | Details | Licence |
|---|---|---|
| Music | Procedurally generated adaptive soundtrack using a step sequencer built on the Web Audio API. Adapts tempo and instrumentation based on game state (day/night, high danger, Speak Up). | Original work — All rights reserved by the development team. |
| Sound Effects | All SFX (footsteps, heartbeat, coin collect, shockwave, coin blips, jump, slide, crash, danger pulse) are synthesised at runtime using oscillators and noise generators via the Web Audio API. | Original work — No external SFX library used. |
| Dialogue Voice Lines | Character dialogues are spoken via the browser's built-in SpeechSynthesis API. The voice is determined by the language/pitch preset and the system voices installed on the player's device. No audio clips are bundled. | Web Speech API — W3C Community Specification. System voices are the user's property. |
| `assets/audio/` directory | Reserved for optional drop-in `.mp3` replacements. No audio files are currently bundled. The directory contains only a `README.md` placeholder. | N/A — No bundled audio files. |

---

## Libraries & Tools

| Asset | Details | Licence |
|---|---|---|
| Third-party JavaScript libraries | None. The game uses zero external JS dependencies, CDN links, npm packages, or frameworks. | N/A |
| Build Tools | Packaged using a custom Python script (`tools/make-zip.py`). Verification via `tools/verify-package.py`. No bundler (Webpack, Vite, etc.) used. | Python Standard Library — PSF License. No third-party Python packages used. |

---

## Development Team

| Role | Name |
|---|---|
| Concept, Design & Narrative | By Team Diet Coke |
| Game Development | Amogh Mani Tripathi|

---

## Special Thanks & Public Interest

- **Emergency Helpline (India):** 112
- **Women Helpline (India):** 181

---

> **Attribution Completeness Note:**  
> All art, audio, and code in GHAR TAK is 100% procedurally generated or original work.  
> No external libraries, CDN resources, or third-party assets (images, audio clips, fonts, or icons) are bundled.  
> The `TODO` entries above require the developer/team name to be filled in before public release.
