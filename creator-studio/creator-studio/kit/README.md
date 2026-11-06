# kit/

This folder holds the cartoon engine that Mode A (video build) runs. It is not included in this repo yet.

Copy these from your original `cartoon-audio-short` skill folder into `kit/`:

- engine files (`web/`: `index.html`, `main.js`, `motion.js`, `paint.js`, `roman.js`, `toonbase.js`, `story.js`)
- tools (`tools/setup.sh`, `render.mjs`, `timing.py`, `audio.py`, `mix.py`, `sheet.py`, `finish.sh`)
- the worked example ("The Soldier Who Never Left")
- vendored three.js r160 and `toon.ts`

Check the file names against your original folder; the list above comes from the references in `SKILL.md`.

Before publishing, confirm that every file you add here may be redistributed. three.js and the Pen library are MIT; keep their license notices next to them.
