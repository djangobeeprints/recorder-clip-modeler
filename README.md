# Recorder Clip Modeler

An interactive three.js tool for designing a 3D-printable tapered
sleeve ("clip") that slips over the barrel of a plastic recorder, as
a base for a note-identification aid.

## Running it

No build step — it's a single self-contained HTML file that loads
three.js from a CDN. Just open `index.html` in a browser, or serve
the folder with any static file server (e.g. `python3 -m http.server`)
and visit it in a browser.

If you push this repo to GitHub, enabling **GitHub Pages** (Settings
→ Pages → deploy from the `main` branch, root folder) will host it
at a public URL automatically, since the entry file is `index.html`.

## Current parameters

The model takes four adjustable inputs, all in millimeters:

- Top inner circumference
- Bottom inner circumference
- Clip length (distance between top and bottom)
- Wall thickness

From these it derives a tapered tube (via a closed lathe profile:
outer wall, top rim, inner wall, bottom rim) and displays derived
diameters, outer circumferences, and the taper half-angle.

Starting measurements: 64mm inner circumference at the top, 60mm
60mm 73mm down.

## Status

Early-stage geometry verification tool. More features (STL export,
a reference barrel overlay for checking clearance, multi-segment
profiles, etc.) are planned.
