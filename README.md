# FBMS — Football 26 data

**Published data only. No backend code lives here.**

This repository holds the static JSON the **Football 26** Android app reads directly
via GitHub raw. It is generated and refreshed automatically by the crawler in the
separate **FootballServer2026** repo (a scheduled GitHub Action), which fetches from
licensed free sources and pushes the results here.

## Files

| File | Contents |
|---|---|
| `meta.json` | generation time + counts |
| `teams.json` | World Cup team catalog `{ code, name, subName }` |
| `matches.json` | fixtures / live / results |
| `standings/groups.json` | group tables |
| `news.json` | featured + article headlines (link-out to publishers) |

## Read from the app

```
https://raw.githubusercontent.com/com-socby-qbase/FBMS/main/teams.json
https://raw.githubusercontent.com/com-socby-qbase/FBMS/main/matches.json
https://raw.githubusercontent.com/com-socby-qbase/FBMS/main/standings/groups.json
https://raw.githubusercontent.com/com-socby-qbase/FBMS/main/news.json
```

(raw is CDN-cached ~5 min; cache-bust against `meta.generatedAt` if needed.)

## Attribution

Match data via **TheSportsDB** (thesportsdb.com). News headlines link to their
original publishers (BBC Sport, The Guardian, Sky Sports); no article bodies are stored.
See `meta.attribution` in each file.
