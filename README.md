# Nifty Dashboard Data

Public data feed for the Nifty option-seller mobile dashboard.

## Endpoint (once pushed)
```
https://raw.githubusercontent.com/<your-username>/<repo-name>/main/data.json
```

Your mobile app polls this URL. No auth needed for a public repo.

## Updating data
Edit `data.json`, then:
```
git add data.json
git commit -m "update: intraday OI refresh"
git push
```
Raw URL reflects new content within seconds (may be CDN-cached ~5 min).

## Files
- `data.json` — current dashboard payload (index closes, OI levels, participant positioning, strategy)
