# Augmented Reality / Spatial Portfolio Experiment

A small browser-based spatial experience, with two separate entry points:

- **[Desktop scene preview](https://hak3du.github.io/AugmentedReality/preview.html)** — camera-free, orbitable 3D scene for desktop and mobile. Drag to orbit, scroll to zoom, or use the preset camera controls. This preview is not marker-tracked AR.
- **[Marker-based AR entry](https://hak3du.github.io/AugmentedReality/)** — the camera-launched A-Frame/AR.js experience, with a floating intro-video panel and a marker-triggered spatial sequence.

## Current assets

- `assets/marker.patt`: marker pattern used by the existing AR entry.
- [Printable marker SVG](assets/printable-marker.svg): reconstructed from the first 16×16 grayscale sample matrix in `marker.patt`, with a high-contrast border. Print at a square aspect ratio, keep the full black border visible, and test recognition on the target phone; this reconstructed print asset is not yet validated against a physical device.
- `assets/audi.glb`: currently only 2 bytes and **not a usable GLB model**. Do not rely on it in the scene until it is replaced with a valid model and checked in a GLB viewer.
- `preview.html`: independent, camera-free visualisation. It deliberately does not load the webcam.

## How to verify

1. Open the desktop preview on a modern browser and confirm the scene renders.
2. Use **Front / Left / Right / Back / Top / Reset**; verify the scene can be inspected from all sides.
3. Drag on the canvas and scroll to orbit/zoom.
4. Confirm no camera permission prompt appears on the desktop preview.
5. Open the marker-based AR entry separately on a supported mobile browser over HTTPS.
6. Grant camera permission only if you intend to test marker tracking; present the correct pattern marker to the camera.
7. Test repeated marker detection, marker loss/re-entry, camera denial/retry, video loading, and device performance before calling the AR experience production-ready.

## Important limitations

- The updated AR entry pins A-Frame 1.6.0 and AR.js 3.4.8 to avoid a moving `master` dependency. These versions and the marker workflow still need real-device browser QA.
- A repository file being present does not prove the page runs on every device. The desktop preview and guided AR launch are implemented; live browser/device QA is still required.
- Do not claim production readiness until the marker workflow, permission/error handling, model assets, and mobile behavior are verified.

## Portfolio links

- [Main engineering portfolio](https://hak3du.github.io/portfolio/)
- [Portfolio source and project index](https://github.com/hak3du/portfolio)
- [GitHub profile](https://github.com/hak3du)
