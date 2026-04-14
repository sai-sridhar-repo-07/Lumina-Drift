# 🌌 Lumina Drift

**Particle Text Canvas** — a calm, interactive particle system where typed words gracefully morph from a glowing 3D sphere. Move your mouse to gently repel particles, click to create ripple pushes, and double-click to reset.

<img width="1500" height="857" alt="Screenshot 2026-04-14 at 10 38 07 PM" src="https://github.com/user-attachments/assets/00318fa2-3907-4a88-8dce-0d196052a183" />


---

## ✨ Features

- **8,800 smooth particles** - high-performance `Float32Array` physics
- **Two modes**:
  - 🌐 Sphere Mode - rotating, softly drifting particle sphere
  - 🔤 Text Mode - particles morph into any typed phrase
- 🖱️ Mouse Repel - cursor gently pushes particles
- 💥 Click Ripple - creates a wave force across particles
- 🔄 Double-click Reset - return to sphere instantly
- 📱 Responsive Canvas - adapts to screen + DPR scaling
- 🧊 Glassmorphism UI - minimal, clean, glowing controls
- ⚡ No dependencies - pure HTML, CSS, JS

---

## 🚀 How to Use

1. Open `index.html` in any modern browser
2. Type a word or phrase -> particles form text
3. Move your mouse -> particles repel smoothly
4. Click -> ripple effect pushes particles
5. Double-click -> reset to sphere

---

## 🎨 Customization

Edit constants inside `<script>` in `index.html`.

### ⚙️ Physics Tuning

```js
const PARTICLE_COUNT = 8800;
const REPEL_RADIUS = 115;
const REPEL_FORCE = 5.6;
const SPHERE_SPRING = 0.012;
const TEXT_SPRING = 0.015;
const DAMPING = 0.88;
const ROTATION_SPEED = 0.0042;
```

### 🎨 Colors

```js
// Sphere Mode -> teal to lavender (HSL 180-300)
let hueVal = 180 + Math.random() * 120;
let sat = 70;
let light = 60;

// Text Mode -> cyan to electric blue (HSL 185-230)
let textHue = 185 + Math.random() * 45;
let textSat = 80;
let textLight = 65;

// Customize freely
hueVal, sat, light;
```

---

## 🌊 Ripple Effect

```js
addRipple(x, y, intensity = 1.0);
```

- Recommended intensity: `0.5` - `1.5`
- Controlled by: `strength`, `radius`, `lifetime`

---

## 🧠 How It Works

- **Fibonacci Sphere** - even particle distribution using the golden angle
- **Text Sampling** - offscreen canvas maps pixels to particle targets
- **Spring Physics** - smooth motion using damped spring forces
- **Mouse Interaction** - cursor + ripple apply radial forces
- **3D Projection** - adds depth using perspective transform

---

## 📂 Project Structure

```text
lumina-drift/
├── index.html
└── README.md
```

No build tools. No setup. Just open and run.

---

## 🖼️ Screenshots

```text
/screenshots/sphere.png
/screenshots/text.png
```

---

## 🌐 Browser Support

- Chrome / Edge 90+
- Firefox 88+
- Safari 14+

📱 Touch Support: Partial (can be extended)

---

## 📝 License

MIT — free to use, modify, and distribute

---

## 🙌 Credits

Built with passion for:

- Creative coding
- Generative visuals
- Calm digital experiences

Inspired by particle systems and interactive typography ✨
