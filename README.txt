# System Index | Computational Design Portfolio

This repository contains the front-end code and lightweight media assets for my computational design and architectural optimization portfolio. 



🌐 **Live URL:** [alimzannar.com]

---

# System Index | Ali Mzannar

This repository contains the front-end code and lightweight media assets for my computational design and architectural optimization portfolio. 

Engineered with a Brutalist, MIT Media Lab aesthetic, the site relies on massive typography, strict spatial alignments, and custom physics-based cursor tracking to reveal architectural media on hover. It is built entirely with zero external dependencies (Vanilla HTML, CSS, JavaScript) to ensure maximum performance, instant global load times, and frictionless maintenance.

🌐 **Live System:** [alimzannar.com]

---

## 🏗️ Architecture & Directory Structure

The portfolio operates on a split-level architecture. The main canvas utilizes a localized JSON data engine and dynamic DOM routing, while specific projects are housed in dedicated sub-directories.

```text
📦 repository-root
 ┣ 📂 assets
 ┃ ┣ 📂 videos               (Optimized .mp4 loops strictly < 5MB)
 ┃ ┗ 📂 images               (Optimized .jpg/.webp static renders)
 ┣ 📂 projects               (Dedicated deep-dive routing pages)
 ┃ ┣ 📜 00-project.html      
 ┃ ┣ 📜 01-project.html
 ┣ 📜 style.css              (Unified Master Stylesheet)
 ┣ 📜 index.html             (Main Canvas & Data Engine)
 ┗ 📜 .gitignore             (Security protocol preventing CAD uploads)