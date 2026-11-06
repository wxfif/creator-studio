# creator-studio

One Claude skill for short-form creators: it makes animated cartoon shorts from your voiceover, and it keeps everything Claude writes for you free of AI filler.

## Why this exists

- Making a cartoon short by hand means writing the idea, the script, the animation, the music and the mix. This skill runs that whole chain.
- Default AI text is padded with hype and filler. This skill bans those patterns in code, docs, scripts and chat replies.

## What it does

| Mode | Use it for |
|------|-----------|
| **A: Cartoon short** | 10 story ideas → script → your voiceover → finished 1080x1920 MP4 with music and SFX at half the voice level |
| **B: No-slop writing** | Code, READMEs, tutorials, blog posts, long-form video scripts, video editing guidance (cuts, pacing, captions) |

Claude picks the mode from your request. Both modes share the same writing rules.

## Quick Start

1. Download or clone this repo.
2. Add the `creator-studio/` folder as a skill in Claude (or Claude Code: put it in your skills directory).
3. Add the cartoon engine to `kit/` (see below). Skip this if you only use Mode B.
4. Ask for what you want:
   - `Give me 10 cartoon short ideas`
   - `Here is my voiceover, make the video`
   - `Write a README for this project`
   - `Cut the fluff from this video script`

## Requirements

Mode B: nothing.

Mode A (video build):
- Node 22.6+
- Python 3 with numpy and Pillow
- ffmpeg
- Playwright with Chromium (`npm i -g playwright && npx playwright install chromium`)
- The `kit/` folder (see `kit/README.md`)

## Structure

```
creator-studio/
├── SKILL.md                      # the skill
├── LICENSE
├── README.md
├── kit/                          # cartoon engine (Mode A), see kit/README.md
├── references/
│   └── examples.md               # before/after examples (Mode B)
└── assets/
    ├── video-script-template.md
    └── readme-template.md
```

## How it works

`SKILL.md` holds the routing table, the shared writing rules and both modes. Claude loads `references/` and `assets/` only when Mode B needs them. Mode A reads the engine from `kit/`.

## Credits

- The cartoon pipeline uses the Pen library (`toon.ts`) and three.js, vendored in `kit/`. Both are MIT. Pen comes from github.com/mromidev/claude-animated-shorts.
- The no-slop rules come from the original `no-slop` skill.

## Contributing

Open a PR. Good additions: more before/after examples, new templates, new outfits and poses for the cartoon cast. Keep new text free of the banned phrases listed in `SKILL.md`.

## License

MIT. See `LICENSE`.
