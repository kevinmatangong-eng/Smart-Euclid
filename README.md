# Smart Euclid

Smart hydration. Better habits.

A hydration-monitoring and personalized drinking-reminder app built for the Grade 12 STEM research project *"Development and Evaluation of a Smart Water Intake Monitoring and Personalized Drinking Reminder Application for Promoting Hydration Habits Among Grade 12 STEM Students of Liceo de Sto. Tomas de Aquinas."*

## Feature list

- Manual water intake logging (presets + custom amount, with input validation)
- Dashboard with progress ring, remaining amount, percentage, and next reminder
- Drinking history grouped by day, with edit/delete
- Personalized reminders (custom start/end time, interval) with School Mode (holds reminders back during class, prioritizes breaks/lunch)
- Streaks, 5 achievements, and 7-day statistics chart with averages and goal-completion rate
- Experimental drinking-detection demo (simulated confirmation flow — does not use the real camera)
- Light/dark theme, data export (JSON), and one-tap data reset
- Installable as a home-screen app (PWA) with basic offline support for the app shell
- All data stays in the browser's local storage on each user's own device — nothing is sent to a server

## Technology stack

- Plain HTML + React (via CDN, no build step) — chosen because this project is developed entirely from a phone, with no desktop/Node.js/Android Studio available
- Tailwind CSS (CDN) for styling
- Hand-drawn inline SVG icons and a hand-built SVG bar chart (no external icon/chart packages, so the whole app is 3 small files plus 2 icons)
- Browser `localStorage` for data persistence and the Notification API for in-tab reminder alerts
- A minimal service worker for offline caching of the app shell

## Files

- `index.html` — the entire app
- `manifest.json` — makes the app installable ("Add to Home Screen")
- `service-worker.js` — basic offline support
- `icon-192.png`, `icon-512.png` — app icons

## Deploying with GitHub Pages (from a phone, no computer needed)

1. Go to **github.com** in your phone's browser and sign in (or create a free account).
2. Tap **+ → New repository**. Name it e.g. `smart-euclid`, set it to **Public**, and create it.
3. Open the new repo, tap **Add file → Upload files**, and upload all 5 files from this folder (`index.html`, `manifest.json`, `service-worker.js`, `icon-192.png`, `icon-512.png`) in one go. Commit the changes.
4. Go to the repo's **Settings → Pages**. Under "Build and deployment", set **Source: Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
5. Wait about a minute, then your app is live at:
   `https://<your-username>.github.io/smart-euclid/`
6. Share that link with your classmates. On Android (Chrome) or iOS (Safari), opening the link shows an **"Add to Home Screen"** / install prompt — once added, it opens full-screen with its own icon, just like a native app.

Whenever you want to update the app, edit `index.html` directly in GitHub (pencil icon → edit → commit), and the live site updates automatically within a minute or two.

## Known limitations (for the research write-up)

- **Drinking detection is a simulated demo, not real camera-based detection.** It demonstrates the intended confirm-before-logging flow (per the spec's accuracy requirements) without accessing anyone's camera. A future version could add real on-device pose detection.
- **Reminders only fire while a participant has the app open in a browser tab or installed as a home-screen app** — this is a browser-based prototype, not a native app, so it cannot send background push notifications the way an installed Android/iOS app from an app store would.
- **Data is local to each device/browser.** There's no shared backend, so a student's data doesn't sync across devices, and clearing browser data or reinstalling will erase it (Export in Settings can be used to back up before that happens).
- All hydration figures are self-reported by the user; the app makes no medical claims and does not diagnose hydration status.

## Want an actual installable Android app (.apk) later?

Once this is hosted (step above), you can generate a real Android package from it — without Android Studio — using **[PWABuilder](https://www.pwabuilder.com)** (a free Microsoft tool, works from any browser including mobile): enter your GitHub Pages URL, it scores your PWA, and gives you a downloadable Android package you can side-load or submit to the Play Store.
