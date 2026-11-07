# AGENTS.md

CYBER SMASH: a 2D browser game in a single `index.html` (HTML, CSS and vanilla JS on a `<canvas>`), a parody of the 90s "destroy the car" bonus stage. Published on GitHub Pages.

## Commands
- Run: open `index.html` in a browser, or serve the folder with `python3 -m http.server 8080`
- Install, build, test, lint: none exist

## Conventions
- Structure: `index.html` is the whole game; `docs/screenshots/` holds the README images; `README.md` documents controls and fighters.
- Single HTML file that runs by opening it. No external images, sprites, fonts, libraries or network requests. Everything is drawn with canvas shapes and all sound comes from the Web Audio API.
- Retro 16-bit look: chunky pixel-style shapes, bold colors, harbor background.
- Chibi caricatures: funny, never mean-spirited. Parody names only, no real names, no copied sprites, music or logos.
- Responsive canvas that scales to the window keeping aspect ratio.
- Comment the code clearly. No placeholder logic: the game must be fully playable start to finish.
- Gameplay spec:
  - 6 fighters, each with a unique special, look and win/lose line.
  - Controls: Left/Right or A/D move; J punch (1x); K kick (1.5x, longer reach); L special (3x, 3s cooldown); Space/Enter confirm; M mute.
  - 40 s timer; the truck ("CYBERCHUNK") has a health bar and 4 damage stages.
  - Hits only count in range.
  - Score: points per hit; PERFECT! bonus is remaining seconds x 1000; results screen with retry and fighter change.
- Workflow per PR: branch from latest `main`, implement only that PR's scope with clear commits, check it in a browser (or a syntax check), open the PR with `gh pr create` (what changed and how to test), then squash-merge.

## Boundaries
- Always: keep the game playable end to end after every change.
- Ask first: adding any external file, library or network call (the rules forbid them).
- Never: commit secrets or read .env files; copy existing games' art, names or music.
