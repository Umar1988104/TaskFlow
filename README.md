# TaskFlow

An offline, iOS-styled task and reminder app. Type a task in plain English and it becomes a scheduled card.

> `tomorrow 7:30-10:30 contest on Codeforces` → **Contest on Codeforces**, tomorrow, 7:30 – 10:30 PM

## Features (v0.2)
- Natural-language parser (dates, times, ranges, categories) written from scratch, no libraries or AI
- Live preview of how your sentence is understood
- Grouped list: Overdue, Today, Tomorrow, Upcoming, Completed
- Multiple reminders per task (1 day, 1 hour, 10 min, at the time) plus snooze
- Works fully offline, data stays on the device (localStorage)
- iOS-style UI with animations, dark mode support

## Run it
Open `docs/index.html` in a browser. No build step.
Reminders in the browser fire while the app is open. For reminders that fire when the app is closed, build the Android app below.

## Build the Android app (Capacitor)
```bash
npm install @capacitor/core @capacitor/android @capacitor/local-notifications
npm install -D @capacitor/cli
npx cap add android
npx cap sync
npx cap open android   # then Run / Build APK in Android Studio
```
The app detects the Local Notifications plugin automatically and schedules real notifications. Follow the plugin docs for Android permissions.

## Hosting
Enable GitHub Pages with source `main` and folder `/docs` to get a live demo link.

## Roadmap
- [x] v1: parser, offline storage, iOS-style list
- [x] v2: reminders and snooze
- [ ] v3: recurring tasks, subtasks, links, swipe gestures
- [ ] v4: streaks, backup/export, polish

## Tech
Vanilla HTML, CSS and JavaScript in a single file. Capacitor for the Android wrapper.
