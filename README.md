# KILN

**Play it here: https://eseto9.github.io/Kiln/**

A stained-glass roguelike in one HTML file. Forty windows, one kiln, no installs.

Each window is a grid of empty glass with a rule at the top. **Drag** across cells to cut a pane. Let go and it either **sets** in colour or **cracks**. Cracks heat the kiln. Setting glass cools it. The heat carries across all forty windows, and if it ever reaches the top the glass shatters and the run ends.

## Rules a window can ask for
| Rule | A pane sets only if… |
|---|---|
| **Shape** | it is the shape shown (rotated or mirrored both count) |
| **Cells** | it has exactly that many cells |
| **Gem** | it holds exactly one gem |
| **Frame** | it touches the outer frame |
| **Dark** | (modifier) gems and lead are hidden until glass is set beside them; cutting into hidden lead cracks the pane |

Every fifth window is a **cathedral window**: bigger, two or three rules at once, and it drops a **relic** that stays unlocked for future runs. Window 40 is The Great Window.

## Heat
| Event | Heat |
|---|---|
| Crack | +5 per cell |
| Set | −1 per cell |
| Fire early | +4 per empty cell, +2 per cracked cell |
| Flawless window (no cracks, no empties) | −8 |

## Boons
After every window, draft one of three. Common, Rare and Legendary, they stack for the run, and four pairs unlock a **synergy** (Spare Pane + Slack, Reclaim + Lead Came, Quench + Cold Start, Tempered + Thick Glass).

## Modes
- **New run** — random seed, carry one unlocked relic.
- **Daily window** — same seed for everyone that day, no relic, best result saved per day. Share button copies a one-line result.

## Run locally
Open `index.html` in any modern browser, desktop or phone. Progress (relics, bests, dailies) is saved in localStorage.
