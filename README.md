# TimothyHadfield.github.io

The landing page for my board and card game projects, served at the root of my GitHub
Pages domain: **https://timothyhadfield.github.io/**

## How this works

This repo holds *only* the landing page. Each game keeps its own repository and its own
GitHub Pages deployment, so nothing here needs to stay in sync with any game's code.

Because every project publishes to `timothyhadfield.github.io/<repo-name>/`, this site sits
at the parent path of all of them — a visitor lands here, browses the cards, and clicks
through to whichever game they want.

## Games listed here

| Game | Repository | Live |
|---|---|---|
| Secret Hitler Companion | [secret-hitler-companion](https://github.com/TimothyHadfield/secret-hitler-companion) | [open](https://timothyhadfield.github.io/secret-hitler-companion/) |
| Wavelength | [wavelength](https://github.com/TimothyHadfield/wavelength) | [open](https://timothyhadfield.github.io/wavelength/) |
| Catan Statistics Tracker | [catan-statistics](https://github.com/TimothyHadfield/catan-statistics) | [open](https://timothyhadfield.github.io/catan-statistics/) |
| BANK Game Evolution | [bank-evolution](https://github.com/TimothyHadfield/bank-evolution) | [open](https://timothyhadfield.github.io/bank-evolution/) |
| BANK AI Trainer | [bank-ai-trainer](https://github.com/TimothyHadfield/bank-ai-trainer) | [open](https://timothyhadfield.github.io/bank-ai-trainer/) |
| Venture Cheat | [venture-cheat](https://github.com/TimothyHadfield/venture-cheat) | [open](https://timothyhadfield.github.io/venture-cheat/) |

## Adding a new game

1. Give the game its own repo with an `index.html` at the root.
2. Enable Pages on that repo (Settings → Pages → source: `main`, folder: `/`).
3. Copy an existing `<a class="card">` block in [`index.html`](index.html), change the
   href, emoji, title, description and tags, and push.

That's the whole process — there is no build step and no dependency between the hub and
the games.
