# Monthly Dashboard — Expense Tracker

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
