# Vardhan Dairy Farm — Operations Tracker

A free, single-page web app for running Vardhan Dairy Farm's day-to-day operations: milk production, customer deliveries and billing, worker attendance, and expenses/profit tracking.

This is a self-built alternative to a vendor proposal that quoted ₹1,50,000 development + ₹8,000/month maintenance for a full multi-role platform (admin/worker/customer logins, backend server, database, AI features, payment gateway). This MVP covers the same day-to-day tracking needs for the owner, at no build or hosting cost:

- No backend, database, or hosting bill — it's a static HTML/CSS/JS page.
- All data is stored locally in the browser (`localStorage`) on the device it's used on.
- Deployable for free on GitHub Pages (or just opened as a local file).
- Works offline once loaded; installable as a home-screen app on phones (PWA manifest included).

## What it tracks

- **Dashboard** — today's production, distribution, revenue, expenses, estimated profit, active customers, pending payments, worker attendance; plus a monthly view with an expense breakdown and top outstanding customers.
- **Production** — daily milk production entries by shift, worker, and quantity, with monthly totals.
- **Customers** — customer profiles (daily quantity, rate per litre), daily delivery logging (with a bulk "log today with defaults" shortcut), running billed/paid/outstanding balance, and payment recording.
- **Workers** — worker profiles and one-tap daily present/absent attendance marking, with a monthly attendance summary.
- **Expenses** — categorized expense entries (feed, veterinary, salaries, utilities, etc.) with monthly category breakdowns.
- **Backup** — one-tap export/import of all data as a JSON file, since everything lives only in the browser.

## Current limits (by design, for this first version)

- Single admin/device use — no separate worker or customer logins, no multi-device sync (data doesn't automatically appear on a second phone/computer).
- No online payment gateway, SMS/WhatsApp notifications, or AI features.

## Running it

Just open `index.html` in a browser, or serve the folder as a static site (e.g. GitHub Pages).

## Phase 2 (when ready to go multi-user)

Once this is validated for daily use, the natural next step is adding a small shared backend (e.g. Supabase/Firebase or a lightweight API + database) so the owner, workers, and customers can all see live, synced data from their own devices — without the ₹8,000/month vendor maintenance cost.
## Deploy with Netlify

The repo includes a `netlify.toml` (static site, no build step, publishes the root folder).

1. Sign in at [app.netlify.com](https://app.netlify.com) and choose **Add new site → Import an existing project**.
2. Pick **GitHub** and select this repository.
3. Leave the build command empty and the publish directory as `.` (already set by `netlify.toml`), then **Deploy**.

Netlify gives you a URL like `https://<site-name>.netlify.app` and redeploys on every push. For a quick one-off without Git, you can also drag this folder onto [app.netlify.com/drop](https://app.netlify.com/drop).
