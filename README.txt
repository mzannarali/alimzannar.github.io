# System Index | Computational Design Portfolio

This repository contains the front-end code and lightweight media assets for my computational design and architectural optimization portfolio. 



🌐 **Live URL:** [alimzannar.com]

---

## 🏗️ System Architecture

This portfolio operates on a "Headless-Style JSON Engine" contained within a single-file architecture. 

* **The Front-End:** A custom infinite-scroll timeline with node-based UI, built entirely in vanilla CSS and JavaScript.
* **The Data:** Projects are not hard-coded into the HTML. They are rendered dynamically via a JSON object array located at the bottom of the `index.html` file. 



**CRITICAL NOTE FOR REPOSITORY MANAGEMENT:** This repository is strictly the **Live Stage**. It is designed for maximum speed and global CDN deployment via GitHub Pages. 

Heavy AEC source files must never be committed to this repository. 
* **Zone A (Archive):** Raw `.3dm`, `.gh`, `.py`, and 4K renders remain on external/cloud storage.
* **Zone B (This Repo):** Only the `index.html` file and optimized web media (Media files must be `.mp4` or `.webp` and strictly **under 5MB**). 

A `.gitignore` file is actively enforcing these limits to prevent repository corruption from heavy CAD files.

---

## 🔄 How to Add a New Project

To publish a new workflow or project to the live timeline, follow this two-step process:

### 1. Add the Media
Drop your optimized looping video (`.mp4`) or thumbnail (`.jpg`/`.webp`) into the repository's media folder. Remember to use machine-readable naming conventions (e.g., `005-facade-optimization.mp4`).

### 2. Update the Data Engine
Open `index.html`, scroll to the `projectData` array in the `<script>` section, and append a new JSON block:

```json
{
    "id": "005",
    "title": "Project Title Here",
    "date": "2026.07",
    "category": "optimization", 
    "metric": "CUSTOM_METRIC: 100%",
    "desc": "A concise, technical description of the computational problem and algorithm used.",
    "mediaSrc": "005-facade-optimization.mp4"
}