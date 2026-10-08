# Racing Simulator

A premium 3D racing simulator in a single `index.html` (Three.js, WebGL, ES modules, no build step, no backend).
Four AI-controlled cars (or three AI + one player) race on spline-based circuits. The result comes from a real simulation: physics, racing lines, AI decisions, checkpoints and timing.

## Run

```bash
npx http-server .     # then open http://localhost:8080
```

Three.js 0.170.0 and its addons load from jsDelivr through an import map, so the page needs internet access.

## Features

- **4 circuits**: Coastal, Desert, Mountain, Night City. Each has elevation changes, banking, curbs, gravel traps, a pit lane, grandstands, floodlights, advertising boards and a start-light gantry. New tracks plug in through `createTrack(config)`.
- **4 vehicle classes**: Formula, GT, Supercar, Hypercar, all with fictional designs. Bodies are lofted procedurally, with PBR paint, carbon, glass, brake discs that glow under heavy braking, visible suspension movement, and headlights and brake lights.
- **Garage**: a setup-point budget of 100/100 shared across six parameters, tires (Soft/Medium/Hard/Wet), pit strategy (none/1/2 stops), livery, number, driver personality with star ratings, AI or player control. The 3D preview updates live.
- **Physics** (fixed 120 Hz): friction circle, speed-dependent downforce, drag and slipstream, gearbox, tire wear and temperature, damage, rain grip, collisions between cars and with barriers, and recovery for stuck cars.
- **AI**: follows a minimum-curvature racing line using a speed profile with braking points. It overtakes on the inside or outside, defends without zig-zagging, and occasionally makes mistakes. Four personalities and four difficulty levels; difficulty changes reaction time, precision and mistakes, never engine power.
- **Race**: formation, five-light start, false-start penalty, sequential checkpoints, live gaps, minimap, event feed, BATTLE FOR P1 and FINAL LAP banners, pit stops, track-limit penalties, results screen with statistics.
- **Cameras**: Chase, Race, Cockpit, Trackside, Top and Action (an automatic director). Transitions are smooth, with cinematic shots for key moments.
- **Replay + highlights** from recorded telemetry.
- **Weather and time of day**: dry/cloudy/rain (rain particles, wet asphalt, spray) and day/sunset/night (floodlights, headlights).
- **Procedural Web Audio**: engines with Doppler, tire squeal, curbs, wind, rain, crowd, the pit lane, the start and the finish.
- **Settings, localStorage saves, automatic quality reduction when frame rate drops, F3 debug view, performance overlay.**

## Controls

| Key | Action |
|---|---|
| `C` / `Shift+C` | Next / previous camera |
| `1`–`4`, `Tab` | Choose which car to follow |
| `Esc` | Pause |
| `H` | Hide the HUD |
| `F3` | Debug view (racing line, checkpoints, braking points, AI targets, velocity, collisions, track limits) |
| `` ` `` | Performance overlay |
| `]` (in debug mode) | Simulation speed 1×/2×/4× |
| `W A S D` / arrows | Drive (when a car is set to PLAYER), `P` to request a pit stop |

## Tests

`index.html?simtest&races=2&laps=4` runs full races headless (no rendering) and prints integrity metrics to the console: NaN checks, recoveries, collisions, overtakes, results.
`index.html?autostart` starts a Quick Race immediately.
