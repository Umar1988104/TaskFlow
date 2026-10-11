# TaskFlow

An offline, iOS-styled task and reminder app. Type a task in plain English and it becomes a scheduled card.

> `tomorrow 7:30-10:30 contest on Codeforces` → **Contest on Codeforces**, tomorrow, 7:30 – 10:30 PM

## Features (v1.0)
- Natural-language parser (dates, times, ranges, categories) written from scratch, no libraries or AI
- Live preview of how your sentence is understood
- Grouped list: Overdue, Today, Tomorrow, Upcoming, Completed
- Multiple reminders per task (1 day, 1 hour, 10 min, at the time) plus snooze
- Recurring tasks: `every sunday 8pm contest`, `daily 6am revise`, `weekly maths homework`
- Steps (subtasks) with progress, and links: paste a URL in the sentence and it becomes an "Open link" button
- Swipe right to complete, swipe left to delete; urgency colors for tasks due soon or overdue
- Progress: day streak, tasks done this week, on-time rate and a 7-day chart
- Backup: download, copy or restore all tasks as JSON
- Installable and offline-capable (PWA manifest + service worker), Android APK built automatically with GitHub Actions
- Works fully offline, data stays on the device (localStorage)
- iOS-style UI with animations, dark mode support

## Run it
Open `docs/index.html` in a browser. No build step.
Reminders in the browser fire while the app is open. For reminders that fire when the app is closed, build the Android app below.

## Get the Android APK (no Android Studio needed)
1. Push this repo to GitHub.
2. Open the **Actions** tab, choose **Build Android APK**, click **Run workflow**.
3. When it finishes, download **TaskFlow-apk** from the run's Artifacts, unzip it and install `app-debug.apk` on your phone.

The workflow installs Capacitor and the Local Notifications plugin, so reminders fire even when the app is closed. To build locally instead: `npm install @capacitor/core @capacitor/android @capacitor/local-notifications`, `npm install -D @capacitor/cli`, `npx cap add android`, `npx cap sync`, `npx cap open android`.

On Android 13+ allow notifications when asked. On Android 12+ also allow "Alarms & reminders" for the app in system settings for exact timing.

## Updating the installed app
Every build is signed with the key in `signing/debug.keystore` and gets a higher version number, so a new APK installs over the old one and keeps your tasks. Never uninstall first. (This is a debug key meant for personal use, not for publishing on the Play Store.)

## Hosting
Enable GitHub Pages with source `main` and folder `/docs` to get a live demo link.

## Roadmap
- [x] v1: parser, offline storage, iOS-style list
- [x] v2: reminders and snooze
- [x] v3: recurring tasks, steps, links, swipe gestures, urgency colors
- [x] v4: streaks and stats, backup/export, installable offline app

## Tech
Vanilla HTML, CSS and JavaScript in a single file. Capacitor for the Android wrapper.
