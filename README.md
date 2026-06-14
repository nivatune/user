# Niva

Niva is a text-based music engraving tool for jazz and pop lead sheets. Write
chord progressions, section markers, barlines, annotations, and roadmaps in a
compact plain-text format and render them to PDF or SVG.

This repository distributes prebuilt Niva binaries. The source lives in a
separate repository.

## Install

### Homebrew (recommended)

```sh
brew tap nivatune/niva
brew install niva
```

### Manual download

Download the latest `niva-<version>-universal-apple-darwin.tar.gz` from
[Releases](../../releases), extract it, and place the binaries on your `PATH`.
Keep `libpdfium.dylib` in the same directory as the `niva` binary — it is
required for PDF rendering.

## Quick start

```niva
title "Autumn Leaves"; composer "Joseph Kosma"; style "Medium Swing"; tempo 132
key Gm; meter 4/4

[A]
| Cm7      | F7        | Bbmaj7    | Ebmaj7    ||
| Am7b5    | D7        | Gm        |           ||
```

```sh
niva render autumn-leaves.niva        # → autumn-leaves.pdf
```

Output is PDF by default; pass `--format svg` (or name an `.svg` output) for SVG.

## Documentation

See [docs/manual.md](docs/manual.md) for the full language reference.

## Platform

macOS universal binary (Apple Silicon + Intel). Linux and Windows builds are
planned.

## License

See [LICENSE](LICENSE).
