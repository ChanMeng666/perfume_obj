# Perfume 3D Viewer

Interactive browser-based 3D viewer for Perfume (Japanese pop group) dance pose models, built with Three.js. The OBJ model was exported from Blender and contains three members — a-chan, kashiyuka, and nocchi — each rendered in a distinct color.

## Features

- **Three.js WebGL rendering** — smooth 3D visualization in the browser
- **Orbit controls** — rotate (left-click drag), zoom (scroll), pan (right-click drag)
- **Per-member coloring** — a-chan (pink), kashiyuka (blue), nocchi (green)
- **Auto-fit camera** — model is centered and camera adjusts to fit automatically
- **Zero build step** — single HTML file with CDN imports, no bundler required
- **Responsive** — full-screen layout that adapts to any window size

## Model Info

| Property | Value |
|----------|-------|
| File | `perfume_3.obj` |
| Vertices | 15,006 |
| Faces | 30,000 |
| Objects | 3 (a-chan, kashiyuka, nocchi) |
| Source | Blender export |

## Quick Start

A local HTTP server is required because the OBJ file is loaded via fetch.

```bash
# Clone the repository
git clone https://github.com/ChanMeng666/perfume_obj.git
cd perfume_obj

# Start a local server (pick one)
npx serve .          # → http://localhost:3000
# or
python -m http.server 8000  # → http://localhost:8000
```

Open the URL in your browser and the 3D model will load automatically.

## Tech Stack

- [Three.js](https://threejs.org/) v0.160 (via unpkg CDN)
- OBJLoader + OrbitControls (Three.js addons)
- Vanilla HTML / JavaScript — no frameworks or build tools

## Project Structure

```
perfume_obj/
├── index.html       # Three.js viewer (single-page app)
├── perfume_3.obj    # 3D model file (Blender export)
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
