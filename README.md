# Smart Euclid

**Stay Hydrated. Stay Curious.**

A futuristic water-intake monitoring and personalized drinking-reminder application designed primarily for students.

Built for the Grade 12 STEM research project:
*Development and Evaluation of a Smart Water Intake Monitoring and Personalized Drinking Reminder Application for Promoting Hydration Habits Among Grade 12 STEM Students of Liceo de Sto. Tomas de Aquinas*

---

## Identity

Science + Technology + Hydration + Futurism + Philosophy + Humor + Personalization

Smart Euclid is a smart hydration companion, not a generic health tracker. It features an interactive robot companion (default nickname **Albert Camus**), absurdist & existentialist quotes, dynamic dark futuristic visuals, streaks, achievements, optional camera verification, and highly customizable reminders.

---

## Core Features

- **Manual water logging** — quick presets (100 / 150 / 250 / 350 / 500 mL) + custom amount
- **Hydration visualization** — living progress display that responds to your intake
- **Smart reminders** — interval + school-aware schedule (respects class time, prioritizes breaks & lunch)
- **Optional camera drinking verification** — detects a drinking gesture, then *you* confirm the amount (never claims precise milliliter measurement)
- **Robot companion** — renameable, with personality presets (Philosophical, Cheerful, Sarcastic, Calm, Scientific, Chaotic). Reacts to progress, logs, streaks, and goals
- **Thought of the Day** + rotating original absurdist / existential quotes
- **Streaks & achievements** — First Sip, Still Alive, Existentially Hydrated, Sisyphus Would Approve, and more
- **Statistics & history** — daily/weekly views, averages, editable timeline
- **Profile** — goal, schedule, camera toggle, robot customization, privacy-first local storage
- **Onboarding** — multi-step setup (name, goal, wake/sleep, school, robot)

No medical claims. No automatic exact volume detection. Manual logging is always available and remains the reliable core.

---

## Technology

- Single-file React (CDN) + Tailwind CSS (CDN) — no build step required
- localStorage persistence
- Progressive Web App ready (manifest + service worker)
- Works on ordinary Android devices and can be installed to the home screen

---

## How to use / deploy

1. Open the live site (GitHub Pages) or open `index.html` in a modern mobile browser.
2. Enable GitHub Pages on this repository if not already active (Settings → Pages → Deploy from branch `main`).
3. Share the Pages URL with participants. On Android/iOS they can “Add to Home Screen” for a full-screen app-like experience.

All data stays on the user’s device.

---

## Research notes

- Camera verification is optional and must be explicitly enabled by the user.
- The camera never assigns a milliliter value; the user always confirms the amount.
- Reminders in this web prototype fire while the app is open or installed; a future native build can add full background notifications and custom ringtone upload.
- Designed for practical student use: log in seconds, school schedule support, no constant interaction required.

---

**Smart Euclid**  
Stay hydrated. Question existence later.
