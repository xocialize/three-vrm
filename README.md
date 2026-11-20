# MToonNodeMaterial: shadows darken instead of shading

A repro for the issue on pixiv/three-vrm. `shadow.html` renders an MToon sphere, shadowed by a box and by itself, under one shadow-casting light (`?light=directional|spot|point`), with `MToonMaterial` on `WebGLRenderer` and with `MToonNodeMaterial` on `WebGPURenderer`, and compares the two frames over the object's pixels. It loads three r186.0 and `@pixiv/three-vrm` 3.5.5 from unpkg; serve the folder over http and open it in a browser with WebGPU.

The pictures (`directional.png`, `spot.png`, `point.png`): `MToonMaterial` (WebGL); `MToonNodeMaterial` as published (3.5.5, and the same with #1878); `MToonNodeMaterial` with the suggested fix. `results-chromium.json` has the numbers (headless Chrome for Testing 156 on Metal, Apple M5 Max, macOS 27.3).
