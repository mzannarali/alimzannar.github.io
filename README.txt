# Ali Mzannar | Computational Portfolio Architecture

This repository contains the front-end architecture for a data-driven computational design portfolio. It is engineered as a lightweight, Headless CMS without the need for a backend server or complex build tools.

## System Architecture

Instead of hardcoding individual HTML pages, the site relies on a **Master JSON Database** (`portfolio-db.json`) and an asynchronous JavaScript Fetch engine to dynamically render all content.

* **`index.html`**: Dynamically reads the JSON file to generate the Research Track directory. It features a CSS Grid-powered animated accordion that reveals ultra-wide cinematic video previews on hover without heavy JavaScript layout calculations.
* **`projects/project.html` (Dynamic Router)**: A universal sub-page receiver. Instead of duplicating HTML files for every research track, this single file acts as a dynamic template. It reads the URL parameter (e.g., `?id=geometry-rationalization`), queries the JSON database, and automatically builds the correct Hero Headers, Meta Data, Institutional Logos, and populates a grid with stacked media and Brutalist Lightbox Modals.
* **Unified Voxel Engine**: A custom DOM-manipulation script that physically breaks typography into 14px CSS grids, synchronized perfectly with an HTML5 `<canvas>` Cartesian noise engine.

---

## Content Management Workflow

### How to Add a New Individual Project (Vault Item)
You **do not** need to edit any HTML files to add new project videos, renders, or text. The entire website is driven by the database.

1. Drop your `.mp4` and/or `.jpg` files into the appropriate folders inside `/assets/`. *(Note: Keep videos under 3MB and ensure media is exported at a 16:9 aspect ratio for perfect grid alignment).*
2. Open `portfolio-db.json`.
3. Locate the correct Research Track object via its `trackId` (e.g., `"geometry-rationalization"`).
4. Add a new data object to the `vaultItems` array. 
5. Note the use of the `gallery` array, which supports unlimited images inside the project modal:

```json
{
    "title": "Your New Project Name",
    "software": "Python / Grasshopper / C#",
    "team": "Computational Design: Ali Mzannar | Lead Architects: BAD",
    "description": "Technical description of the algorithmic logic, systems architecture, or performance optimization.",
    "videoSrc": "assets/videos/your-video.mp4",
    "gallery": [
        "assets/images/render-01.jpg",
        "assets/images/render-02.jpg"
    ],
    "projectLogos": [
        "assets/logo/BAD.jpg"
    ]
}