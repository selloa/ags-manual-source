# In-editor help source

This repo holds the full AGS manual. The **in-editor** profile is a filtered subset for a future help pane.

| File | Role |
|------|------|
| `editor/manifest.txt` | Basenames included in the editor package |
| `_EditorSidebar.md` | Sidebar for the filtered HTML build (top-level; excluded from page list like `_Sidebar.md`) |
| `EditorHelpHome.md` | Pane landing page |
| `EditorCheats.md` | Shortcuts / guides hub |
| `EditorLanguageCheat.md` | Language essentials |

Public TOC remains `_Sidebar.md` / `index.md` (full manual).

Non-page files live under `editor/` so the Pandoc build (which only packages top-level tracked files) does not treat them as HTML topics.

## Preview

From the private build tree (`../ags-manual`):

```bat
rebuild-editor-preview.ps1
start-editor-preview.bat
```

See `../ags-manual/PREVIEW.md`.
