# Ali Mzannar | Computational Portfolio Architecture

This repository contains the front-end architecture for a data-driven computational design portfolio. It is engineered as a lightweight, Headless CMS without the need for a backend server.

## System Architecture

Instead of hardcoding individual HTML pages, the site relies on a **Master JSON Database** (`portfolio-db.json`) and an asynchronous JavaScript Fetch engine. 

* **`index.HTML`**: Dynamically reads the JSON file to generate the Research Track directory and binds spatial intersection listeners for hover-state video previews.
* **`projects/_TEMPLATE.HTML`**: A universal sub-page receiver. By changing a single variable at the top of the script (`CURRENT_TRACK_ID`), the page queries the JSON database, builds the correct Hero Headers, Meta Data, and populates a Masonry Grid with stacked media and Brutalist Lightbox Modals.
* **Unified Voxel Engine**: A custom DOM-manipulation script that physically breaks typography into 14px CSS grids, synchronized perfectly with an HTML5 `<canvas>` Cartesian noise engine.

---

## Content Management Workflow

### How to Add a New Individual Project (Sub-Work)
You **do not** need to edit any HTML files to add new project videos or renders.

1. Drop your `.mp4` and/or `.jpg` files into the appropriate folder inside `/assets/`.
2. Open `portfolio-db.json`.
3. Locate the correct `trackId` (e.g., `"robotic-fabrication"`).
4. Add a new object to the `vaultItems` array:
```json
{
    "title": "Your New Project Name",
    "software": "Python / Grasshopper",
    "team": "Your Name, Collaborator",
    "description": "Technical description of the script or fabrication logic.",
    "videoSrc": "assets/videos/your-video.mp4",
    "renderSrc": "assets/images/your-render.jpg"
}