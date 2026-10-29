# Solar system explorer

A single-page Three.js educational visualization with time controls, orbit paths, body selection, and first-person travel.

## Run locally

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/solar_system.html`. A WebGL-capable desktop browser and network access are required: the import map loads Three.js 0.161.0 from unpkg. There is no npm build step.

Select a body, use Find/Follow or the travel controls, and change the time-rate slider to pause, reverse, or accelerate orbital motion. WASD moves horizontally; Space/Shift moves vertically. The page lists its other keyboard controls. Mouse/pointer-lock interaction makes this primarily a desktop experiment.

## Model and limits

`solar_system.html` uses mean orbital elements at J2000 with a Kepler solver for solar orbits and circular approximations for moons. Sizes and distances share a 10,000 km/unit scale; an optional enlargement toggle helps visibility. This is **educational**, not ephemeris-grade astronomy, an N-body integration, or physically realistic faster-than-light travel.

The old hosted address is not a canonical portfolio link; local serving is the reproducible entry point. A local headless Chromium smoke check rendered one canvas and clicked Find without page errors; module syntax also passed. This is not full interaction or astronomical validation. MIT: [LICENSE](LICENSE), with Three.js remaining separately licensed upstream.
