# Go-Go Royalty VR — Site Package

## Folder Structure

```
site/
├── index.html              ← Main page (45 KB)
├── README.md
└── assets/
    └── 3d/
        ├── scene.gltf      ← 3D model manifest (9.5 KB)
        ├── scene.bin       ← Geometry data (4.8 MB)
        └── textures/       ← WebP textures (218 KB total)
            ├── wire_056035148_baseColor.webp
            ├── wire_085028177_baseColor.webp
            ├── wire_126042025_baseColor.webp
            ├── wire_177161249_baseColor.webp
            └── wire_194045245_baseColor.webp
```

## GitHub Pages Deployment

1. Push ALL files maintaining this exact folder structure
2. Enable GitHub Pages on your repo (Settings → Pages → main branch)
3. Site will be live at: https://dfrazier205.github.io/[repo-name]/

```bash
git init
git add .
git commit -m "Go-Go Royalty VR site"
git remote add origin https://github.com/DFrazier205/[repo-name].git
git push -u origin main
```

## File Sizes

| File              | Size    | Notes                          |
|-------------------|---------|--------------------------------|
| index.html        | 45 KB   | Full page, all CSS + JS inline |
| scene.gltf        | 9.5 KB  | Model manifest                 |
| scene.bin         | 4.8 MB  | Geometry (loads progressively) |
| textures (WebP)   | 218 KB  | Converted from 695 KB JPEG     |
| **Total**         | **~5.1 MB** |                            |

## Browser Download on First Visit

| Asset             | Size    | How                            |
|-------------------|---------|--------------------------------|
| index.html        | 45 KB   | Immediate                      |
| Three.js (CDN)    | ~580 KB | Parallel, cached after 1st load|
| Google Fonts      | ~20 KB  | Non-blocking, cached           |
| scene.gltf        | 9.5 KB  | After page load                |
| scene.bin         | 4.8 MB  | Progressive, background        |
| textures          | 218 KB  | Progressive, background        |
| Hero video        | ~4 MB   | Streamed, non-blocking         |

Page text and layout appear **instantly** — 3D model fades in once loaded.

## Updating the YouTube Video Links

In index.html, search for `exp-card-link` to find each card's href.
Currently live: Card 01 (TCB Live) → https://youtu.be/q7kwfxjzA0Q
