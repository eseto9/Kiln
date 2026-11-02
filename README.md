# KILN

**Play it here: https://eseto9.github.io/Kiln/**

A stained-glass roguelike in one HTML file. Forty windows, one day of light, no installs.

You are a glazier. Each window is a grid of empty glass with a rule at the top. **Drag** across cells to cut a pane. If it obeys the rule it **sets** in colour and throws its light onto the floor below. If not, it dissolves. Any pane can be lifted back out with **Undo**.

The sky behind the glass moves from dawn to dusk over the forty windows. Your light is your buffer: spend it carelessly and night falls early.

## Rules a window can ask for
| Rule | A pane sets only if… |
|---|---|
| **Shape** | it is the shape shown (rotated or mirrored both count) |
| **Cells** | it has exactly that many cells |
| **Gem** | it holds exactly one gem |
| **Frame** | it touches the outer frame |
| **Dark** | (modifier) gems and lead are hidden until glass is set beside them |

Every fifth window is a **cathedral window**: bigger, two or three rules at once, and it drops a **relic** that stays unlocked for future runs. Window 40 is The Great Window.

## Light
| Event | Light |
|---|---|
| Undo a pane | −1 |
| A pane dissolves | −2 |
| Each empty cell when the window fires | −4 |
| Every window fired (the day moving on) | −2 |
| Flawless window, every cell set | +5 |

At 0, night falls and the run ends.

## Boons
After every window, draft one of three. Common, Rare and Legendary, they stack for the run, and four pairs unlock a **synergy** (Spare Pane + Slack, Filler + Lead Came, Dawn Chorus + Afterglow, Steady Hand + Slow Sun).

## Modes
- **New run** — random seed, carry one unlocked relic.
- **Daily window** — same seed for everyone that day, no relic, best result saved per day. Share button copies a one-line result.

## Run locally
Open `index.html` in any modern browser, desktop or phone. Progress (relics, bests, dailies) is saved in localStorage. `Z` undoes on a keyboard, `Esc` pauses.
