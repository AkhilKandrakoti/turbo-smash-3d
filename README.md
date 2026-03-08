# 🏎️ TURBO SMASH 3D

<div align="center">

![Turbo Smash 3D](https://img.shields.io/badge/TURBO-SMASH%203D-FFD600?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iI0ZGRDYwMCIgZD0iTTUgMTFMMSAxNWgzdjRoNnYtNGg0djRoNnYtNGgzTDE5IDExSDV6Ii8+PC9zdmc+)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=three.js&logoColor=white)
![No Dependencies](https://img.shields.io/badge/Dependencies-ZERO-00FF88?style=for-the-badge)
![Mobile Ready](https://img.shields.io/badge/Mobile-Ready-00EEFF?style=for-the-badge)

### 🎮 [▶ PLAY NOW — turbo-smash-3d.vercel.app](https://turbo-smash-3d.vercel.app)

*A fully featured 3D kart battle game — built in a single HTML file, zero installs, runs in your browser.*

</div>

---

## 📸 Overview

**Turbo Smash 3D** is a browser-based 3D kart battle game inspired by Smash Karts, built entirely with [Three.js](https://threejs.org/) in a single self-contained HTML file. Jump into any of 5 themed arenas, choose your difficulty, pick up weapons, and obliterate AI opponents — all without installing anything.

---

## ✨ Features

### 🗺️ 5 Unique Arenas
| Arena | Theme | Weather |
|-------|-------|---------|
| 🏜️ Desert Dunes | Scorching hot sandstone | Sandstorm |
| 🌆 Night City | Neon-lit cyberpunk streets | Rain |
| 🌴 Jungle Rush | Dense wild terrain | Clear |
| ❄️ Snow Peak | Blizzard ice arena | Snowfall |
| 🌋 Volcano Core | Lava rivers & fire | Rising embers |

### 💥 5 Weapons with Realistic 3D Models
| Weapon | Model | Damage Rule |
|--------|-------|-------------|
| 🔫 Machine Gun | Brass bullet with lead tip | 3 hits = kill · 2 hits = 70% · 1 hit = 50% |
| 💣 Triple Bomb | Round fuse bomb with spark | 3 bombs arced — direct hit = instant kill |
| ☢️ Nuke Missile | White rocket with red fins | Any hit = instant kill + massive AOE |
| ⚙️ Land Mine | Disc with prongs + warning light | Contact after arming = instant kill |
| 🛡️ Shield | Cyan energy dome | Blocks all damage for 5 seconds |

### 🧠 Smart AI — 3 Difficulty Levels
- **🟢 Easy** — 5 bots, slow, wide aim, lots of mistakes
- **🟡 Medium** — 6 bots, smart pathfinding, 72% accuracy
- **🔴 Hard** — 7 bots, near-perfect aim, always targets you, ruthless

AI uses **raycasting wall detection** across 5 rays, **flanking pathfinding**, and **staggered replanning** — no more bots driving into walls.

### 🚗 Real Physics
- **Car-to-car collision** with velocity impulse, momentum transfer and yaw deflection
- **Wall reflection** off surface normals — hit a wall at an angle and slide along it
- **Scrape sparks** on wall hits · **Impact sparks** on car collisions
- **Camera shake** on heavy impacts

### ⏱️ Flexible Time Limits
Choose from **1:00 Sprint**, **2:00 Standard**, **3:00 Extended**, **5:00 Marathon**, or **∞ No Limit**

### 📱 Mobile Friendly
- Virtual joystick (left thumb) + Fire / Boost buttons (right thumb)
- `safe-area-inset` support for notched phones
- Touch ID tracking for reliable multi-touch

---

## 🎮 Controls

### Desktop
| Key | Action |
|-----|--------|
| `W` / `↑` | Accelerate |
| `S` / `↓` | Brake / Reverse |
| `A` / `←` | Steer Left |
| `D` / `→` | Steer Right |
| `Space` / `Enter` | Fire Weapon |
| `Shift` | Boost |

### Mobile
| Control | Action |
|---------|--------|
| Left joystick | Steer & accelerate |
| 🔫 Button | Fire weapon |
| ⚡ Button | Boost |

---

## 🚀 Play & Deploy

### Play Instantly
👉 **[https://turbo-smash-3d.vercel.app](https://turbo-smash-3d.vercel.app)**

No install. No login. Just open and play.

### Self-Host in 60 Seconds
```bash
# Clone the repo
git clone https://github.com/YOUR-USERNAME/turbo-smash-3d.git

# Open directly in browser — no server needed
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

## 🏗️ Tech Stack

| Technology | Usage |
|-----------|-------|
| **Three.js r128** | 3D rendering, scene, lighting, shadows |
| **WebGL** | GPU-accelerated graphics via Three.js |
| **Vanilla JS** | Game loop, physics, AI, controls |
| **HTML5 Canvas** | Minimap, weapon pickup labels |
| **CSS3** | HUD, UI screens, animations |

**Zero npm. Zero build step. Zero backend.** One file, ~2200 lines.

---

## 📁 Project Structure

```
index.html          ← The entire game (HTML + CSS + JS in one file)
README.md           ← You are here
```

---

## 🎯 Gameplay Tips

- 🔵 **Blue glowing pads** on the ground = **boost pads** — drive over them for a speed burst
- 🌀 **Spinning weapon pickups** show their name — choose wisely before picking up
- 💨 **Boost** just before firing a nuke for extra range
- 🛡️ **Shield first** if you're low on HP — then find a weapon
- 🗺️ Use the **minimap** (bottom-left) to track enemies and pickups

---

## 🙌 Credits

Built with ❤️ using [Three.js](https://threejs.org/) — the open source 3D library for the web.

---

<div align="center">

**[🎮 PLAY TURBO SMASH 3D NOW](https://turbo-smash-3d.vercel.app)**

*If you enjoy it, drop a ⭐ on GitHub!*

</div>
