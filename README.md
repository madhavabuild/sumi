# A Universe Named Sumi

A cinematic, interactive love letter — built as a small universe of starlight, animated anime skies, and quiet surprises. Made for Sumi, from Madhava.

## Run it

The site uses ES modules, so serve the folder instead of double-clicking `index.html`.

```bash
cd sumi-universe
python -m http.server 5500
```

Then open <http://localhost:5500>.

You can also use the VS Code **Live Server** extension. An internet connection is needed the first time for Google Fonts and the Three.js CDN.

## The experience

1. **Opening veil** — a moonlit title screen with a choice: enter with ambient sound, or wander in quietly.
2. **Prologue** — a slow Ken Burns sky, drifting sakura, and a cursor that leaves starlight.
3. **01 · The sky** — a word-by-word quote over an aurora sea.
4. **02 · The stars** — light five stars to draw a constellation. Each one opens a message; light all five and a hidden sixth star awakens.
5. **03 · The wishes** — tap the moonlit meadow to release glowing wish lanterns, each carrying a whispered wish.
6. **04 · The letter** — break the wax seal to unfold a handwritten letter.
7. **05 · Your name** — thousands of particles assemble into a constellation spelling **SUMI**.
8. **06 · Forever** — make a wish and let the sky answer.

## Hidden things

- Type `sumi` anywhere on the page for a tiny celebration.
- The ambient track is generated live with the Web Audio API — a soft pad plus occasional bell tones. There is no audio file.
- The star map, lanterns, letter, and name constellation are all keyboard-friendly.

## Files

```text
sumi-universe/
├── index.html
├── style.css
├── script.js
├── assets/
│   ├── hero-sky.png      (generated anime sky)
│   ├── garden-night.png  (generated moonlit meadow)
│   └── aurora-sea.png    (generated aurora seascape)
└── README.md
```

## Personalize it

- All copy lives in `index.html` — names, quotes, star messages, wishes, and the letter.
- Star positions and messages are in `initConstellation()` inside `script.js`.
- Wish-lantern lines are in `initLanterns()`.
- Colors and fonts are defined as CSS variables at the top of `style.css`.

## Technical notes

- Vanilla JavaScript, CSS, and Three.js for the fixed starfield; everything else is hand-rolled Canvas/CSS animation.
- Respects `prefers-reduced-motion` and includes visible focus styles.
- No analytics, no storage, no personal data. Everything stays in the browser.
- Artwork was generated for this project; fonts are Cormorant Garamond, DM Sans, and Shippori Mincho via Google Fonts.
