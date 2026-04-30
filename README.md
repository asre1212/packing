# Pack — travel packing app

A single-file iPhone-friendly packing app. All data is stored locally on the phone in the browser. Backups move between phones via a JSON file.

## Files

- `index.html` — the entire app
- `manifest.webmanifest` — lets iPhone install it as a standalone app
- `icon.png` — placeholder icon (replace with your own; keep the filename `icon.png`)

## One-time setup: host on GitHub Pages

1. Sign in at <https://github.com> and click **New repository**. Name it something like `pack` and make it **Public**. Skip adding a README.
2. On the new empty repo page, click **uploading an existing file** and drag in all three files (`index.html`, `manifest.webmanifest`, `icon.png`). Click **Commit changes**.
3. Go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**. Pick branch `main` and folder `/ (root)`. Click **Save**.
5. Wait ~30 seconds, then refresh that page. GitHub will show a URL like `https://YOUR-USERNAME.github.io/pack/`.

## Add to your iPhone home screen

1. Open the GitHub Pages URL in **Safari** on the iPhone (it must be Safari, not Chrome, for the "Add to Home Screen" install behavior).
2. Tap the **Share** button → **Add to Home Screen** → **Add**.
3. Launch from the home-screen icon. It will run full-screen with no Safari chrome, like a native app.

## Replacing the icon later

1. Save your icon as a square PNG (1024×1024 is ideal). Name it exactly `icon.png`.
2. In the GitHub repo, click `icon.png` → the pencil/edit icon → **Replace this file** → upload your new file → **Commit changes**.
3. On the iPhone, delete the old home-screen icon and re-add it from Safari (iOS caches the original icon).

## Using the app

- **Master List tab** — your library of every item you might ever pack. Add items one at a time, or tap **Batch add** to paste many at once (one per line; optional `, 5` or ` x5` for quantity).
- **+ Trip** — create a trip. You'll get four bag sections per trip; rename each by tapping its title.
- **+ From master** — inside a trip, pick which master items go in this trip and which bag they belong to. This **does not** delete from the master list.
- **Quick add item** — for trip-only items not worth saving to master.
- **Move ⇄** — move an item between bags inside a trip.
- **Checkboxes** — check items off as you pack them.

## Backup / restore (transferring between phones)

- **Backup** (toolbar) → downloads `pack-backup-YYYY-MM-DD.json`. AirDrop, email, or save to iCloud Drive.
- On the new phone, open the app and tap **Restore**, then pick that JSON file. It replaces all data on the new device.

## Excel export

- Toolbar → **Excel** → downloads `pack-YYYY-MM-DD.xlsx` with one sheet for the master list and one sheet per trip (grouped by bag, with a packed column).
- Requires internet on first use (the Excel library loads from a CDN). After that, iOS Safari usually caches it.

## Privacy

Nothing leaves your device unless you explicitly tap Backup or Excel and share the file yourself. There is no server, no account, no tracking.
