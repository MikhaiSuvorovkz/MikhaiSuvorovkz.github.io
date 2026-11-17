# Project Overview

Last updated: 2026-11-17

## What this repo is

Static GitHub Pages site for `Wild Horse Simulator Family 3D`
(`magic.horse.simulator.free.sim.games.kids`), `Winter Tiger Family Simulator`
(`unimix.studio.winter.tiger.family.simulator`), `Fox Family Simulator`
(`unimix.studio.fox.family.simulator`), `Panther Family Simulator`
(`unimix.studio.panther.family.simulator`), `Wolf Family Simulator`
(`unimix.studio.wolf.simulator`), and `Snow Leopard Family Simulator`
(`unimix.studio.snow.leopard.family.simulator`), `Bear Simulator Family 3D`
(`unimix.studio.bear.simulator.animal.family`), `Deer Simulator: Animal Family`
(`unimix.studio.deer.simulator.animal.sim.family`), and `Cyberbeat`
(`com.skillapp.cyberbeat`).

## Live URLs

- Site: `https://mikhaisuvorovkz.github.io/`
- Wild Horse Privacy Policy: `https://mikhaisuvorovkz.github.io/privacy-policy/`
- Winter Tiger Privacy Policy: `https://mikhaisuvorovkz.github.io/winter-tiger-family-simulator/privacy-policy/`
- Fox Privacy Policy: `https://mikhaisuvorovkz.github.io/fox-family-simulator/privacy-policy/`
- Panther Privacy Policy: `https://mikhaisuvorovkz.github.io/panther-family-simulator/privacy-policy/`
- Wolf Privacy Policy: `https://mikhaisuvorovkz.github.io/wolf-simulator/privacy-policy/`
- Snow Leopard Privacy Policy: `https://mikhaisuvorovkz.github.io/snow-leopard-family-simulator/privacy-policy/`
- Bear Privacy Policy: `https://mikhaisuvorovkz.github.io/bear-simulator-family-3d/privacy-policy/`
- Deer Privacy Policy: `https://mikhaisuvorovkz.github.io/deer-simulator-animal-family/privacy-policy/`
- Cyberbeat game page: `https://mikhaisuvorovkz.github.io/cyberbeat/`
- Cyberbeat Privacy Policy: `https://mikhaisuvorovkz.github.io/cyberbeat/privacy-policy/`
- app-ads.txt: `https://mikhaisuvorovkz.github.io/app-ads.txt`
- Wild Horse Google Play: `https://play.google.com/store/apps/details?id=magic.horse.simulator.free.sim.games.kids`
- Winter Tiger Google Play: `https://play.google.com/store/apps/details?id=unimix.studio.winter.tiger.family.simulator`
- Fox Google Play: `https://play.google.com/store/apps/details?id=unimix.studio.fox.family.simulator`
- Panther Google Play: `https://play.google.com/store/apps/details?id=unimix.studio.panther.family.simulator`
- Wolf Google Play: `https://play.google.com/store/apps/details?id=unimix.studio.wolf.simulator`
- Snow Leopard Google Play: `https://play.google.com/store/apps/details?id=unimix.studio.snow.leopard.family.simulator`
- Bear Google Play: `https://play.google.com/store/apps/details?id=unimix.studio.bear.simulator.animal.family`
- Deer Google Play: `https://play.google.com/store/apps/details?id=unimix.studio.deer.simulator.animal.sim.family`
- Cyberbeat Google Play: not published yet

## Current content

- Home page with a rotating hero carousel: eight animal games plus `Cyberbeat`.
  Carousel slides take an optional `playLabel` (Cyberbeat points at its own page, not a
  store listing) and an optional `theme`, where `neon` swaps the green hero overlay in
  `assets/styles.css` for a dark violet one.
- Privacy policy pages for all eight animal app packages.
- Landing page for `Cyberbeat` at `/cyberbeat/`, with its own dark neon styling
  (`assets/cyberbeat.css`) and images in `assets/cyberbeat/`. It is linked from the home page
  carousel (`assets/cyberbeat-hero.jpg`, composed from in-game screenshots), the "Also from
  this developer" section and the footer. The game is not on Google
  Play yet, so the store button on it is a "coming soon" label, not a link.
- Standalone bilingual (EN/RU) privacy policy page for `Cyberbeat`, linked from the home page
  developer files panel and footer.
- Root `app-ads.txt` file for AdMob and mediation sellers.

## Implementation notes

- GitHub Pages is built from the `main` branch.
- `privacy-policy.md` uses Jekyll front matter and `_layouts/default.html`.
- `cyberbeat/privacy-policy/index.html` is an exception: it is a byte-for-byte copy of a file
  generated in the `Cyberbeat` Unity project, so it has no front matter and keeps its own
  inline styles. Its source of truth is the in-game localization text, so never edit this page
  by hand. To update it: run `python3 -I tools/privacy/build_privacy_page.py` in the
  `Cyberbeat` project, then copy `Documentation/Privacy/privacy-policy.html` over this file.
- `cyberbeat/index.html` is hand-written static HTML with no front matter, because the game's
  art direction does not fit `assets/styles.css`. Its screenshots, track covers and icon are
  exported from the `Cyberbeat` Unity project (`reports/` and `Assets/`) with ImageMagick.
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
