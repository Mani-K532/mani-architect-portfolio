# Portfolio (GitHub Pages)

## How it works
- `index.html` is the whole site — a "card catalog" themed portfolio.
- Content lives in `content.json`. The page loads this file automatically, so editing it is the permanent way to change what visitors see.
- There's also an in-page **Edit mode** (pencil button, bottom right) for making changes visually — text, photo, skills, projects. Those edits autosave to your browser's local storage only, on your device. Visitors never see them unless you export and publish.

## Publishing an edit
1. Open `index.html` locally (or on your live GitHub Pages URL) and click **Edit**.
2. First time: you'll be asked to create a passcode — this just locks the Edit button on your own device, it is not real security (the site's code is public, like any static site). Don't use a password you use elsewhere.
3. Make your changes: click any text to type over it, use the photo tile to upload/replace your photo, add or remove skills and project cards.
4. Click **Export content.json** in the bottom bar. This downloads the updated file.
5. Replace the old `content.json` in your repo with the downloaded one, then commit and push. GitHub Pages will now serve your changes to everyone.

## Why it works this way
GitHub Pages only hosts static files — there's no server to save edits centrally. So "edit mode" is a convenience for drafting changes visually, and `content.json` is the single source of truth that actually gets published when you commit it.

## Local preview
Because the page uses `fetch()` to load `content.json`, opening `index.html` directly via `file://` may not load it in some browsers (CORS restrictions). Easiest fix: run a tiny local server from this folder, e.g. `python3 -m http.server`, then visit `http://localhost:8000`.

## Setup checklist
- [ ] Replace placeholder name, title, tagline, location, email in Edit mode or directly in `content.json`
- [ ] Upload your photo
- [ ] Update About paragraph
- [ ] Update skills list
- [ ] Update/replace the two sample project cards, add more as needed
- [ ] Update GitHub / LinkedIn / website links in Contact
- [ ] Export `content.json`, commit, push
