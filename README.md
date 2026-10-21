# Payoff Planner

A self-contained web app: one-time entry of bills and debt payments, carried forward
on their own cadence (weekly / biweekly / monthly / quarterly / annual) until the
linked debt balance is paid off. Calendar, monthly breakdown, charts. All data stays
on the device (browser storage) with copy/paste and file backup.

## Put it on an iPad

1. Host this folder anywhere that serves plain files over HTTPS
   (GitHub Pages, Netlify Drop, Cloudflare Pages - all free).
2. Open the URL in Safari on the iPad.
3. Tap Share -> "Add to Home Screen".

After that it launches like an app, runs offline (sw.js caches it), and keeps
its data in that app's own storage. Use Settings -> Backup to keep a copy.

## Import from Excel

Settings -> "Import from the Excel template" (or "Import from Excel" on the Bills tab)
reads the Expense_and_Debt_Tracker_Template.xlsx workbook: the Debt Tracker and
Expense Entry tabs plus the dropdown lists on Start Here. The reader (SheetJS) is
fetched from cdnjs the first time and cached by sw.js afterwards.

Files: index.html (the whole app), sw.js (offline cache), manifest.json.
