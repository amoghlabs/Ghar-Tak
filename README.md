# GHAR TAK (घर तक) — Loop Broken

> **Theme:** LOOP  
> **Tagline:** *Same street. Same words. Every day.*  
> A college girl walks home through a crowded Indian street. Dodging harassment, gossip, and societal judgment, she gathers courage, learns to **SPEAK UP**, and breaks the daily loop once and for all.

---

## 🎮 How to Play

### Controls
| Action | Keyboard | Touch / Mobile |
| :--- | :--- | :--- |
| **Change Lane** | `Left` / `Right` or `A` / `D` | Swipe Left / Right or On-screen `◀` / `▶` buttons |
| **Jump** | `Up` or `W` | Swipe Up or On-screen `▲` button |
| **Slide / Fast-Fall** | `Down` or `S` | Swipe Down or On-screen `▼` button |
| **SPEAK UP!** | `SPACE` | Tap the glowing **SPEAK UP** button |
| **Pause** | `P` or `Esc` | Tap `⏸️` button |
| **Mute Audio** | `M` | Tap `🔊` button |

### Gameplay Mechanics
1. **Confidence (Health):** Starts at 100%. Street obstacles cost 10%, Person obstacles cost 20%. Hits trigger camera shake, a stumble, and 1.5s of invincibility. If you dodge cleanly for 8 seconds, Confidence regenerates (+1%/s). Below 30%, dark vignette and heartbeats begin.
2. **Courage & SPEAK UP:** Collect glowing golden **Courage Orbs** to fill your meter. When full (100%), activate **SPEAK UP** to shout *"BAS! BAHUT HO GAYA!"*, unleashing an expanding shockwave that silences all harassers on screen, unlocks their Voice badge, and plays the girl's comeback!
3. **Friend Call:** Pickup the ringing smartphone for a 5-second protective shield where obstacles bounce off you.
4. **Cutting Chai:** Drink steaming chai to restore +15% Confidence.
5. **The Daily Loop:**
   - One run is her walk home from **College Gate -> Market Street -> Colony Lane -> Home Gate** (~40s on Day 1).
   - Reaching home triggers a door slam, the card *"Safe... for today"*, an alarm clock, and a VHS rewind glitch into **Day 2**.
   - With each Day, the speed ramps up and the sky shifts: **Afternoon (Day 1) -> Sunset (Day 2) -> Dusk (Day 3) -> Neon Night (Day 4+)** with streetlights turning on.
   - Dialogue escalates across 3 tiers, gaining echoes and overlapping.
6. **Breaking the Loop:**
   - Silence all 4 person obstacles at least once using Speak Up to unlock their **4 Voices** (Drunk Man, Gossip Aunties, Marriage Uncle, Dress-Code Aunty).
   - Voices persist across runs in `localStorage`!
   - Once all 4 are unlocked, reaching Home Gate triggers the **"LOOP BROKEN"** ending: the infinity symbol snaps, music resolves to a triumphant major chord, other young women join her side by side, and the harassment stops forever.

---

## 🛠️ Tech Stack & Offline Standalone Design

- **Pure HTML5 + CSS + Vanilla JS**: No frameworks, no ES modules, no CDNs, no external web fonts or dependencies.
- Runs offline via `file:///` protocol (just double click `index.html`) or inside an iframe embed on itch.io.
- **Canvas 2D Pseudo-3D Engine**: 3 lanes, vanishing point perspective math ($scale = 0.25 + 0.75 \times t$, $y = \text{lerp}(horizonY, playerY, t^{1.4})$).
- **Web Audio API Sound Engine**: 100% procedural synthesizers for all SFX, ambient street hums, and a dynamic 4-layer looping music track (Drums -> Bass -> Lead Melody -> Tension synth).
- **Voice Fallback Chain**:
  1. Recorded `.mp3` audio files in `assets/audio/`
  2. Web SpeechSynthesis (`hi-IN` Hindi voices with customized pitch & rate per character)
  3. Real-time synthesized typewriter blip-talk!

---

## 📦 Packaging

To package the game into a standalone distribution zip ready for itch.io or web export, run:

```bash
python tools/make-zip.py
```

This builds `dist/GharTak.zip` with `index.html` at the zip root and all paths using standard forward slashes.

To verify the package structure, letter-casing, and asset links:
```bash
python tools/verify-package.py
```

### itch.io Upload Instructions
1. Upload `dist/GharTak.zip`.
2. On itch.io, choose **HTML** as project kind.
3. Check **"This file will be played in the browser"**.
4. Set viewport dimensions: **540 x 960** (or check *Fullscreen button* enabled).

---

## 🧪 Debug Mode & Hotkeys

Launch with query parameter `?debug=1` (e.g. `index.html?debug=1`) or press backquote (`` ` ``) to toggle debug info:
- `1`, `2`, `3`, `4`: Instantly jump to Day 1, 2, 3, or 4 (adjusts lighting, speed, music layers, and dialogue tiers)
- `O`: Instantly fill Courage meter to 100% (ready for Speak Up)
- `V`: Instantly unlock all 4 Voices
- `H`: Toggle cheat invincibility and restore 100% Confidence
- `C`: Fast-forward route to the Home Gate
