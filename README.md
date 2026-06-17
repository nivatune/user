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
brew trust nivatune/niva    # Required once for third-party taps
brew install niva
```

### Manual download

Download the latest release archive for your platform from
[Releases](../../releases):

- **macOS:** `niva-<version>-universal-apple-darwin.tar.gz`
- **Windows:** `niva-<version>-x86_64-pc-windows-msvc.zip`

Extract the archive and add the folder to your `PATH` (or move the binaries to
a directory already on your `PATH`). Keep the PDFium library in the **same
directory** as the `niva` binary — `libpdfium.dylib` on macOS, `pdfium.dll` on
Windows. It is required for PDF rendering.

On Windows, Defender SmartScreen may warn about unsigned binaries until code
signing is in place.

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

- **macOS:** universal binary (Apple Silicon + Intel); Homebrew or manual tarball.
- **Windows:** x64 zip (`niva.exe` + `pdfium.dll`).
- **Linux:** planned.

## License

See [LICENSE](LICENSE).
