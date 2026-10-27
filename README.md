# StressLens

A 3D digital twin that makes the invisible stress inside warehouse pallet racking visible, before a beam fails.

Built for the Youth Speak Forum 2026 · Youth Innovation Challenge, Day 2 ("Making the invisible visible", SDG 7 · 9 · 11), Expo City Dubai, 28 October 2026.

**Live demo:** enable GitHub Pages on this repository (Settings → Pages → Deploy from branch → `main` / root) and the site is served at `https://<your-username>.github.io/stresslens/`.

## What it shows

1. **Today.** A forklift puts a third, heavier pallet on a beam already near its rating. Nothing warns anyone. Eleven days later, on the night shift, the beam gives way.
2. **Rewind, with StressLens.** The same morning, with one strain sensor at mid-span of every beam. The twin predicts 110% before the pallet touches steel; the forklift screen refuses the put-away, the control room gets the alert, a maintenance ticket opens.
3. **Free play.** Tap any level to load it and watch utilisation climb. Shake or tilt the phone to feed the vibration sensors.

## How it works

- Sensors go where a finite-element model says the structure bends most: mid-span of each beam, base of each upright. One strain gauge and one accelerometer per critical point.
- Beam utilisation = maximum bending moment ÷ rated moment, computed live for a simply supported beam with point loads.
- Alerts at 75% (watch) and 90% (block put-away, open ticket).

All loads, readings and costs in the demo are simulated.

## Running it

Open `index.html` in any modern browser. No build step. The only external dependency is three.js r128 from cdnjs. Phone tilt needs the page served over HTTPS (GitHub Pages is fine) and, on iOS, a tap on "Enable tilt".

## Author

Kareena Mueenuddin · B.Tech Mechatronics Engineering, Amity University Dubai
