# Ha! A Field Guide to Laughter

An interactive, single-page website about the virtues of humor and laughter.

**Live site:** https://field-guide-to-laughter.higgsfield.app

## What's on the page

| Section | What it does |
| --- | --- |
| Hero | Looping video of friends laughing. Tap the giant “Ha!” or “Play a laugh” to hear one. |
| Laugh ribbon | Scrolling words for laughter (giggle, guffaw, cackle, hoot…). Each plays its own synthesized laugh. |
| Science | A dictionary entry for *gelotology*, an interactive “Anatomy of a ha” waveform with voice, note-count and spacing controls, and four research findings with citations. |
| Virtues | Six photographs, each paired with one thing laughter does for a life. |
| Contagion | A room of twelve faces. Tap one and watch laughter spread to its neighbours. |
| Joke jar | 32 clean puns with a reveal, plus “Ha!” and “Groan” ratings. |
| Practice | A guided one-minute laughter yoga routine with a progress ring, clap rhythm and cues. |
| Quotes | A carousel of sourced quotes about laughter. |
| Laugh log | Tap each time you laugh today. Shows a 7-day chart, streak and best day, stored only in the browser. |

Every laugh is generated live with the Web Audio API (formant-filtered voiced notes with aspirated onsets). The default timing follows Robert Provine's measurements: notes of about 75 ms, repeated about every 210 ms, fading as they go.

## Files

- `index.html` is the complete page: markup, CSS and JavaScript in one file, no build step.
- Images and the hero video load from `img/` next to the page. They were generated with Higgsfield (GPT Image 2.5 for the photographs, Seedance 2.5 for the hero loop) and are served by the live site at `https://field-guide-to-laughter.higgsfield.app/img/<name>`.

Expected asset names: `hero.webp`, `hero-loop.mp4`, `bench.webp`, `rain.webp`, `sunflower.webp`, `tickle.webp`, `hospital.webp`, `artist.webp`, `yoga.webp`, `jar.webp`, `campfire.webp`, `og.jpg`.

## Running locally

Put the assets in `laughter/img/`, then serve the folder:

```sh
cd laughter
python3 -m http.server 8000
```

Open http://localhost:8000. Without the `img/` folder the page still works; photo areas stay empty.
