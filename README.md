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

Fill in Payoff_Planner_Import.xlsx (in this folder, and downloadable from the
site at /Payoff_Planner_Import.xlsx): its Bills & Debts and Income tabs are the
app's own fields. Settings -> Import, or "Import from Excel" on the Bills tab.
Every row is previewed before anything is saved. The older
Expense_and_Debt_Tracker_Template.xlsx workbook still imports. The reader (SheetJS) is
fetched from cdnjs the first time and cached by sw.js afterwards.

Files: index.html (the whole app), sw.js (offline cache), manifest.json.
