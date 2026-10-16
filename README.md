# TaskFlow

An offline-first task, timetable and reminder app for students. Type a task the way you speak (English or Hinglish) and it becomes a scheduled card. Built with plain HTML, CSS and JavaScript in a single file, packaged as an Android app with Capacitor.

> `kal shaam 7 baje contest` -> **Contest**, tomorrow, 7:00 PM, reminders set

## Screenshots
Add your screenshots to `docs/screenshots/` and list them here:

| Today | Timetable | Weekly review |
|---|---|---|
| `docs/screenshots/today.png` | `docs/screenshots/timetable.png` | `docs/screenshots/review.png` |

## Features (v5.0)
**Tasks**
- Natural-language input in English and Hinglish: dates, times, ranges, repeats, priority (`!high`), tags (`#dsa`), links
- Compact task boxes colored by priority; tap for details, description, steps and history; Edit with iOS-style wheel pickers
- Repeating tasks (daily, weekdays, custom days): done counts for today only and returns on its next day
- Swipe to complete or delete, long-press menu, undo bar, search, reschedule overdue tasks
- Week strip, list or day-timeline view, focus mode, big + quick-add sheet

**Timetable**
- College-style layout: month card, week chips, period cards with time, room, subject and teacher
- Set period times once, add a class to several days and periods at once, copy a day, holidays and cancelled classes
- Tap a class to add homework: saved under the subject and shown as a normal task
- Class reminders, optional timetable end date

**Insights**
- Weekly review (share as text, Sunday notification), 17-week heatmap, streaks, homework progress per subject

**Integrations**
- Contest import from Codeforces, LeetCode, CodeChef and AtCoder, with contest cards and countdowns
- Morning summary notification, automatic backup to Documents/TaskFlow, backup and restore

**Look and feel**
- Theme packs (Default, AMOLED, Paper, Midnight, Sakura), accent colors, text size, left-handed mode, welcome screens
- Works fully offline; all data stays on the device

## Run it
Open `docs/index.html` in a browser. No build step. Notifications and automatic backup need the Android app.

## Get the Android APK (no Android Studio needed)
1. Push this repo to GitHub.
2. Open the **Actions** tab, choose **Build Android APK**, click **Run workflow**.
3. When it finishes, download **TaskFlow-apk** from the run's Artifacts, unzip it and install `app-debug.apk` on your phone.

On Android 13+ allow notifications when asked. On Android 12+ also allow "Alarms & reminders" for the app in system settings for exact timing.

## Updating the installed app
Every build is signed with the key in `signing/debug.keystore` and gets a higher version number, so a new APK installs over the old one and keeps your tasks. Never uninstall first. This is a debug key for personal use, not for the Play Store.

## Hosting
Enable GitHub Pages with source `main` and folder `/docs` for a live web demo.

## Tech
Vanilla HTML, CSS and JavaScript (no frameworks, one file). Capacitor for the Android wrapper, Local Notifications and Filesystem plugins, GitHub Actions for CI builds. Data is stored in localStorage.

## Roadmap
All planned phases are complete. Ideas: home-screen widget, voice input, calendar month view, sync between phones.
