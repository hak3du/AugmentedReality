# Augmented Reality / Spatial Portfolio Experiment

A small browser-based spatial experience, with two separate entry points:

- **[Desktop scene preview](https://hak3du.github.io/AugmentedReality/preview.html)** — camera-free, orbitable 3D scene for desktop and mobile. Drag to orbit, scroll to zoom, or use the preset camera controls. This preview is not marker-tracked AR.
- **[Marker-based AR entry](https://hak3du.github.io/AugmentedReality/)** — the existing A-Frame/AR.js experience, which requests camera access to detect a printed pattern marker.

## Current assets

- `assets/marker.patt`: marker pattern used by the existing AR entry.
- `assets/audi.glb`: currently only 2 bytes and **not a usable GLB model**. Do not rely on it in the scene until it is replaced with a valid model and checked in a GLB viewer.
- `preview.html`: independent, camera-free visualisation. It deliberately does not load the webcam.

## How to verify

1. Open the desktop preview on a modern browser and confirm the scene renders.
2. Use **Front / Left / Right / Back / Top / Reset**; verify the scene can be inspected from all sides.
3. Drag on the canvas and scroll to orbit/zoom.
4. Confirm no camera permission prompt appears on the desktop preview.
5. Open the marker-based AR entry separately on a supported mobile browser over HTTPS.
6. Grant camera permission only if you intend to test marker tracking; present the correct pattern marker to the camera.
7. Test repeated marker detection, leaving/re-entering the marker, camera denial, and device performance before calling the AR experience production-ready.

## Important limitations

- The original AR entry currently references A-Frame 1.4.2 and an AR.js `master` URL. Pinning and testing known dependency versions is a follow-up before production use.
- A repository file being present does not prove the page runs on every device. The desktop preview has been added and statically inspected; live browser/device QA is still required.
- Do not claim production readiness until the marker workflow, permission/error handling, model assets, and mobile behavior are verified.

## Portfolio links

- [Main engineering portfolio](https://hak3du.github.io/portfolio/)
- [Portfolio source and project index](https://github.com/hak3du/portfolio)
- [GitHub profile](https://github.com/hak3du)
