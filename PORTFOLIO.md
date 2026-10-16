# TaskFlow: portfolio kit

## GitHub "About" text (paste into the repo description)
Offline-first student planner: natural-language (English + Hinglish) task input, weekly timetable with homework, reminders, weekly review. Vanilla JS + Capacitor Android app built by GitHub Actions.

**Topics to add:** `javascript` `pwa` `capacitor` `android` `offline-first` `task-manager` `timetable` `natural-language-processing` `productivity` `vanilla-js`

## Resume bullets (pick 3 or 4)
- Built TaskFlow, an offline-first Android task and timetable app in vanilla JavaScript (single-file, zero dependencies), packaged with Capacitor.
- Wrote a rule-based natural-language parser that turns sentences like "kal shaam 7 baje contest !high #cp" into structured tasks (dates, time ranges, repeats, priority, tags), supporting English and Hinglish.
- Designed a college timetable module with reusable period times, multi-day class entry, holidays, and homework linked to subjects that also appears in the main task list.
- Implemented local notification scheduling (task reminders, class reminders, morning summary, weekly review) and automatic JSON backups to device storage.
- Set up a GitHub Actions pipeline that builds and signs an installable APK with a stable key so updates install over existing data.
- Added analytics views: streaks, 17-week heatmap, weekly review and per-subject homework progress.

## LinkedIn post (draft)
I built a task and timetable app for my own college life, and I use it every day.

You type tasks the way you speak, even in Hinglish ("kal shaam 7 baje contest") and it sets the date, time and reminder. You enter your timetable once, tap a class to add homework, and it shows up in your task list. It also gives a weekly review, a focus mode and works completely offline.

Built with plain JavaScript, wrapped as an Android app with Capacitor, and built automatically with GitHub Actions.

Code and APK: <your GitHub link>

## 30-second demo script
1. Type "kal shaam 7 baje contest zaruri #cp" and show the chips and the created task.
2. Open Timetable, show a day with 8 periods, tap a class, add homework.
3. Go back to Today: show the homework as a task, long-press it, reschedule.
4. Show the week strip, then Timeline view.
5. Open Progress: heatmap and weekly review.

## Screenshots to capture (phone, light and dark)
Today list, Today timeline, Timetable day, class sheet with homework, task details, weekly review, heatmap, Settings theme packs, contest import.
