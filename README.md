# Training Procedure Tracker

Personal workout PWA: KAZ + LBA + C25K + lifts. Session checklists with set logging, week sequence (legs first, rest second), built-in C25K interval run timer with voice cues, floating resizable stopwatch, training log with notes and editing, AI coach with LIVE voice logging, next-session targets, and automatic GitHub backup of the log.

Static files only. No build step, no server. All data lives on the device, mirrored to a private GitHub repo once sync is configured.

## Files

index.html (the whole app), manifest.json, sw.js, icon-192.png, icon-512.png

## In-app setup (owner only)

1. Coach: COACH button, gear icon, paste Anthropic API key from console.anthropic.com. Stored on device only.
2. Backup: LOG view, tap the cloud line, enter owner/repo of a PRIVATE repo plus a fine-grained token scoped to that repo with Contents read/write. Stored on device only. After this, the log pushes automatically on every change and restores automatically if local storage is ever empty.
3. History: LOG view, Import Log, paste an export JSON once if migrating.

## Updating the app later

Replace files in the repo and bump the CACHE name in sw.js (tt-2 to tt-3, etc). Installed phones pick up the new version on next open plus refresh.
