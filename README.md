# College Football Eliminator

> **Standalone website distribution:** all 138 logos, schedules, styles, and application code are embedded in `index.html`. Open it directly or enable GitHub Pages using **Deploy from a branch → main → / (root)**. The source folders and development commands described below apply to the original College Football Eliminator project on your computer; this repository contains the ready-to-use website.

A personal 2026 college football workspace with all **138 FBS teams**. The website has no runtime dependencies, accounts, API keys, or build requirement. Your rankings stay in your own browser.

## Open the website

- **Localhost:** double-click `Start Localhost.cmd`, then open **http://localhost:4173**. Node.js 24 is available on the development computer. Keep the command window open while using the site.
- **Completely offline:** open `index.html` directly. Keep the adjacent scripts, stylesheet, and `assets` folder together. Logos and the full 2026 schedule snapshot are included.
- **GitHub Pages:** the target repository is [schaafconnor0-collab/CollegeFootballEliminator](https://github.com/schaafconnor0-collab/CollegeFootballEliminator). See publication instructions below.

## Ranking and elimination

- Drag a team before another, use the up/down buttons, or click its rank to enter a position.
- Conference rankings are filtered views of the **same national power ranking**. Moving the 14th Big Ten team above the 13th places it immediately ahead of that team nationally. National changes also change conference order.
- The playoff eliminator has an **independent order of playoff hopes**, initially copied from the alphabetical power board. Every team still displays its power rank. Use **Use power order** to copy your current power order into the eliminator.
- Click × or drop a team in the eliminated section to eliminate it. Restore it with ↶. This never removes a team from power rankings. Elimination is your opinion; the app does not automatically judge postseason eligibility or decide who qualifies.

## Ranking history and saving

- **History starts only when you first click Save ranking on that board.** The initial alphabetical order and unsaved edits are never included in the graphs or movement indicators.
- After the first explicit save, future weeks record your latest order automatically when you use the app. Manual snapshots stay fixed, and the app does not add an automatic snapshot to a week that already has a manual save.
- Open a team to see its schedule and separate power/playoff graphs. Click a graph point, then confirm, to remove only that team's historical entry. Ranking history also lets you view or delete entire snapshots with confirmation.
- Rankings save in browser storage. **Export backup** downloads a portable JSON file with both boards, eliminations, and history. **Import backup** validates and restores it after confirmation.
- The file, localhost, and GitHub Pages versions have **separate browser storage**. Move rankings between them with Export/Import. Clearing browser data and private browsing can remove automatic saves. Keep exported copies. File URL storage is browser dependent; localhost is recommended for reliable automatic saving.
- A browser page cannot save weekly changes while closed. It records later weeks when you next open or use it.

## Live scores and offline behavior

| Version | Rankings, logos, history | Live scores online | Offline scores and schedules |
| --- | --- | --- | --- |
| Open `index.html` | Yes; browser saving varies for file URLs | Yes if the browser permits the public feed | Included snapshot plus successfully saved updates |
| Localhost | Yes | Yes | Included snapshot plus saved updates |
| GitHub Pages (HTTPS) | Yes | Yes | Included snapshot plus saved updates; service worker caches the website after an initial successful online visit |

The scoreboard refreshes every **60 seconds while the page is visible and online**. Open team details refresh that team's schedule. **Download all schedules** updates all 138 teams and confirms whether the website itself was cached for offline reopening. The downloaded project folder always works offline without a prior visit.

Scores **cannot update without internet**. The interface shows download timestamps and keeps previous data when a request fails. The live adapter uses ESPN's public JSON feed, which currently returns `Access-Control-Allow-Origin: *`; this was verified for the target GitHub Pages origin on September 6, 2026 (Central time). It is an unofficial, unsupported feed and can change or become unavailable. No reliability or availability guarantee is implied. There is no proxy server, paid subscription, or secret API key.

Requests use the calendar's **explicit date ranges** because week-only requests can return just a limited selection of games. Cached full-season schedules allow every week to be browsed offline. Times use the device's timezone. Postseason and unresolved opponents only appear once announced by the source.

## Development and publishing

```powershell
npm ci --ignore-scripts
npm test
npm run build
npm start
```

`npm run build` validates 138 local logo files and produces `dist/` plus the root service worker. It leaves the root `index.html` directly usable. Development dependencies are used only for tests; visitors download no npm packages.

To refresh the bundled 2026 schedules, scoreboard, and missing logos:

```powershell
npm run refresh-data
npm run build
```

The complete source can be committed to the supplied repository's `main` branch. In **Settings → Pages → Build and deployment**, choose **GitHub Actions**. The included `.github/workflows/pages.yml` tests the source, builds `dist/`, and publishes it. GitHub write access is needed to upload code; repository settings access is needed to enable Pages.

Alternatively, upload the contents of the generated `publish/` directory to the repository root and select **Deploy from a branch → main → / (root)** in Pages settings. This compact distribution embeds all logos, data, styles, and scripts in `index.html`, with a small separate service worker for offline web access. It can also be opened offline as a single HTML file.

Expected URL once GitHub confirms deployment: `https://schaafconnor0-collab.github.io/CollegeFootballEliminator/`. A prepared repository is not evidence that the site has been published.

## Sources and ownership

- [ESPN teams](https://www.espn.com/college-football/teams): current team IDs, names, and logos.
- [Pac-12 2026 football schedule](https://pac-12.com/news/2026/2/9/general-the-new-pac-12-announces-its-2026-football-schedule.aspx).
- [NDSU FBS FAQ](https://gobison.com/sports/2026/2/9/fbs-frequently-asked-questions): 2026 Mountain West membership.
- [Sacramento State joins the MAC](https://hornetsports.com/news/2026/2/16/hornet-football-to-join-the-mac-in-2026.aspx).
- [2026 Sun Belt schedule](https://sunbeltsports.org/news/2026/3/13/sun-belt-announces-2026-football-schedule.aspx): Louisiana Tech replaces Texas State.

`assets/logo-sources.json` records every local logo's actual source URL and team source page. Team names and marks belong to their respective owners. These identification assets are not represented as royalty-free stock imagery. No affiliation with ESPN, the NCAA, conferences, or teams is implied.

All project source, downloaded images, dependency files, build artifacts, and project tooling stay in the College Football Eliminator folder. No system-wide package installation is needed.
