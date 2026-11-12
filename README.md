# Copilot V2 Repository

A simple, curated list of every file for the Copilot V2 project (AC Service and Repair | Product Business Team): sheets, docs, decks, forms, query exports and tools. Each entry links to the file in Google Drive. Links only open for people who already have access in Drive.

## Structure

```
index.html         the page
assets/style.css   styles (light and dark)
assets/app.js      filters by type, sorts A → Z or by type
assets/icon.svg    tab icon
data/files.json    the file list (edit this to add or change files)
.nojekyll          serve files as-is on GitHub Pages
```

## Add or change a file

Edit `data/files.json` and add an entry:

```json
{
  "name": "File name",
  "type": "Sheet",
  "link": "https://docs.google.com/...",
  "summary": "What is in the file and who should use it.",
  "keywords": ["keyword", "another"],
  "updated": "2026-11-12"
}
```

`type` is one of `Sheet`, `Doc`, `Deck`, `Form`, `Query`, `Other`. Leave `link` empty to show "Link coming".

## Publish on GitHub Pages

Settings → Pages → Build and deployment → Source: **Deploy from a branch** → Branch: `main`, folder `/ (root)` → Save. The site appears at `https://<account>.github.io/<repository-name>/`.

## Preview locally

```
python -m http.server 8000
```

Then open http://localhost:8000. Opening `index.html` directly from disk will not load the list.
