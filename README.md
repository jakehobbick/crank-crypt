# WattQuest

A Slay-the-Spire-style dungeon run you play on a smart trainer. Three acts, 15 bosses, 103 achievements, 20 heroes, and a Grimoire (manga) art style.

**Play:** https://jakehobbick.github.io/crank-crypt/

- iPad / iPhone: open the link in the **Bluefy** browser (Safari can't use Bluetooth).
- Laptop / Android: use Chrome or Edge.
- Connect your trainer (FTMS) and optional heart-rate strap from the title screen.
- No gears (Zwift Cog / Zwift Ride)? Set **Bike gears → No gears** under Rider.

## Adding art

Painted art lives in `art/` and is listed in `art/manifest.json`. The game loads whatever the manifest lists and falls back to the built-in drawn art for anything that's missing or fails to load.

- `art/heroes/<hero id>.webp`: side view, facing **right**, transparent background. `l`/`r` are the left/right edges of the wheels as a fraction of image width, and `b` is the wheel bottom as a fraction of height. They line every bike up to the same size.
- `art/bosses/<boss key>.webp`: facing **left** (toward the hero). `h` is the height in game units (about 300–420), and `aura` is an optional glow colour like `"255,40,70"`.
- `art/enemies/<enemy key>.webp`: facing **left**. Optional `scale` (default 1), `dy` (vertical nudge) and `flip`.

**Hero ids:** kai, bram, sable, nami, luna, grim, mira, ash, frost, volt, zephyr, ember, sol, vex, pip, torvin, rin, thorn, tide, champ

**Boss keys:** lich, colossus, slime, mimic, kraken, spider, golem, vampire, minotaur, beholder, dragon, demon, herald, empress, sovereign

**Enemy keys:** skeleton, bat, ogre, zombie, goblin, slimeking, mimic, kraken, spider, golem, vampirelord, minotaur, beholder, dragon, demon (these are also used by any room or boss that draws that creature)

Example manifest entry:

```json
"enemies": { "skeleton": { "file": "art/enemies/skeleton.webp", "scale": 1.0 } }
```
