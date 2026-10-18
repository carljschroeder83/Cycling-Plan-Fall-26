# Winter Cycling Block 1 — Setup

Installable Android app (PWA). All logged data stays on your phone. No accounts, no servers.

## Files

| File | Purpose |
|---|---|
| `index.html` | The full app: plan, tracker, export |
| `manifest.json` | Install-as-app metadata |
| `sw.js` | Service worker for offline use |
| `icon-192.png`, `icon-512.png` | Home screen icons |

## Deploy (about 5 minutes)

1. On GitHub, create a new **public** repository, e.g. `winter-cycling-block-1`.
2. Upload all 5 files to the repository root (Add file, then Upload files).
3. Go to **Settings, then Pages**. Set Source to "Deploy from a branch", branch `main`, folder `/ (root)`, and save.
4. After about a minute the app is live at `https://carljschroeder83.github.io/winter-cycling-block-1/`.

## Install on your phone

1. Open that URL in Chrome on Android.
2. Tap the menu (three dots), then "Add to Home screen" / "Install".

## Notes

- **Separate from the old plan.** This app stores data under its own key prefix (`wcb1_`) and its own cache name, so it will not collide with the Summer plan on the same github.io domain. Remove the old home screen app when you retire it.
- **Backups.** Data lives in Chrome's site storage. Clearing site data or uninstalling deletes it. Use the Export button each week as your backup.
- **No sync.** Phone and laptop keep separate copies.
- **Updating the plan.** Replace `index.html` in the repo and bump `CACHE_NAME` in `sw.js` (`wcb1-v1` to `wcb1-v2`) so phones pick up the change.
- **Weekly check-in.** Use Export for check-in on the Sunday evening and paste it into Claude on Monday.
