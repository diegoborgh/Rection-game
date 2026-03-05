Here's a comprehensive README for your Neural Reflex project:

```markdown
# ⚡ Neural Reflex | 3D Reaction Timer

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Three.js](https://img.shields.io/badge/Three.js-black?style=flat&logo=three.js&logoColor=white)](https://threejs.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)

A cyberpunk-styled, browser-based reaction time tester featuring real-time 3D graphics, synthesized audio feedback, and statistical tracking. No installation required—just open and play.

[🎮 **Play Now**](#) https://diegoborgh.github.io/Rection-game/ <!-- Add your deployed link here -->


## 🎯 Overview

**Neural Reflex** tests your neural pathway speed through an interactive 3D experience. Watch the neural core (icosahedron) as it shifts from standby blue to **emerald green**—click the moment it activates to measure your reaction time in milliseconds.

Built as a single-file application using vanilla JavaScript and Three.js, it requires zero build tools or dependencies beyond a modern web browser.

## ✨ Features

### Gameplay
- **5-Stage State Machine**: Idle → Waiting → Ready → Result/False Start
- **Randomized Delay**: 1-5 second random interval prevents anticipation
- **False Start Detection**: Penalty system for clicking too early
- **Performance Analytics**: Tracks last, average, best times, failed attempts, and total tries
- **Dynamic Feedback**: Contextual messages based on your speed (Superhuman! ⚡, Lightning fast! 🚀, etc.)

### Visual Experience
- **3D Icosahedron Core**: Wireframe + solid mesh with dynamic emissive materials
- **State-Based Color Coding**:
  - 🔵 **Blue**: Idle/Waiting
  - 🟢 **Emerald**: Ready to click
  - 🔴 **Red**: False start
- **Particle Background**: 600 floating data points with additive blending
- **Responsive Animations**: Float, shake, pulse, and rotation speed changes
- **Glassmorphism UI**: Frosted glass stat cards with hover effects

### Audio & Interaction
- **Synthesized SFX**: Real-time Web Audio API generated tones (no external assets)
- **Multi-Input Support**: Mouse, touch (mobile), and keyboard (Spacebar)
- **Raycasting**: Cursor changes when hovering over the 3D core

## 🚀 Getting Started

### Option 1: Direct Open
Simply open `index.html` in any modern browser. No server required.

### Option 2: Local Server (Recommended)
```bash
# Python 3
python -m http.server 8000

# Node.js
npx serve

# PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000`.

## 🎮 How to Play

1. **Start**: Click the neural core or press `Spacebar` to begin
2. **Wait**: The core turns blue and spins—wait for it to turn **green**
3. **React**: Click immediately when it turns green
4. **Results**: View your reaction time in milliseconds
5. **Retry**: Click again to add to your statistics

### Scoring Reference
| Time | Rating |
|------|--------|
| < 200ms | Superhuman! ⚡ |
| < 250ms | Lightning fast! 🚀 |
| < 300ms | Great! 👏 |
| < 400ms | Good |
| 400ms+ | Keep practicing |

> **Tip**: Clicking before the core turns green counts as a failed attempt!

## 🕹️ Controls

| Input | Action |
|-------|--------|
| `Click` | Interact with core |
| `Spacebar` | Alternative interaction |
| `Touch` | Mobile support |
| `Reset Data` button | Clear all statistics |

## 🛠️ Technical Details

### Architecture
- **Single File Application**: All HTML, CSS, and JavaScript contained in one file
- **No External Build Step**: Uses CDN links for Three.js and Tailwind CSS
- **State Machine Pattern**: Clean separation of game states (IDLE, WAITING, READY, RESULT, FALSE_START)

### 3D Graphics (Three.js)
- **Core Geometry**: Icosahedron with dual mesh rendering (wireframe + solid)
- **Lighting**: Ambient + dual point lights (blue/green)
- **Materials**: Standard material with dynamic emissive properties
- **Particle System**: BufferGeometry with 600 vertices for background ambiance

### Performance
- **Device Pixel Ratio Cap**: Limited to 2x for performance
- **Efficient Raycasting**: Only checks intersection when necessary
- **RequestAnimationFrame**: Smooth 60fps animation loop

### Browser Support
- Chrome/Edge 80+
- Firefox 75+
- Safari 13+
- Mobile Safari (iOS 13+)
- Chrome Android

*Note: Requires WebGL and Web Audio API support.*

## 📁 File Structure

```
neural-reflex/
├── index.html          # Complete application (single file)
└── README.md           # This file
```

## 🔮 Future Enhancements

- [ ] Global leaderboard integration
- [ ] Dark/light theme toggle
- [ ] Export statistics to CSV
- [ ] Additional 3D core shapes
- [ ] Haptic feedback for mobile


**Built with** 🧠 **and** ⚡ **using Three.js & Tailwind CSS**
```

**Quick Tips for customizing:**
1. Replace `screenshot.png` with an actual screenshot of your game (you can use the browser's dev tools to capture the 3D scene)
2. Add your deployed URL to the "Play Now" badge if you host it on GitHub Pages/Netlify
3. The code is production-ready as a single file, making it perfect for sharing via GitHub Gist or codepen.io