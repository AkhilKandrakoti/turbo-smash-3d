# 🏎️ Turbo Smash 3D

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white)
![No Dependencies](https://img.shields.io/badge/Dependencies-ZERO-00FF88?style=for-the-badge)
![Mobile Ready](https://img.shields.io/badge/Mobile-Ready-00EEFF?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

### 🎮 [▶ PLAY NOW — turbo-smash-3d.vercel.app](https://turbo-smash-3d.vercel.app)

*A complete 3D kart battle game built in a single HTML file — zero installs, zero dependencies, runs entirely in your browser.*

</div>

---

## 📖 About

Turbo Smash 3D is a fully featured browser-based 3D kart battle game built from scratch using [Three.js](https://threejs.org/). The entire game — rendering engine, physics system, AI, sound effects, UI and all game logic — lives inside a single `index.html` file with no build step, no backend, and no external dependencies beyond Three.js.

The project was built as a challenge to see how much of a complete, polished game experience could be packed into one self-contained file.

---

## ✨ Features

### 🗺️ 5 Themed Arenas
| Arena | Atmosphere | Weather Effect |
|-------|-----------|----------------|
| 🏜️ Desert Dunes | Hot sandstone, golden light | Sandstorm particles |
| 🌆 Night City | Neon cyberpunk, rain-slicked streets | Rainfall |
| 🌴 Jungle Rush | Dense foliage, green fog | Clear |
| ❄️ Snow Peak | Icy tundra, blizzard conditions | Snowfall drift |
| 🌋 Volcano Core | Lava rivers, ember glow | Rising embers |

### 💥 5 Weapons — Each with a Unique 3D Model
| Weapon | Visual | Mechanic |
|--------|--------|----------|
| 🔫 Machine Gun | Brass casing + lead tip | Burst of 3 bullets — 1 hit = 50hp, 3 hits = kill |
| 💣 Triple Bomb | Fuse sphere + spark glow | 3 arced bombs — direct hit = instant kill |
| ☢️ Nuke Missile | Rocket body + tail fins | Any hit = instant kill + mushroom cloud AOE |
| ⚙️ Land Mine | Disc + prongs + pulsing light | Arms after 1.5s — contact = instant kill |
| 🛡️ Shield | Transparent energy dome | Blocks all damage for 5 seconds |

Weapon pickups display a **floating billboard label** and **spinning colored ring** in the arena so players always know what they are picking up before driving over it.

### 🧠 AI System
Three difficulty levels with genuinely different behaviour — not just speed changes:

- **Easy** — 5 bots, slow speed, 45% aim accuracy, lots of navigation errors
- **Medium** — 6 bots, balanced speed, 72% accuracy, chases the player
- **Hard** — 7 bots, fast, 94% accuracy, always targets the player, near-perfect aim

The AI uses a **5-ray raycasting wall detection** system, **flanking pathfinding** when blocked, **staggered replanning timers** to avoid synchronized behaviour, and **speed reduction on sharp turns** for realistic handling.

### 🚗 Physics System
- Velocity-based movement with engine thrust blending
- Car-to-car collision using impulse resolution and momentum transfer
- Wall surface normal reflection — glancing hits slide along walls
- Positional correction to prevent overlap clipping
- Yaw deflection on impact for realistic spin-out effect
- Camera shake scaled to impact force
- Scrape sparks on wall hits, impact sparks on car collisions

### 🔊 Procedural Audio
All sound effects generated at runtime using the Web Audio API — no audio files required.

Engine hum that dynamically pitches with speed, machine gun burst, explosion noise, deep nuke rumble, pickup ascending chime, boost sweep tone, damage impact thud, victory fanfare, defeat melody, and countdown beeps.

### ⏱️ Game Modes
Choose your time limit before each match: **1 min Sprint**, **2 min Standard**, **3 min Extended**, **5 min Marathon**, or **No Limit** (shows elapsed time).

### 📱 Mobile Support
- Virtual joystick for steering and acceleration
- Dedicated fire and boost buttons
- Multi-touch support (joystick + fire simultaneously)
- Responsive HUD that adapts to screen size
- Landscape orientation optimized

---

## 🎮 Controls

### Desktop
| Input | Action |
|-------|--------|
| `W` or `↑` | Accelerate |
| `S` or `↓` | Brake / Reverse |
| `A` or `←` | Steer Left |
| `D` or `→` | Steer Right |
| `Space` / `Enter` | Fire Weapon |
| `Shift` | Boost |

### Mobile
| Control | Action |
|---------|--------|
| Left joystick | Steer and accelerate |
| Fire button | Fire weapon |
| Boost button | Activate boost |

---

## 🏗️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| **Three.js r128** | 3D scene, rendering, lighting, shadows, particles |
| **WebGL** | GPU-accelerated graphics via Three.js |
| **Web Audio API** | Procedural sound effects, engine audio |
| **HTML5 Canvas** | Minimap rendering, weapon pickup labels |
| **Vanilla JS** | Game loop, physics engine, AI system, controls |
| **CSS3** | HUD, animated UI screens, responsive layout |

No npm. No build step. No backend. One file.

---

## 🚀 Getting Started

### Play instantly
👉 [https://turbo-smash-3d.vercel.app](https://turbo-smash-3d.vercel.app)

### Run locally
```bash
# Clone the repo
git clone https://github.com/YOUR-USERNAME/turbo-smash-3d.git
cd turbo-smash-3d

# Open directly — no server needed
open index.html
```

### Deploy to Vercel
```bash
npm i -g vercel
vercel --prod
```

### Deploy to GitHub Pages
1. Push `index.html` to your repo
2. Go to **Settings → Pages → Branch: main → Save**
3. Live at `https://YOUR-USERNAME.github.io/turbo-smash-3d`

---

## 📁 Project Structure

```
index.html     ← Entire game (HTML + CSS + JS, ~2300 lines)
README.md      ← This file
```

---

## 💡 How It Works

The game runs a fixed-timestep `requestAnimationFrame` loop. Each frame:

1. Player input is read from keyboard state or virtual joystick
2. All karts apply engine thrust to a velocity vector
3. `resolveCarCollisions()` checks all kart pairs and applies impulse physics
4. Wall collision checks reflect velocity off surface normals
5. Bullets, bombs, mines and shields are updated
6. Particles and weather effects are animated
7. The minimap is redrawn on a 2D canvas
8. The HUD, leaderboard and speedometer are refreshed
9. Three.js renders the full 3D scene

AI bots run their own decision tree each frame — casting rays, selecting targets, planning paths and firing weapons independently.

---

## 🎯 Gameplay Tips

- Glowing pads on the ground are **boost pads** — drive over them for a speed burst
- Floating weapon pickups show their name — read it before you pick it up
- If you are low on HP grab a **Shield** first, then hunt for a weapon
- Use the **minimap** (bottom-left) to track enemies and pickups
- Boost just before firing a nuke for maximum range

---

## 📜 License

MIT — free to use, modify and distribute.

---

<div align="center">

Built by AKHIL KANDRAKOTI [Three.js](https://threejs.org/)

**[🎮 Play Turbo Smash 3D](https://turbo-smash-3d.vercel.app)**

</div>
