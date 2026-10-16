# Game hub (TimothyHadfield.github.io)

Tim's GitHub Pages **root site**: a one-page landing hub that links to his board and card
game projects. Visitors (Tim, friends he plays with) land here and tap through to a game.
Live: https://timothyhadfield.github.io/

Local checkout: `OneDrive\Desktop\my-website\Code Projects\Board and Card Games\Hub`
(the folder name is "Hub", the repo is `TimothyHadfield.github.io`).

## File map
- `index.html`: the whole site. Inline `<style>` (CSS tokens on `:root`, dark only), no JS,
  no external requests. One `<a class="card">` per game inside `<main class="grid">`.
- `README.md`: GitHub showcase (screenshots + table of games with repo and live links).
- `docs/screenshots/desktop.png`, `phone.png`: images used only by the README.
- `progress.md`: handoff notes (state, traps, decisions).

## Games linked (each is its own repo + Pages site at `/<repo>/`)
secret-hitler-companion, wavelength, cribbage, catan-statistics, bank-evolution,
bank-ai-trainer, venture-lab. All 7 live URLs and 7 GitHub repo URLs returned 200 on
2026-10-16. A broken link to any of them counts as a bug in this repo.

## Run locally
`python -m http.server 8113` from the repo root (use the background option), then
`http://localhost:8113/`. No build step, no dependencies.

## Test
No test suite (one static page, no JS). Verify with phone-view:
- `node ~/.claude/tools/phone-view.mjs http://localhost:8113/ --out shot.png` (+ `--desktop`)
- Check: no console errors, no horizontal overflow at 393px, every card link resolves.
- Link check: HEAD request each `https://timothyhadfield.github.io/<repo>/` and
  `https://github.com/TimothyHadfield/<repo>`; expect 200.

## Deploy
Push to `main` -> GitHub Pages serves the repo root as `https://timothyhadfield.github.io/`.
Check with `python ~/.claude/hooks/live-check.py "<checkout>"`.

## Adding a game
Copy an existing `<a class="card">` block (href, emoji, title, description, two tags), and
add a matching row to the README table. Card wording, emoji and tags are Tim's call.

## Traps
- This repo's Pages is the parent path of every other project's site. Renaming or deleting
  a game repo breaks its card here; renaming THIS repo breaks the root domain.
- Do not add a `404.html` casually: a root-site 404 page may also be served for missing
  paths under project sites that have no 404 of their own (reasoned, not tested).
- The README screenshots are static images; update them if the hub's look changes.
- The hub lists board/card games only. Tim's other apps (fitness, school, etc.) are not
  on it; adding them is Tim's decision, not a fix.
