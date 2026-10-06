# Lotus Pond — Gesture-Controlled Interactive 3D Web App

Bloom twelve 3D lotus flowers with just your hands, each one opening from a closed bud through its own growth stages. MediaPipe hand tracking reads your fingers through the webcam while Three.js renders the petals in real time — all in the browser, with no video uploaded.

**Live demo:** https://bhonepyaemin.com/lotus/

## Features

- **12 independent lotus flowers**, each on its own stem, with its own color variety and its own lifecycle.
- **Three growth stages per flower:** Bud Formation → Vegetative Phase → Blooming / Anthesis. The flowers open in a staggered order, so the pond shows buds and blooms at the same time.
- **Procedural 3D petals:** thick, cupped, boat-shaped petals in four layers, pointed teardrop buds, and a raised seed pod with seed bumps and stamens — all generated in code.
- **Natural rendering:** soft shadows between petals, baked ambient occlusion and veins, a velvety petal sheen, and a rim light for translucent-looking edges.
- **Hand gestures:** spread your thumb and index finger to bloom; move your hand to move the flowers.

## Controls

| Input | Action |
|---|---|
| Thumb–index spread (either hand) | Bloom the flowers |
| Move an open hand | Move the flowers |
| Mouse drag / scroll | Orbit / zoom the camera |
| `D` | Toggle the automatic demo cycle |
| `1` / `2` / `3` | Hold at bud / vegetative / full bloom |
| `0` | Back to the cycle |
| `H` | Hide the status overlay |

## Run locally

The camera only works on `localhost` or HTTPS, so serve the folder instead of opening the file directly:

```bash
python -m http.server 8651
```

Then open http://localhost:8651 and allow camera access.

## Tech

Computer Vision · MediaPipe Hand Landmarker · Three.js · WebGL · anime.js · JavaScript

Everything runs client-side; webcam frames never leave the browser.
