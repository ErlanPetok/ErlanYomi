# ErlanYomi

A single-file manga reader and reading tracker that runs entirely in your browser. Add manga from a linked folder or by uploading CBZ files, read them in a full-screen reader, and keep counters, bookmarks, and reading stats along the way.

No server, no account, no install. Open `manga-counter-working-v2.html` and go.

> Formerly "Manga Counter".

## Features

### Library
- Add manga by **linking a folder** or **uploading CBZ/ZIP files** (no upload size cap)
- Bulk CBZ import with automatic grouping into volumes and chapters, plus an editor to fix volume/chapter numbers and names before saving
- Favorites, rename, delete, and a "Hide completed" filter
- Progress ring, last-read time, and total reading time on every card
- Continue button, and double-click a card to jump back in
- Structure view grouped by volume, with lazy-loaded chapter thumbnails
- Read/unread chapter markers, "mark preceding chapters as read", and an option to hide read chapters

### Reader
- Full-screen reader with per-manga fit modes: **Page, Width, Height, Original**
- Right-to-left or left-to-right reading order
- Single or double-page layout with a cover offset
- Pinch zoom, double-tap zoom, and pan on touch devices
- Tap or click the left/right side to turn pages; swiping is disabled while zoomed in so you don't flip by accident
- Jump menu with search, and long-press the page number to jump to a page
- Chapter transition screen, resume-reading prompt after a reload, and automatic restoration of your place
- Keyboard shortcuts for navigation and counting
- Reader settings for scroll mode, progress bar position, preloading, greyscale, and dimming

### Counters and stats
- Custom counters with quick-count chips right inside the reader
- Per-volume summaries, totals, notes, and bookmarks
- Reading sessions with duration, pages, and chapter ranges
- **Reading time** tracked per chapter, summed per volume and per manga
- Export your data as a JSON save or CSV

### Appearance
- Five themes: Dark, Pink Cutesy, Matcha, Sky, and Vintage
- Mobile-friendly layout

## Getting started

1. Download `manga-counter-working-v2.html` from this repo.
2. Open it in a modern browser (a local file or any static host both work).
3. Click **Add manga** and either link a folder or upload CBZ files.

> **Browser note:** linking a folder uses the File System Access API, which is available in Chromium-based desktop browsers. Browsers without it can still use CBZ upload.

## Your data

Everything stays on your device:

| What | Where |
| --- | --- |
| Library, counters, bookmarks, stats, settings | `localStorage` |
| Uploaded images and linked folder handles | `IndexedDB` |

Clearing site data for the page will erase your library, so use the built-in **export** to back up regularly. Imported CBZ files take up browser storage, so very large libraries may hit your browser's storage quota.

## Finding manga

The library page links to a third-party MangaDex downloader (`manga.danbulant.eu`). It is a separate website, not MangaDex itself, and is not affiliated with this project. Please support creators and follow the terms of any site you download from.

## Tech

- One self-contained HTML file with plain HTML, CSS, and JavaScript
- No build step and no dependencies

## Contributing

Issues and pull requests are welcome. Because the whole app lives in one file, please keep changes backward compatible with existing saved data (storage keys and manga data structures).

## License

Add a license of your choice here (for example MIT).
