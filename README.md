# TaskFlow

An offline, iOS-styled task and reminder app. Type a task in plain English and it becomes a scheduled card.

> `tomorrow 7:30-10:30 contest on Codeforces` → **Contest on Codeforces**, tomorrow, 7:30 – 10:30 PM

## Features (v4.0)
- Timetable tab: subjects, weekly classes (days, times, room, teacher), holidays (single day or range), cancel one class, today's classes card, class reminders; tap a class to add homework that is saved under the subject and also appears as a normal task
- Natural-language input: `tomorrow 7:30-10:30 contest on Codeforces !high #cp`, `every mon wed fri 5pm class`, `daily except sunday 6am gym`
- Compact task boxes (title and time), colored by priority; tap a box for details, description, steps and history; Edit opens a full editor with iOS-style wheel pickers for date and time
- Repeating tasks: marking one done counts only for today and it returns automatically on its next day
- Contest import from Codeforces, LeetCode, CodeChef and AtCoder (best effort; needs internet)
- Today dashboard with progress bar and a live Next up countdown, Upcoming tab grouped by date, Progress tab with streaks
- Morning summary notification and automatic backup to Documents/TaskFlow (Android app)
- Settings: theme, accent color, reminders, 12/24-hour time, backup and restore
- Android Back button goes to the previous screen; it exits the app only from the Today screen
- Works fully offline; data stays on the device

## Run it
Open `docs/index.html` in a browser. No build step.
Reminders in the browser fire while the app is open. For reminders that fire when the app is closed, build the Android app below.

## Get the Android APK (no Android Studio needed)
1. Push this repo to GitHub.
2. Open the **Actions** tab, choose **Build Android APK**, click **Run workflow**.
3. When it finishes, download **TaskFlow-apk** from the run's Artifacts, unzip it and install `app-debug.apk` on your phone.

The workflow installs Capacitor and the Local Notifications plugin, so reminders fire even when the app is closed. To build locally instead: `npm install @capacitor/core @capacitor/android @capacitor/local-notifications @capacitor/filesystem`, `npm install -D @capacitor/cli`, `npx cap add android`, `npx cap sync`, `npx cap open android`.

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
- [x] v5: morning summary, automatic backup
- [x] v6: contest import, redesign, details and editor

## Tech
Vanilla HTML, CSS and JavaScript in a single file. Capacitor for the Android wrapper.
