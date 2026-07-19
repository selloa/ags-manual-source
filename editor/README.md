# In-editor help source

Filtered manual corpus for a future AGS Editor **bottom help panel** (riders → article list → viewer), inspired by Sonic-Pi’s in-app docs.

Public full-manual TOC remains [`_Sidebar.md`](../_Sidebar.md) / [`index.md`](../index.md).

## Rider model

| Rider | Purpose |
|-------|---------|
| Home | Landing page |
| Index | A–Z, overview, obsolete, constants/types/variables |
| World | Rooms, characters, hotspots, camera, … |
| UI | Dialogs, GUIs, controls, mouse, overlays |
| Media | Audio, drawing, sprites, speech |
| Data | File, String, Game, System, collections, … |
| Language | Cheat sheet + language reference |
| Guides | Shortcuts, blocking, events, global handlers |
| Editor | Panel/property reference |

## Files

| File | Role |
|------|------|
| [`nav.json`](nav.json) | **Plugin contract** — riders, article ids, titles, defaults |
| [`manifest.txt`](manifest.txt) | Packaging include list (every `nav.json` article id) |
| [`../_EditorSidebar.md`](../_EditorSidebar.md) | Preview HTML sidebar mirror of `nav.json` |
| [`../EditorHelpHome.md`](../EditorHelpHome.md) | Default article (`defaultArticle`) |
| [`../EditorCheats.md`](../EditorCheats.md) | Guides hub |
| [`../EditorLanguageCheat.md`](../EditorLanguageCheat.md) | Language hub |

Article `id` values are Markdown basenames (no `.md`). The plugin should load `nav.json` and show HTML pages `{id}.html` in the viewer.

## Preview

From the private build tree (`../ags-manual`):

```bat
rebuild-editor-preview.ps1
start-editor-preview.bat
```

See `../ags-manual/PREVIEW.md`.
