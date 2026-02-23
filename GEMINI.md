# Aussie Meme Boss Rush: 3D Story Deluxe

A high-octane, neon-drenched 3D boss rush shooter where you face off against cybernetic versions of Australia's most infamous wildlife memes. Built with Three.js and designed for both desktop precision and mobile accessibility.

## 🇦🇺 The Story
In the year 20XX, the Great Emu War has escalated into a digital nightmare. The "Outback Protocol" has been triggered, and the memes of the old world have been uploaded into a neon-noir combat simulation. You are a Cyber-Operator tasked with surviving the "Big Five" to prevent a total reality collapse.

## 🕹 Gameplay Mechanics
- **Combat:** Precision-based shooting. Hit enemies, projectiles, and power-ups by clicking/tapping them directly on your screen.
- **Weapon System:**
  - **Standard (Green):** Reliable 4 shots per second.
  - **Hyper-Beam (Cyan):** High damage, activated by weapon power-ups.
- **Defensive Shield:**
  - **Engagement:** Right-click, on-screen button, or a second finger touch on mobile.
  - **Stats:** 0.6s active window, 2s recharge.
- **Scoring & Multipliers:**
  - Successive boss hits double your multiplier up to **16x**.
  - At **16x**, the multiplier catches fire—literally.
  - Taking damage or missing a shot resets the multiplier.

## 🛠 Technical Implementation
- **Graphics:** `Three.js` (WebGL) with a custom procedural shader system.
- **Audio:** Custom procedural sound engine using Web Audio API. Generates real-time synth basslines and FM-style sound effects without external assets.
- **Materials:** Bosses use procedural "Noise" chunks (Snoise) for fur, scales, and tech-vein effects without external textures.
- **Targeting:** Pure 2D screen-space hit detection. Entities and boss parts are projected to UI coordinates for pixel-perfect tap/click accuracy.
- **Physics:** Custom ragdoll simulation triggered on boss death—pieces fall, bounce off the ground plane, and flail in slow motion before exploding into confetti.
- **Phase 2 Transformation:** Mid-fight cinematic cutscene where body parts dynamically transform into indestructible glowing silver steel, requiring precision targeting of remaining organic segments.
- **Responsive Design:** Dynamic viewport scaling (`--vh`) and adaptive UI layouts to support Portrait and Landscape orientations across all devices.

## 👾 The Bosses
1. **Drop Bear:** The hanging terror of the neon forest.
2. **Cyber Emu:** A speed demon from the Great War.
3. **Magpie Drone:** Swoop season in the digital suburbs.
4. **Cyber Huntsman:** Eight-legged fury in the neon shed.
5. **K-9000 Roo:** The ultimate boxing champion of the Outback.

## 📜 Editing Guidelines
- **Single-File Architecture:** Keep the core game within `index.html` for maximum portability and "just works" deployment.
- **Procedural First:** Prefer generated geometries and shaders over external assets.
- **Performance:** Maintain 60fps by pooling particles and cleaning up ragdoll entities after the confetti explosion.
- **Style:** Adhere to the "Press Start 2P" font and the neon-cyan/magenta/yellow color palette.
- **Responsiveness:** Always test UI overlaps in narrow portrait modes. The Shield Indicator and Multiplier should never collide.

## 🚀 Future Ideas
- **Global Leaderboard:** Replace LocalStorage with a lightweight backend for cross-device competition.
- **Shop:** Spend score between missions on shield duration or projectile speed.
