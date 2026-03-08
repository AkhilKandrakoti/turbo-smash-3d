# 🏎️ Turbo Smash 3D

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white)
![No Dependencies](https://img.shields.io/badge/Dependencies-ZERO-00FF88?style=for-the-badge)
![Mobile Ready](https://img.shields.io/badge/Mobile-Ready-00EEFF?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

### 🎮 [▶ PLAY NOW — turbo-smash-3d.vercel.app](https://turbo-smash-3d.vercel.app)

*A complete 3D kart battle game — single HTML file, zero installs, runs in any browser on any device.*

</div>

---

## 📸 Screenshots

> Desert Dunes · Night City · Volcano Core

![Turbo Smash 3D Gameplay](https://turbo-smash-3d.vercel.app/preview.jpg)

---

## 📖 About

**Turbo Smash 3D** is a fully featured browser-based 3D kart battle game built from scratch using [Three.js](https://threejs.org/). The entire game — 3D engine, physics, AI, weapons, sound effects, UI — lives in a single `index.html` with no build step, no backend, and no dependencies beyond Three.js.

Pick an arena, choose your difficulty, pick up weapons, and destroy AI opponents. Runs smoothly on **Windows, macOS, iOS, Android** and every browser.

---

## ✨ Features

### 🗺️ 5 Themed Arenas

| Arena | Atmosphere | Weather |
|-------|-----------|---------|
| 🏜️ Desert Dunes | Hot sandstone, golden sky | Sandstorm particles |
| 🌆 Night City | Neon cyberpunk, rain-slicked streets | Heavy rainfall |
| 🌴 Jungle Rush | Dense foliage, green haze | Clear |
| ❄️ Snow Peak | Icy tundra, blizzard conditions | Snowfall drift |
| 🌋 Volcano Core | Lava rivers, ember glow, fire sky | Rising embers |

### 💥 5 Weapons — Each with a Unique 3D Model

| Weapon | 3D Model | Damage |
|--------|----------|--------|
| 🔫 Machine Gun | Brass casing + lead tip | 1 hit = 50hp · 2 hits = 70hp · 3 hits = kill |
| 💣 Triple Bomb | Fuse sphere + spark glow | 3 arced bombs · direct hit = instant kill |
| ☢️ Nuke Missile | White rocket + red tail fins | Any hit = instant kill + mushroom cloud AOE |
| ⚙️ Land Mine | Disc + prongs + pulsing warning light | Arms after 1.5s · contact = instant kill |
| 🛡️ Shield | Transparent cyan energy dome | Blocks all damage for 5 seconds |

Every pickup shows a **floating 3D name label** and **dual spinning rings** so you always know what you're grabbing.

### 🧠 AI System — 3 Difficulty Levels

| Level | Bots | Behaviour |
|-------|------|-----------|
| 🟢 Easy | 5 | Slow speed, 45% accuracy, makes navigation mistakes |
| 🟡 Medium | 6 | Smart pathfinding, 72% accuracy, chases the player |
| 🔴 Hard | 7 | Fast, 94% accuracy, near-perfect aim, always targets you |

AI uses **5-ray raycasting wall detection**, **flanking pathfinding** when blocked, and **staggered replanning timers** so bots never move in sync.

### 🚗 Physics System

- Velocity-based movement with engine thrust blending
- Car-to-car collision with impulse resolution and momentum transfer
- Wall surface normal reflection — glancing hits slide along walls
- Yaw deflection on impact for realistic spin-out
- Camera shake scaled to impact force
- Scrape sparks on wall hits · Impact sparks on car collisions

### 🔊 Procedural Audio

All sound effects generated in real time using the **Web Audio API** — zero audio files:

Engine hum that rises with speed · Machine gun burst · Explosion noise · Deep nuke rumble · Pickup chime · Boost sweep · Impact thud · Victory fanfare · Defeat melody · Countdown beeps

### ⏱️ Time Limit Options

**1 min Sprint** · **2 min Standard** · **3 min Extended** · **5 min Marathon** · **∞ No Limit**

### 📱 Full Mobile Support

- Virtual joystick (left thumb) for steering and acceleration
- Dedicated fire and boost buttons (right thumb)
- Multi-touch support — joystick + fire simultaneously
- `viewport-fit=cover` and `safe-area-inset` for notched phones
- Landscape optimised

---

## 🎮 Controls

### ⌨️ Desktop

| Input | Action |
|-------|--------|
| `W` / `↑` | Accelerate |
| `S` / `↓` | Brake / Reverse |
| `A` / `←` | Steer Left |
| `D` / `→` | Steer Right |
| `Space` / `Enter` | Fire Weapon |
| `Shift` | Boost |

### 📱 Mobile

| Control | Action |
|---------|--------|
| Left joystick | Steer and accelerate |
| 🔫 Button | Fire weapon |
| ⚡ Button | Activate boost |

---

## 🏗️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| **Three.js r128** | 3D scene, rendering, lighting, particles |
| **WebGL** | GPU-accelerated graphics via Three.js |
| **Web Audio API** | All sound effects, engine audio |
| **HTML5 Canvas** | Minimap, weapon pickup labels |
| **Vanilla JS** | Game loop, physics engine, AI, controls |
| **CSS3** | HUD, animated UI screens, responsive layout |

No npm. No build step. No backend. **One file.**

---

## 🚀 Getting Started

### Play instantly
👉 [https://turbo-smash-3d.vercel.app](https://turbo-smash-3d.vercel.app)

### Run locally
```bash
git clone https://github.com/YOUR-USERNAME/turbo-smash-3d.git
cd turbo-smash-3d
open index.html   # no server needed
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
index.html     ← Entire game (HTML + CSS + JS, ~2500 lines)
README.md      ← This file
```

---

## ⚡ Performance

Optimised to run smoothly on every system — Windows, macOS, iOS, Android, and budget laptops:

- Pixel ratio capped (1× on mobile, 1.5× on desktop)
- Shadows disabled — no shadow render pass
- `MeshLambertMaterial` used throughout — no PBR lighting overhead
- All arena point lights removed — `DirectionalLight` only
- Weather particles capped at 800
- Camera far plane set to 250 — fog hides everything beyond it
- DT capped at 25ms — no speed bursts after tab switches or lag spikes

---

## 🎯 Tips

- Blue glowing pads on the ground are **boost pads** — hit them for a speed burst
- Spinning pickups show their weapon name before you drive over them
- Grab **Shield** first when low HP, then hunt for a weapon
- Use the **minimap** bottom-left to track enemies and pickups
- Boost just before firing a Nuke for maximum range

---

## 📜 License

MIT — free to use, modify and distribute.

---

<div align="center">

Built with ❤️ using [Three.js](https://threejs.org/)

**[🎮 Play Turbo Smash 3D](https://turbo-smash-3d.vercel.app)**

*If you enjoy it, drop a ⭐ on GitHub!*

</div>
