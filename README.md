# Camo Grind game data

Weapon and camo data for the Camo Grind Stream Deck plugin by itsCRA1G. Every Camo Grind install checks this repo every 6 hours and downloads newer data by itself.

## Files
- `index.json`: the list of games and their current data version (`rev`).
- `mw4.json`: Call of Duty: Modern Warfare 4.

## Releasing an update (e.g. new season weapons)
1. Edit the game file (e.g. add the new weapons to `season`).
2. Add 1 to `rev` in the game file, and set `updated` to today's date.
3. Put the same `rev` number in `index.json`.
4. Commit. Streamers get it within 6 hours, or straight away when they restart Stream Deck.

## Rules
- Never rename a weapon once it's out: the name is how progress is kept.
- No `<` or `>` characters anywhere, or every install will refuse the update.
- The plugin also refuses a file that isn't valid JSON, so a typo can't break anyone's tracker. They keep the last good copy.
