# A Little Universe For You 💗

An interactive romantic website in a single file: `index.html`.
No backend, no database, no build tools, no dependencies.

## How to run

Open `index.html` directly in any modern browser (Chrome, Edge, Firefox, Safari, Android, iPhone).

## What's inside

- **Cinematic intro** with Enter and Skip buttons, and a zoom transition into the site.
- **Particle heart engine** (canvas): about 950 particles (420 on small screens) float, gather into a dotted heart, pulse and orbit, dissolve, morph into a circle, then repeat. Mouse repels particles; touch attracts them.
- **Background universe**: twinkling stars, floating hearts, shooting stars, parallax and soft nebula glow.
- **Floating glass navigation** with smooth scroll, active-section indicator and mobile hamburger menu.
- **A Few Words For You**: 25 notes with a typewriter effect, shown in random order without repeats until all have appeared.
- **Love letter**: envelope opens, letter types out, hearts float. Close and replay buttons included.
- **Memory gallery**: 5 horizontal cards with 3D tilt.
- **Quiz**: 7 questions, one per screen, animated progress bar, 4 score-free results, replay.
- **Catch The Hearts**: 30 seconds, combo bonus, rising difficulty, pause and restart.
- **Find The Hidden Heart**: 5 rounds, 20 seconds each, progress bar.
- **Send A Little Happiness** button: heart burst and a message.
- **Final surprise** with a Replay The Magic button.
- **Sound** generated with the Web Audio API. It is muted by default and only starts after you press the speaker button.

## Customising

All content is plain text inside `index.html`. Search for these names:

| What to change | Where to look |
| --- | --- |
| Notes | `const NOTES` |
| Love letter text | `const LT` |
| Quiz questions | `const QS` |
| Quiz results | `const RS` |
| Gallery card titles and colours | `const GC` |
| Colours | `:root` at the top of the CSS |
| Particle count | `build()` function (the `420` and `950` numbers) |
| Heart cycle timing | `phase()` function |

### Adding your own photos

In the Memories section, tap **Add photo** on a card and paste an image link (`https://...`). The photo only lasts until you reload the page, because nothing is saved. To keep a photo permanently, edit the code: in the `$('#gal').innerHTML` line, replace `linear-gradient(135deg,${g[2]})` with `url("your-image-link")` for that card.

## Accessibility and performance

- Respects `prefers-reduced-motion`.
- Animations pause when the tab is hidden.
- Games only run their loops while playing.
- If canvas is unavailable, the page still works without the particle background.

## Notes

- The gallery cards are placeholders. They are not real memories.
- Sounds are quiet
- and optional.
