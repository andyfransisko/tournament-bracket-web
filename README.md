# Tournament Bracket Builder

A single-page, client-side tool for building single-elimination tournament brackets. Paste in a list of participants, optionally shuffle the seeding, and get an auto-generated bracket with bye handling, score entry, and automatic winner propagation through to a champion banner.

No build step, no backend, no dependencies at runtime — it's one `index.html` file.

## Features

- Paste participants one per line (any count — automatically padded with byes to the next power of two)
- Optional random shuffle for seeding
- Score entry per match, with automatic winner advancement to the next round
- Live champion banner once the final is decided
- State persists to `localStorage`, so a reload doesn't lose your bracket
- Dark, responsive UI (mobile-friendly sidebar collapse)

## Usage

Just open [index.html](index.html) in a browser — no server required.

To serve it locally instead:

```bash
npm install
npm start
```

This serves the current directory at `http://localhost:3000`.

## Development

The entire app (markup, styles, and logic) lives in `index.html`. There's no build pipeline — `npm run build` just sanity-checks that the file exists and isn't empty, useful as a CI smoke check.

```bash
npm run build   # verify index.html is present and non-trivial
```

## Demo
[Demo Website](https://tournament-bracket.andyfransisko.com)

## License

MIT — see [LICENSE](LICENSE).
