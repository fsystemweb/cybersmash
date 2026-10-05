# CYBER SMASH — project rules

## What this is
A 2D browser game in a **single `index.html`** (HTML + CSS + vanilla JS on `<canvas>`).
Parody of the 90s "destroy the car" bonus stage. All art and characters are original.

## Hard rules
- Single HTML file, runs by opening it. **No external images, sprites, fonts, libraries or network requests.**
  Everything is drawn with canvas shapes; all sound comes from the Web Audio API.
- Retro 16-bit look: chunky pixel-style shapes, bold colors, harbor background (crates, cargo ships, nervous salesman).
- Chibi caricatures (big head, small body): funny, never mean-spirited. Parody names only, no real names, no copied sprites/music/logos.
- Responsive canvas that scales to the window keeping aspect ratio.
- Comment the code clearly. No placeholder logic: the game must be fully playable start to finish.

## Gameplay spec
- 6 fighters: Donald Tromp, Elon Muskrat, Mark Zuckerbot, Demis Hassabyte, Jensen Hwatt, Sam Oldman — each with a unique special, look, and win/lose line.
- Controls: Left/Right or A/D move; J punch (1x); K kick (1.5x, longer reach); L special (3x, 3s cooldown meter); Space/Enter confirm; M mute.
- 40 s timer. Truck ("CYBERCHUNK") has a health bar and 4 damage stages (windows crack, dents, panels fall off, collapse + smoking battery).
- Hits only count in range. Juice: screen shake, freeze frames, debris, comic text (BONK!, CRUNCH!, RECALL!).
- Scoring: points per hit by damage; PERFECT! bonus = remaining seconds x 1000; SALE CANCELLED with defeat line on timeout; results screen (score, time left, hits), retry / change fighter, session best score.

## Workflow (every PR)
1. Branch from latest `main`. 2. Implement only that PR's scope, clear commits.
3. Test in headless Chrome / syntax check, fix errors. 4. Push, `gh pr create` (what changed + how to test).
5. `gh pr merge --squash --delete-branch`, pull `main`, next PR.

## PR plan
1 skeleton/loop/scaling · 2 truck + damage stages · 3 fighter, punch/kick, hits · 4 timer/score/end screens ·
5 character select · 6 specials + cooldown · 7 juice · 8 audio + mute · 9 polish, README screenshots, GitHub Pages.
