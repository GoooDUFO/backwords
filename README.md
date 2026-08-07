# Backwords

Type a sentence, get it back with the words in the opposite order.

> `go out to` → `to out go`

**Live: https://gooodufo.github.io/backwords/**

## Modes

| Mode | `the quick brown fox` becomes |
| --- | --- |
| **Words** (default) | `fox brown quick the` |
| **Letters** | `eht kciuq nworb xof` |
| **Both** | `xof nworb kciuq eht` |

Multi-line input is reversed line by line, so paragraphs keep their shape.
Emoji and accented characters are split on grapheme clusters (via
`Intl.Segmenter` where available) rather than raw code units, so they don't
come apart.

## Running it

It's one self-contained `index.html` — no build step, no dependencies, no
network calls. Open the file directly, or serve the folder:

```sh
python3 -m http.server 8080
```

## Deploying

GitHub Pages serves the repository root of `main`. Push to `main` and the
site updates.
