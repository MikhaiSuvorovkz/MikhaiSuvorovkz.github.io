# Project Overview

Last updated: 2026-07-09

## What this repo is

Static GitHub Pages site for `Wild Horse Simulator Family 3D`
(`magic.horse.simulator.free.sim.games.kids`), `Winter Tiger Family Simulator`
(`unimix.studio.winter.tiger.family.simulator`), `Fox Family Simulator`
(`unimix.studio.fox.family.simulator`), `Panther Family Simulator`
(`unimix.studio.panther.family.simulator`), and `Wolf Family Simulator`
(`unimix.studio.wolf.simulator`).

## Live URLs

- Site: `https://mikhaisuvorovkz.github.io/`
- Wild Horse Privacy Policy: `https://mikhaisuvorovkz.github.io/privacy-policy/`
- Winter Tiger Privacy Policy: `https://mikhaisuvorovkz.github.io/winter-tiger-family-simulator/privacy-policy/`
- Fox Privacy Policy: `https://mikhaisuvorovkz.github.io/fox-family-simulator/privacy-policy/`
- Panther Privacy Policy: `https://mikhaisuvorovkz.github.io/panther-family-simulator/privacy-policy/`
- Wolf Privacy Policy: `https://mikhaisuvorovkz.github.io/wolf-simulator/privacy-policy/`
- app-ads.txt: `https://mikhaisuvorovkz.github.io/app-ads.txt`
- Wild Horse Google Play: `https://play.google.com/store/apps/details?id=magic.horse.simulator.free.sim.games.kids`
- Winter Tiger Google Play: `https://play.google.com/store/apps/details?id=unimix.studio.winter.tiger.family.simulator`
- Fox Google Play: `https://play.google.com/store/apps/details?id=unimix.studio.fox.family.simulator`
- Panther Google Play: `https://play.google.com/store/apps/details?id=unimix.studio.panther.family.simulator`
- Wolf Google Play: `https://play.google.com/store/apps/details?id=unimix.studio.wolf.simulator`

## Current content

- Home page with a rotating hero carousel for five games.
- Privacy policy pages for all app packages.
- Root `app-ads.txt` file for AdMob and mediation sellers.

## Implementation notes

- GitHub Pages is built from the `main` branch.
- `privacy-policy.md` uses Jekyll front matter and `_layouts/default.html`.
- `app-ads.txt` is served from the site root, not from a subpage.
- The AdMob seller line is present in the root `app-ads.txt`.
- Public verification already confirmed that the site and `app-ads.txt` return `200`.

## How to add the next game

1. Add a new landing page for the game.
2. Add a matching privacy policy page if the app needs its own policy.
3. Update `app-ads.txt` only if the monetization setup changes.
4. Update the README and this document so the new game is discoverable.

## Play Console reminder

The developer website in Google Play should point to the site root.
AdMob checks the public site after Play Console updates, so a crawl delay is normal.
