# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an archived mirror of the 1996 Space Jam movie website (www.spacejam.com/1996/), captured via HTTrack Website Copier on December 5, 2025. It is a static HTML archive — there is no build system, package manager, or test suite.

## Structure

All content lives under `fullsite/`. Key sections in `fullsite/cmp/`:

- `jamcentral/` — Production notes, filmmaker info, theatrical trailer, weekly photos
- `behind/` — Behind-the-scenes: character sketches, animation development, B-roll, technical notes
- `junior/` — Kids section: games, Looney Tunes bios, coloring book, basketball tips
- `lineup/` — Cast/player bios, Monstar villains, trivia quiz
- `bball/` — Basketball section: NBA player bios, QTVR elements, games
- `tunes/` — Soundtrack content (Atlantic Records) with artist info
- `souvenirs/` — Merchandise: posters, screensavers, postcards, clips, icons
- `pressbox/` — Credits and production info
- `jump/` — Links and promotional content

Other directories: `css/`, `dld/` (downloads), `img/` (images), `med/` (audio/video).

## Technical Notes

- Pure 1996-era HTML: uses `<center>`, `<font>`, `bgcolor`, `<nobr>`, image maps, and framesets
- Navigation uses `<map>`/`<area>` image maps and frame-based layouts (`*frames.html` / `*noframes.html` pairs)
- Server-side includes (SSI) appear as `<!--#include virtual="..."-->` comments — these were dynamic ad injections that no longer resolve
- Modern additions layered on top of the archive: Google Tag Manager scripts and `css/wbPolicyUpdatedNoticeStyle.css` for a Warner Bros. cookie/policy notification banner
- Media formats reflect 1990s technology: QuickTime VR (`.qt`), Macromedia Director (`.dir`), BinHex (`.hqx`), AIR audio (`.air`), WAV
- Some dynamic/server-dependent content (games, interactive features) will show 404s since it relied on server-side functionality
