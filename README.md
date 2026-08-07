# Nifty Option Seller Terminal

Full dashboard terminal (`index.html`) + data feed (`data.json`) for the Nifty option-seller mobile/web dashboard.

## View the live dashboard (GitHub Pages)
1. Push this repo to GitHub (see below).
2. Repo → Settings → Pages → Source: `main` branch, `/ (root)` → Save.
3. Your dashboard is live at:
```
https://<your-username>.github.io/<repo-name>/
```
GitHub Pages takes 1-2 minutes to build after your first push.

## Raw data endpoint (for a native mobile app instead of the web page)
```
https://raw.githubusercontent.com/<your-username>/<repo-name>/main/data.json
```
No auth needed for a public repo.

## Push to GitHub
```
git init
git add .
git commit -m "init: nifty terminal dashboard"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## Updating data
Edit `data.json` (or regenerate it from the option chain), then:
```
git add data.json
git commit -m "update: intraday OI refresh"
git push
```
`index.html` fetches `data.json` fresh on every page load — just refresh the browser tab after pushing. Raw/Pages content reflects new pushes within seconds to a few minutes (CDN cache).

## Files
- `index.html` — the dashboard terminal (dark theme, full option chain table, support/resistance walls, participant OI, strategy panel)
- `data.json` — data payload the dashboard reads (index closes, full 113-strike option chain, OI levels, participant positioning, strategy legs)
