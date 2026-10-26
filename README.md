# Khushi — Software Engineer & Creative Developer

[![Vite](https://img.shields.io/badge/Vite-6.1-646CFF?style=flat-square&logo=vite&logoColor=white)](https://vitejs.dev/)
[![React](https://img.shields.io/badge/React-19.0-61DAFB?style=flat-square&logo=react&logoColor=black)](https://react.dev/)
[![Lenis](https://img.shields.io/badge/Lenis-Smooth_Scroll-black?style=flat-square)](https://github.com/darkroomengineering/lenis)
[![Tests](https://img.shields.io/badge/Tests-All%20Suites%20Passing-brightgreen?style=flat-square)](https://github.com/khushigsd2924-design/khushi-portfolio)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](LICENSE)

An award-winning luxury interactive portfolio website featuring real-time 60 FPS HTML5 canvas cursor gaze-tracking, inertial momentum smooth scrolling, procedural audio synthesis, and an atmospheric velvet-wine visual aesthetic.

---

## ✨ Features & Engineering Highlights

### 👁️ 60 FPS Cursor-Tracking Character Canvas
- **Pure 1080p WebP Frames**: 64 high-resolution studio directional frames (`000.webp`–`063.webp`) plus a centered neutral rest pose (`center.webp`) extracted directly from video with Telea watermark inpainting.
- **Fluid Gaze Physics**: Real-time Cartesian-to-polar angle translation with circular radian wrapping (`normTarget = (angle + 2π) % 2π`) and smooth frame interpolation governed by an adaptive velocity step limiter (`MAX_FRAME_STEP + (absDiff * 0.05)`).
- **Sub-Pixel Pointer Lerping**: Mouse coordinates are filtered via exponential damping (`1 - Math.pow(1 - 0.22, dt)`) to eliminate micro-jitter while tracking fast cursor sweeps.
- **Deadzone Eye-Contact Locking**: When cursor Euclidean distance from center $r < 0.12$, the engine locks immediately into `center.webp` for direct eye-to-eye gaze.
- **High-DPI Retina Rendering**: Automatically scales for device pixel ratios (`dpr = Math.min(window.devicePixelRatio, 2)`) with high-quality bicubic smoothing.

### 🌊 Inertial Momentum Smooth Scrolling (Lenis)
- Integrated [Lenis](https://github.com/darkroomengineering/lenis) for 60/120 FPS momentum-driven scrolling across Windows, macOS, and Linux.
- Custom exponential luxury easing (`cubic-bezier(0.16, 1, 0.3, 1)`) with zero-snap anchor navigation for internal links (`#projects`, `#about`).
- Dynamic viewport observer via `MutationObserver` that pauses smooth scrolling while modals are open to guarantee clean backdrop locking.

### 🎨 Atmospheric Visual Identity & Analog Film Grain
- **Luxury Editorial Color System**: Deep velvet wine (`#16070a`), dusty rose canvas background (`#9c474f`), champagne gold accents (`#f8c8a0`), and blush highlights (`#e3b5be`).
- **Organic Canvas-to-Body Blend**: Hero section exits through a multi-stop vertical gradient dissolving into a 4-point radial ambient mesh in `.portfolio-content`.
- **Analog SVG Film Grain**: Fixed non-blocking procedural SVG fractal noise (`feTurbulence`) overlay eliminating digital color banding with zero GPU or battery overhead.
- **Jitter-Free Scroll Indicator**: Capsule track featuring a continuously gliding champagne gradient pulse.

### 🔊 Procedural Web Audio Engine
- Built with the native Web Audio API — zero external `.mp3` or `.wav` dependencies.
- Synthesizes organic high-frequency click transients, harmonic chime chords, and ambient resonant feedback with an intuitive global mute toggle.

---

## 💼 Featured Projects Showcase

The portfolio showcases 8 software engineering projects sourced directly from [`khushigsd2924-design`](https://github.com/khushigsd2924-design):

1. **[Reading History](https://github.com/khushigsd2924-design/Reading_History)** *(Full-Stack Web)*
   - Full-stack book tracker & reading analytics platform with live reading goals and Supabase cloud persistence.
   - *Tech:* TypeScript, React 18, Tailwind CSS, Supabase, Lucide React, Vite.

2. **[Interactive 3D Gaze Portfolio](https://github.com/khushigsd2924-design/khushi-portfolio)** *(Interactive Web)*
   - 60 FPS real-time cursor gaze tracking portfolio powered by 64 WebP frames and Web Audio API synthesis.
   - *Tech:* React 19, Vite 6, HTML5 Canvas 2D, Web Audio API, Lenis Smooth Scroll.

3. **[Code With AI Quiz](https://github.com/khushigsd2924-design/quiz-app-code-with-ai)** *(Interactive Web)*
   - Interactive computer science and AI assessment application with live scoring and zero runtime dependencies.
   - *Tech:* JavaScript (ES6+), Modern CSS3, HTML5.

4. **[Student Marks Analysis Engine](https://github.com/khushigsd2924-design/messy-python-refactoring)** *(Python & Algorithms)*
   - Python academic performance analyzer computing distributions, percentiles, and class toppers with refactored modularity.
   - *Tech:* Python 3, Statistical Algorithms, Data Processing.

5. **[TDD Defect Lifecycle Harness](https://github.com/khushigsd2924-design/buggy-python-debugging)** *(Software Engineering)*
   - Test-driven development verification suite illustrating the Red $\to$ Fix $\to$ Green lifecycle and regression tests.
   - *Tech:* Python 3, Pytest, Unit Testing, TDD, Bug Auditing.

6. **[C++ Struct to Python Dict](https://github.com/khushigsd2924-design/python-basics-struct-to-dict)** *(Systems & Data)*
   - Memory record mapping utility converting low-level C++ schemas into verified Python dictionaries with documentation audits.
   - *Tech:* Python 3, C++ Concepts, Data Structures, Audit Verification.

7. **[Fibonacci Sequence Generator](https://github.com/khushigsd2924-design/python-basics-fibonacci)** *(Python & Algorithms)*
   - Configurable sequence engine optimized for algorithmic complexity and verified against formal claims in `Audit.md`.
   - *Tech:* Python 3, Mathematical Computing, Algorithmic Analysis.

8. **[Factorial Algorithmic Engine](https://github.com/khushigsd2924-design/python-basics-factorial)** *(Python & Algorithms)*
   - High-precision factorial computation engine with recursive/iterative models and edge verification audit trails.
   - *Tech:* Python 3, Recursive Math, Verification Audit, Clean Code.

---

## 🛠️ Tech Stack

- **Frontend Framework**: [React 19](https://react.dev/) + [Vite 6](https://vitejs.dev/)
- **Smooth Scrolling**: [Lenis 1.3](https://github.com/darkroomengineering/lenis)
- **Icons**: [Lucide React](https://lucide.dev/)
- **Graphics & Physics**: HTML5 Canvas 2D API + RequestAnimationFrame loop
- **Typography**: Syne (Display), Plus Jakarta Sans (Body), JetBrains Mono (Technical)
- **Styling**: Modern CSS3 (CSS variables, backdrop-filter blur, CSS Grid, clamp)
- **Testing**: Node.js ESM verification suites + Python 3 frame integrity suite

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org/) (v18.0.0 or higher)
- `npm` (v9.0.0 or higher)
- Optional: Python 3 with `opencv-python` and `Pillow` (if re-extracting frames from source video)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/khushigsd2924-design/khushi-portfolio.git
   cd khushi-portfolio
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start the local development server**:
   ```bash
   npm run dev
   ```
   Open [http://localhost:3000](http://localhost:3000) in your browser.

---

## 🧪 Testing & Verification

Run the entire verification suite (all 7 suites execute in under 10 seconds):

```bash
npm test
```

The test harness verifies:
1. `scripts/test_scaffolding.mjs` — CSS variables, typography, and palette foundations.
2. `scripts/test_canvas.mjs` — Gaze angle mapping, wrapping physics, and step governor math.
3. `scripts/test_hero.mjs` — Hero structure, SpeechBubble cyclic rotation, and sound hooks.
4. `scripts/test_projects.mjs` — Project schemas, GitHub URL validations, modal rendering, and filtering logic across all 8 projects.
5. `scripts/test_about.mjs` — Skills taxonomy and responsive grid rendering.
6. `scripts/test_app.mjs` — Contact modal, Resume/CV print layouts, and App root orchestration.
7. `scripts/test_frames.py` — Integrity check of all 65 WebP frames.

---

## 📦 Production Build & Deployment

Compile the optimized production bundle:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

### Deploy to Vercel
1. Import this repository into [Vercel](https://vercel.com/new).
2. Framework preset is auto-detected as **Vite**.
3. Click **Deploy** — your portfolio is live in seconds with automatic deployments on every `git push`!

---

## 📁 Repository Structure

```text
khushi-portfolio/
├── public/
│   └── frames/                  # 64 raw 1080p WebP gaze frames + center.webp
├── scripts/
│   ├── extract_khushi_frames.py # Frame extraction pipeline with watermark inpainting
│   ├── test_scaffolding.mjs     # Foundation & CSS tokens tests
│   ├── test_canvas.mjs          # Canvas engine & trigonometry math tests
│   ├── test_hero.mjs            # Hero & speech bubble interaction tests
│   ├── test_projects.mjs        # Projects section & modal tests (8 projects)
│   ├── test_about.mjs           # About section & skills taxonomy tests
│   ├── test_app.mjs             # Root app & modal orchestration tests
│   └── test_frames.py           # Frame resolution & integrity verification
├── src/
│   ├── AboutSection.css
│   ├── AboutSection.jsx         # Philosophy & technical skill taxonomy
│   ├── App.jsx                  # Root layout & modal coordinator
│   ├── CharacterCanvas.css
│   ├── CharacterCanvas.jsx      # 60 FPS gaze tracking canvas engine
│   ├── ContactModal.css
│   ├── ContactModal.jsx         # Direct message modal dialog
│   ├── ContactSection.css
│   ├── ContactSection.jsx       # Footer & contact call-to-action
│   ├── HeroSection.css
│   ├── HeroSection.jsx          # Full-viewport hero with speech bubble & nav
│   ├── ProjectModal.css
│   ├── ProjectModal.jsx         # Detailed project modal with features & links
│   ├── ProjectsSection.css
│   ├── ProjectsSection.jsx      # Featured work grid with 8 projects & filters
│   ├── ResumeModal.css
│   ├── ResumeModal.jsx          # Printable Curriculum Vitae modal
│   ├── soundEffects.js          # Procedural Web Audio API sound generator
│   ├── SpeechBubble.css
│   ├── SpeechBubble.jsx         # Interactive floating thought bubble
│   ├── useLenis.js              # Lenis momentum smooth scroll hook
│   ├── useScrollReveal.js       # IntersectionObserver entrance animator
│   ├── index.css                # Global tokens, luxury film grain & reset
│   └── main.jsx                 # React root entrypoint
├── package.json
└── README.md
```

---

## 📄 License & Credits

- **Author**: [khushigsd2924-design](https://github.com/khushigsd2924-design)
- **License**: This project is licensed under the [MIT License](LICENSE).
