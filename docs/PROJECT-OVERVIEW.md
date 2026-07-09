# Project Overview

Last updated: 2026-07-09

## What this repo is

Static GitHub Pages site for `Wild Horse Simulator Family 3D`
(`magic.horse.simulator.free.sim.games.kids`).

## Live URLs

- Site: `https://mikhaisuvorovkz.github.io/`
- Privacy Policy: `https://mikhaisuvorovkz.github.io/privacy-policy/`
- app-ads.txt: `https://mikhaisuvorovkz.github.io/app-ads.txt`
- Google Play: `https://play.google.com/store/apps/details?id=magic.horse.simulator.free.sim.games.kids`

## Current content

- Home page with a custom hero image and game description.
- Privacy policy page for the app package.
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
