# Hisaab — Day Points

A personal daily task ledger that runs entirely in the browser. Your day runs from one wake-up to the next, and finished tasks add points to it.

## What it does

- **Today** — the day's checklist with search, filters, quick tick-off and a one-tap time setter.
- **Dashboard** — the points dial (Productive, Average, Waste), points by category and a four-quadrant breakdown.
- **Focus** — countdown timer for timed tasks and a stopwatch for measuring new ones.
- **Tasks** — Stephen Covey's four-quadrant matrix:
  - Q1 Do first (urgent and important)
  - Q2 Schedule (important, not urgent)
  - Q3 Delegate (urgent, not important)
  - Q4 Eliminate (neither)

  Tasks are sorted automatically from their name and category. Tap a task's Q badge to move it. Search accepts `q1` to `q4`.
- **Progress** — calendar coloured by each day's verdict, a 14-day chart and a per-day breakdown.
- Light, dark or match-device theme.
- Works offline after the first visit and can be installed to the home screen.

## Publish on GitHub Pages

1. Create a new repository on GitHub, for example `hisaab`.
2. Upload every file and folder from this zip to the repository's root, keeping `icons/` as a folder. Commit.
3. Open **Settings → Pages**. Under *Build and deployment* choose **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
4. After a minute or two the app is live at `https://<your-username>.github.io/hisaab/`.
5. On your phone, open that link in Chrome and choose **Add to Home screen** (or **Install app**).

## Your data

Everything is stored in the browser's local storage on that device only. Nothing is sent anywhere.

Browser storage is tied to the web address. Data from the copy you opened as a file, or from another link, does not appear automatically on the GitHub Pages link. To move it:

1. In the old copy, open **Settings → Download backup file** (or **Copy backup**).
2. In the new copy, open **Settings → Restore from backup**.

Take a backup now and then.

## Releasing an update

1. Replace `index.html` with the new version.
2. In `sw.js`, raise `VERSION` (for example `hisaab-v3.0.1`) so phones pick up the new files.
3. Commit. Open the app once while online, then reopen it to see the update.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole app: markup, styles and logic in one file |
| `manifest.webmanifest` | Name, colours and icons for installing to the home screen |
| `sw.js` | Service worker that caches the app for offline use |
| `icons/` | App icons and favicon |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |
