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

**Mirror** is a view toggle that works with any mode: it flips the result
horizontally, as if held up to a mirror. Copy still copies the plain text.
(Tip: **Both** + **Mirror** shows your original sentence in mirror-writing.)

**Speak** buttons on both fields read the text aloud with the browser's
built-in speech engine (nothing is sent anywhere). **Squeaky**, on by default,
turns pitch and rate up for a high cartoon voice. How squeaky it gets depends
on the voices your OS provides, and some engines ignore pitch.

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
