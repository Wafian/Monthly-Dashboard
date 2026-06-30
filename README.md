# Monthly Dashboard

Single-file, offline-first web apps. No build step — open the HTML files directly
in a browser, or host them on GitHub Pages / Netlify / Vercel.

## Apps
- **`task-tracker.html`** — a TickTick-style task tracker (see below).
- **`expense-tracker.html`** — an installable iPhone expense tracker (see below).

---

# Task Tracker

A TickTick-style task tracker in a single HTML file (HTML + CSS + vanilla JS).
Open `task-tracker.html` in any browser — no server or build step required.

## Features
- **Three-pane layout:** sidebar (views + lists) · task list (grouped by
  Overdue / Today / Next 7 days / Later / No date) · detail panel.
- **Views:** Today, All, Next 7 days, No date, Completed, plus per-list filters
  (MyBL, Rider Pack, Creative, Brand).
- **Priority** (P1–P4) shown as colored circular checkboxes; click to complete.
- **Subtasks**, expandable inline and editable in the detail panel.
- **Detail panel edits:** title, deadline, priority, status, list, internal /
  external stakeholders, notes, and subtasks.
- **Add tasks** from the top bar (Enter); **sort** toggle (deadline, then priority).
- **Reset** button restores the original seed list.

## Storage
On-device via `localStorage` (key `tasks-v1`). Data stays in your browser; it
seeds a starter list on first load.

---

# Expense Tracker

A single-file, offline-first expense tracker built as an installable iPhone web app.
No build step; open `expense-tracker.html` in a browser or add it to your Home Screen.

## Features
- **Four tabs:** Dashboard, Add, Log, Settings.
- **On-device storage** via `localStorage` (key `wafianExpenseTracker_v1`), with JSON
  backup export/import and CSV export.
- **Multi-month:** month switcher in the header and a Months manager in Settings.
  New months carry the previous month's frozen balance forward.
- **Editable budgets** and per-month name, days, initial balance, and frozen balance.
- **Charts** (Chart.js via CDN): daily spend trend, category doughnut, and payment-method
  breakdowns.
- **Effective spend:** `sum(all totals) + initialBalance − frozenBalance`.
- **Splits in the Add form:** Just me / 50-50 / 3-way / Custom.
- **Dark mode:** Auto (follows the system appearance), or force Light/Dark in Settings.
  The preference persists and is included in JSON backups.

## Install on iPhone
1. Host the file (e.g. GitHub Pages) and open the URL in **Safari**.
2. **Share → Add to Home Screen.** It launches full-screen as a standalone app.

## Privacy
The committed `expense-tracker.html` ships with **no personal data** — it starts empty.
Restore your own data on-device via **Settings → Import backup (.json)**.
