# Ameen Yousef — Portfolio

A single-file portfolio site. Everything is in `index.html`. No build tools, no Node — just static files on GitHub Pages.

## Folder layout
```
your-repo/
├── index.html          ← the whole site
├── img/                ← all photos go here
│   ├── about.jpg
│   ├── modular-robot-1.jpg
│   ├── modular-robot-2.jpg
│   └── ...
└── file/
    └── resume.pdf      ← your CV (the "Download CV" button)
```

## How to add or edit a project
1. Open `index.html`.
2. Find the block that starts with `const PROJECTS = [`.
3. Copy one `{ ... }` project block, paste it, and edit the fields.

Field rules:
- **category** must be exactly one of: `Machine Design`, `Robotics`, `Make for fun` (filter tabs are built automatically).
- **cover** — the card image, e.g. `img/3d-mixer-1.jpg`.
- **images** — array of photos for the slideshow, e.g. `["img/3d-mixer-1.jpg","img/3d-mixer-2.jpg"]`.
- **video** — a YouTube **ID only**. For `https://www.youtube.com/watch?v=ABC123XYZ` you write `video:"ABC123XYZ"`. Leave `""` if there's no video.
- **link** — external write-up (Fab Academy etc.) or `""`.
- **wip** — `true` shows a small "WIP" badge for unpublished projects.

Missing photos show a tidy "ADD IMAGE" placeholder, so the site never looks broken while you fill it in.

## Photos — keep them light
- Resize to ~1600px on the long edge and compress (squoosh.app is free).
- Keep all project photos roughly the same shape (4:3 looks best on the cards).

## Videos — DO NOT put video files in the repo
Upload each clip to **YouTube → set Visibility to "Unlisted"**, then copy the ID into the project's `video` field. This keeps the site fast and within GitHub's limits.

## Deploy (clean URL)
1. Rename your repo to **`aminyousef.github.io`** — GitHub then serves it at `https://aminyousef.github.io/` (no typo'd subfolder).
2. Put `index.html`, the `img/` folder, and `file/` folder in the repo root.
3. Settings → Pages → Branch: `main` / root → Save.
