# Story of Seasons: A Wonderful Life Gift Finder

Static page. Search a gift category (Eggs, Fish, Gemstones, etc.) to see which villagers favour it. Or pick a villager to see their full favourite-category list, grouped by their location.

## Data

Parsed from `../source_sirus.txt` (sirusgaming.com, "Story of Seasons: A Wonderful Life Gift Guide – Best Gifts for Every Character", posted June 29, 2023, fetched 2026-11-26) via `../parse.py` into `../parsed.json`, then embedded in `data.js`.

32 villagers covered by the source, all 32 parsed cleanly with a non-empty category list; none were skipped or failed to parse. Nothing is invented to fill gaps; villagers or categories not in the source are simply not listed. Two entries carry the source's own qualifiers verbatim ("Meals (except for fishes)" for Pui, "Milk (May vary based on his age)" for Hugh) rather than being simplified or dropped.

## Files

- `index.html` — the page
- `data.js` — the 32 villagers' favourite-category data (also usable from Node via `module.exports`)
- `test.js` — known-answer tests, run with `node test.js`

## Caveat

Single source, favourite categories only, no dislikes listed. Community gift guides can disagree with each other and with in-game behavior. Verify in-game.
