# Paper Toss

Flick a crumpled paper ball into the bin across seven rooms, from the office to a space station.

**Play:** https://udayansinha2027-source.github.io/paper-toss/

**Support:** if you enjoy it, [buy me a coffee](https://buymeacoffee.com/udayansinhf).

The whole game is one file, `index.html`: canvas rendering, physics, sound and UI with no build step and no dependencies beyond two Google Fonts.

## How to play

- Swipe up from the ball. A faster flick throws farther; the angle of the swipe aims.
- Wind pushes the paper sideways, so aim into it.
- Ten throws per room. 4, 6 and 8 makes earn one, two and three stars. One star unlocks the next room.
- A make that misses the rim is a swish and scores +5. Makes in a row add a streak bonus.

| Level | Room | Challenge |
|---|---|---|
| 01 | Office | Steady breeze |
| 02 | Classroom | Moving bin |
| 03 | Airport | Moving belt |
| 04 | Café | Long throw |
| 05 | Stadium | Crosswind |
| 06 | Beach | Gusts |
| 07 | Space Station | Low gravity |

## Run locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8765
```

Then visit http://localhost:8765. Stars and best scores are saved in the browser's local storage.

## Tuning

Difficulty constants sit near the top of the script: bin size (`BIN_R`), wind strength (`WIND_K`), star thresholds (`STAR_AT`), flight speed (`FLIGHT_SPEED`), and the flick-to-speed curve in `release()`.
