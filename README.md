# Training Tracker — Standalone App

**TL;DR:** 4 files + 2 icons. Put them on any static host (GitHub Pages is free), open the URL in Chrome, install to home screen. Real app, real mic, permanent storage on your phone. Coach works after you paste your Anthropic API key once (⚙ in the coach panel — key never leaves your device).

## What this is

The complete tracker as a Progressive Web App: sessions, week sequence, C25K run timer with audio cues, training log with edit/export/import, and the AI coach. No server. No accounts. All data lives in your phone's browser storage and survives forever unless you clear site data.

## Deploy — Path A: entirely from your phone (~10 min)

1. Get these files onto your phone and **unzip** them (Files app can extract).
2. Go to **github.com** in Chrome, sign in, tap **+ → New repository**. Name it `training-tracker`, keep it **Public** (required for free Pages), create.
3. On the empty repo page: **uploading an existing file** link → select all 6 files (index.html, manifest.json, sw.js, icon-192.png, icon-512.png, README.md) → Commit.
4. Repo **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main**, folder **/ (root)** → Save.
5. Wait ~2 minutes. Your app is live at `https://YOURUSERNAME.github.io/training-tracker/`
6. Open that URL in Chrome → menu → **Install and create shortcut** → Install. It's now its own app — its own icon, its own identity, nothing can hijack it.

## Deploy — Path B: Claude Code (~2 min of your attention)

Put this folder somewhere Claude Code can see it and say:

> "Deploy the standalone folder as a GitHub Pages site. Create a public repo called training-tracker, push these files, and enable Pages from the main branch root. Give me the live URL."

## First run

- The app offers **Import**: paste the JSON from the artifact version's **Export Log** button and your whole history + cycle position carries over. Or start fresh.
- **Coach setup:** COACH → ⚙ → paste your API key from **console.anthropic.com** (create one under API Keys; add a payment method — typical coach usage costs cents per month). The key is stored only in your phone's local storage for this app. Type CLEAR in the same dialog to remove it.
- **Mic:** first tap will trigger a normal Chrome permission prompt. Allow it.

## Things worth knowing

- **Public URL, private data.** The page itself is public (it's just the empty app); your log and API key exist only on your device. Anyone visiting your URL gets a blank tracker.
- **Backups:** storage is permanent but lives in Chrome's site data. Hitting "Clear browsing data" for all sites can wipe it. Export Log occasionally and paste the JSON somewhere safe (notes app). Import restores everything.
- **Updates:** to update the app later, replace index.html in the repo (GitHub web: open file → pencil icon or re-upload). The service worker picks it up on the next refresh; bump the CACHE name in sw.js ("tt-v1" → "tt-v2") when you change files, or just hard-refresh.
- **Run timer + screen:** the app requests a wake lock during runs so the screen stays on; audio cues are most reliable with the screen awake.
