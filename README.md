# ⚽ Friends World Cup 2026 Draft Tracker

Live standings for a 7-person fantasy draft pool following the **2026 FIFA World Cup** (June 11 – July 19, 2026).

🌐 **[View the live site](https://rhall2968-dev.github.io/friends-worldcup-tracker/)** (coming soon)

---

## Draft Picks

| | Cole | Markus | J Mill | Joey | Logan | Ryan | Austin |
|--|------|--------|--------|------|-------|------|--------|
| 1 | France | Spain | Argentina | England | Germany | Portugal | Brazil |
| 2 | Senegal | Norway | Morocco | Belgium | Croatia | Colombia | Netherlands |
| 3 | Uruguay | Ivory Coast | Ecuador | Switzerland | USA | Japan | Mexico |
| 4 | Turkey | South Korea | Austria | Canada | Egypt | Sweden | Australia |
| 5 | Ghana | Tunisia | Czechia | Paraguay | Algeria | Scotland | Iran |

---

## Scoring

| Result | Points |
|--------|--------|
| Win | 3 |
| Overtime Win (ET or Penalties) | 2 |
| Tie | 1 |
| Overtime Loss (ET or Penalties) | 1 |
| Loss | 0 |

---

## How It Works

- **Site:** Static HTML/CSS/JS hosted on [GitHub Pages](https://pages.github.com/)
- **Data:** Match results fetched from [worldcup26.ir](https://worldcup26.ir) — free, no API key required
- **Updates:** GitHub Actions runs every night at 4am Eastern, fetches all finished matches, recalculates standings, and commits `data/standings.json`
- **Manual trigger:** Go to **Actions → Update World Cup Standings → Run workflow** to pull the latest results on demand

---

## Project Structure

```
worldcup-tracker/
├── index.html               # Main site
├── style.css                # Styles
├── script.js                # Frontend — reads standings.json and renders the page
├── data/
│   └── standings.json       # Auto-updated nightly by GitHub Actions
├── scripts/
│   └── fetch_standings.py   # Fetches match results and writes standings.json
└── .github/
    └── workflows/
        └── update-standings.yml  # Nightly cron job
```

---

## Tournament

- **Opening match:** June 11, 2026 — Mexico City
- **Final:** July 19, 2026 — New Jersey
- **Format:** 48 teams, 12 groups, 104 total matches
