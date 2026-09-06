# Changelog

Version shows in the app header (BUILD vX.Y.Z). The sw.js cache name is locked to the version (tt-vX.Y.Z), so every version bump forces installed phones onto the new build. Commit convention: "vX.Y.Z: summary".

## 0.9.3
- Triceps superset converted to a tracked lift (DB Skullcrusher, 3 sets with steppers) so its history, blurb, and seeding connect; band extension noted in the sub
- Refreshed four stale August-dated lift sub-texts to durable progression phrasing (chest press, fly, lateral raise, leg extension)

## 0.9.2
- Set steppers now initialize from the most recent history entry for that lift instead of baked-in defaults (falls back to defaults only when the lift has no history)

## 0.9.1
- Tap zones split on checklist items: the GO square marks complete, tapping the row body opens details (lift logger, or a note panel on non-lift items) so notes can be added before finishing
- Every non-lift exercise now has its own add-note button

## 0.9.0
- Version number displayed in header; cache name locked to version
- One-time sweep of checkboxes stuck by the old stamp bug
- Manual notes: session notes panel on every session page, per-lift add-note in the logger
- Notes editing on history records: list, delete, and add notes retroactively in edit mode
- Last-performance blurb at the top of each lift logger (last date, sets compressed, most recent note)
- Rest chip is a toggle: tapping a logged rest reopens it and pulls the cycle pointer back
- Import errors shown inside the modal with character count (truncated pastes self-identify); toasts render above all overlays

## 0.8.0
- GitHub sync: auto-push of the full log to a private repo on every change, auto-restore when local storage is empty, sha conflict retry, status line in the log view

## 0.7.0
- Week reordered: Legs, Rest, Run F, Push, Run L, Pull, Run F (rest guaranteed after legs)
- Rest became a mid-cycle step; cycle wraps automatically after D7
- Floating stopwatch: draggable, persistent, three sizes (pill, big, fullscreen)

## 0.6.0
- LIVE coach: spoken set reports get logged, notes captured, next-session targets set; every write announced by toast; logs only explicitly stated numbers
- Target chips on lifts with tap-to-load
- Fixed stamp bug that cleared checkboxes under the wrong keys
- Notes and targets round-trip through export/import

## 0.5.0
- Built-in C25K interval run timer: full-screen overlay, per-week segments (including W5/W6 run variants), beep and spoken cues, wake lock, segment strip, auto-checks the run on finish

## 0.4.0
- Standalone conversion: localStorage, first-run import screen, PWA packaging (manifest, service worker, icons), bring-your-own Anthropic API key with direct browser access

## 0.3.0
- Training log: history records on stamp, progression summary, record editing and deletion
- Coach mode: context-aware chat with mic and text input, spoken replies
- Export log

## 0.2.0
- Pull day added; LBA upper-back block moved to pull
- Week sequence strip with skip and completed-chip navigation

## 0.1.0
- Base tracker: five sessions, checklists, set steppers with baselines, C25K week counter, stamp flow
