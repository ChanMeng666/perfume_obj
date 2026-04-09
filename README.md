# Perfume 3D Viewer

**[Live Demo](https://perfume-3d-viewer.pages.dev)**

Interactive browser-based 3D viewer for Perfume (Japanese pop group) dance pose models, built with Three.js. The OBJ model was exported from Blender and contains three members — a-chan, kashiyuka, and nocchi — each rendered in a distinct color with PBR materials and cinematic lighting.

## Features

- **Three.js WebGL rendering** — PBR materials with ACES filmic tone mapping
- **Cinematic lighting** — 5-light rig with warm key, cool fill, rim, and hemisphere bounce
- **Orbit controls** — rotate (drag), zoom (scroll), pan (right-drag), auto-rotation
- **Per-member coloring** — a-chan (pink), kashiyuka (blue), nocchi (green)
- **Glass-morphism UI** — branded overlays with member legend and controls hints
- **Auto-fit camera** — model is centered and camera adjusts to fit automatically
- **Responsive** — full-screen layout with mobile-optimized FOV and touch controls
- **Zero build step** — single HTML file with CDN imports, no bundler required

## Model Info

| Property | Value |
|----------|-------|
| File | `perfume_3.obj` |
| Vertices | 15,006 |
| Faces | 30,000 |
| Objects | 3 (a-chan, kashiyuka, nocchi) |
| Source | Blender export |

## Quick Start

```bash
# Clone the repository
git clone https://github.com/ChanMeng666/perfume_obj.git
cd perfume_obj

# Install dependencies (only needed for deployment)
npm install

# Start a local server
npx serve .          # → http://localhost:3000
```

Open the URL in your browser and the 3D model will load automatically.

## Deployment

Hosted on [Cloudflare Pages](https://pages.cloudflare.com/):

```bash
npx wrangler login
npx wrangler pages deploy . --project-name=perfume-3d-viewer
```

## Tech Stack

- [Three.js](https://threejs.org/) v0.160 (via unpkg CDN)
- OBJLoader + OrbitControls (Three.js addons)
- Vanilla HTML / JavaScript — no frameworks or build tools

## Project Structure

```
perfume_obj/
├── index.html       # Three.js viewer (single-page app)
├── perfume_3.obj    # 3D model file (Blender export)
├── package.json     # Deploy scripts and wrangler dependency
└── README.md
```

## Controls

| Action | Input |
|--------|-------|
| Rotate | Left-click + drag |
| Zoom | Scroll wheel |
| Pan | Right-click + drag |

## License

This project is for personal/educational use. The Perfume motion capture data originates from publicly shared resources by Perfume Global Site.
