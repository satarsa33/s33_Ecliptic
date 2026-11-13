# S33 - Ecliptic

A generative ambient machine of the **S33** family. Six layers (Drone, Pad, Melody, Texture, Field, Pulse) follow **the Arc**, a curve of intensity over the session, the way the sun follows the ecliptic across the sky.

Runs in Chrome on the Mac; installable as a PWA and works offline.

## How it works

- **Brain** decides what happens and when: the arc and its sections (Emergence, Drift, Bloom, Hollow, Return), harmonic states (Stable, Suspended, Modulating, Dark), modes, voice leading, phrases, rhythms. It only emits events, and every event can be translated into MIDI.
- **Body** turns events into sound with the Web Audio API: analog-style drone and pad, soft FM melody (Glass, Soft Rhodes, Bell, Breath), a granular texture made from the pad's chord, field sounds (wind, rain, tape, surf), a soft euclidean pulse.
- **Face** is the interface: the living arc (what sounded on the left, the forecast on the right), the circle of fifths, five double-ring macros, a six-channel mixer.

The layers listen to each other: the texture thins out when the melody speaks; the pulse arrives only when the arc rises; the field fills the quiet moments.

## Controls

| Control | What it does |
|---|---|
| Density | how many voices, grains, notes and hits |
| Light | brightness of filters and of the mode (Lydian → Phrygian) |
| Tension | richer chords, suspensions, modulations |
| Space | reverb, delay, how present the field is |
| Motion | how often things change, how much they move |

Inner ring = your setting · outer ring = after the arc. Drag, scroll or use the arrow keys; double-click resets.

**Seed**: the same seed with the same settings gives (almost) the same piece.
**Time 4× / 10×**: preview a whole arc quickly; the pulse always stays in real time.

## Recording and sessions

- **● Rec** records the master output. Saving the take gives `audio.wav` (16-bit stereo), `layers.mid` (one track per layer, tempo = pulse BPM, so Logic's grid matches) and `session.json`.
- **Sessions** keeps seed, arc, macros, mix, timbre and position — in the browser, or exported as `.json`.

## Install

1. Upload these files to a GitHub repository and enable GitHub Pages.
2. Open the page in Chrome on the Mac and choose *Install S33 - Ecliptic* in the address bar.

Files: `index.html`, `manifest.json`, `sw.js`, `icons/`.

When you publish an update, bump `CACHE` in `sw.js` (`ecliptic-v1` → `ecliptic-v2`), or the installed app keeps showing the old version.

## Later

Designed to become a module of **S33 - Mother Board**: audio out L/R, MIDI out (to Vega, Hexa, Twin Core), clock in.
