# College Football Eliminator

> **Standalone website distribution:** all 138 logos, schedules, styles, and application code are embedded in `index.html`. Open it directly or enable GitHub Pages using **Deploy from a branch → main → / (root)**. The source folders and development commands described below apply to the original College Football Eliminator project on your computer; this repository contains the ready-to-use website.

A personal 2026 college football workspace with all **138 FBS teams**. The website has no runtime dependencies, accounts, API keys, or build requirement. Your rankings stay in your own browser.

Backfield Football branding uses a black-and-gold default theme and an optional gold-and-white light theme. The theme selection is saved in this browser. **Quick tutorial** explains ranking, saving history, and exporting a backup.

## Open the website

- **Localhost:** double-click `Start Localhost.cmd`, then open **http://localhost:4173**. Node.js 24 is available on the development computer. Keep the command window open while using the site.
- **Completely offline:** open `index.html` directly. Keep the adjacent scripts, stylesheet, and `assets` folder together. Logos and the full 2026 schedule snapshot are included.
- **GitHub Pages:** the target repository is [schaafconnor0-collab/CollegeFootballEliminator](https://github.com/schaafconnor0-collab/CollegeFootballEliminator). See publication instructions below.

## Ranking and elimination

- Drag a team before another, use the up/down buttons, or click its rank to enter a position.
- Conference rankings are filtered views of the **same national power ranking**. Moving the 14th Big Ten team above the 13th places it immediately ahead of that team nationally. National changes also change conference order.
- The playoff eliminator has an **independent order of playoff hopes**, initially copied from the alphabetical power board. Every team still displays its power rank. Use **Use power order** to copy your current power order into the eliminator.
- Click × or drop a team in the eliminated section to eliminate it. Restore it with ↶. This never removes a team from power rankings. Elimination is your opinion; the app does not automatically judge postseason eligibility or decide who qualifies.
- Choose a week on the eliminator board, then mark active teams **Safe** or **Hanging by a thread**, or eliminate them. Status changes carry into later weeks until another change. Earlier weeks keep their own status; restoring a team records a safe status for the selected week. Existing eliminations from older backups remain undated until you assign their week.

## Eliminator video

Open **Video Tools → Open eliminator video**. Select **YouTube (1920 × 1080)** or **YouTube Shorts (1080 × 1920)**, choose the week, and start the presentation. Both layouts use team logos without printed team names, ranks or records.

The opening stadium thumbnail automatically features the three highest teams in your current power ranking among those eliminated by the selected week. It uses fewer logos when fewer than three teams have been eliminated. The presentation then shows newly eliminated teams for that week, all other eliminated teams, teams hanging by a thread, and safe teams by conference. The **Group of 6** combines the American, Conference USA, MAC, Mountain West, Pac-12 and Sun Belt; independents have their own group. Empty sections are skipped and large groups continue onto additional slides.

Use the arrow keys, Previous / Next, or click the slide to advance. **Home** returns to the thumbnail and **End** opens the last slide. **Full screen** hides the controls for recording; Escape restores them on the same slide. Download any slide as a **PNG** at the selected dimensions or as a self-contained **SVG**. The presentation captures your status and power rankings when you start, without changing either board. Weekly status history is included in the normal ranking backup.

## Top 25 presentation

Open **Video Tools → Present Top 25** and choose **YouTube** or **YouTube Shorts** before starting.

**YouTube Shorts (1080 × 1920)** shows one fixed board of all 25 rank positions, with logos revealed in five cumulative groups: **25–21, 20–16, 15–11, 10–6, and 5–1**. Earlier reveals stay visible. There are exactly five slides, with only rank numbers and team logos on the board. Each slide downloads as a portrait PNG or self-contained SVG. Home returns to the first five-team reveal; End shows all 25 teams.

For **YouTube**, choose **three different teams** for the opening thumbnail, then **Start presentation**. The selectors include all 138 teams and remember your choices in this browser. A live preview shows the left, upper-right and lower-right logos over a stadium background. The first slide can be downloaded as a **1920 × 1080 PNG** or SVG from the toolbar.

After the opening thumbnail, count down from **No. 25 to No. 1 using your own current national power rankings**. Conference filters, search results and playoff-hopes order do not change the presentation. Each team slide includes its season record, full schedule, latest completed game and saved power ranking history. The final slide creates a Top 25 graphic with all teams, records and ranking movement.

Before starting, optionally enable **Include a “Just missed out” slide**. Choose an ending rank from **27 through 35**: the graphic includes every team from **26** to that rank (2–10 teams). It appears after the opening thumbnail and before No. 25 and has its own download buttons.

Use **Previous / Next**, arrow keys, Page Up / Page Down, or Space on the slide. **Home** returns to the opening thumbnail, **End** opens the final graphic, and **Esc / Close** exits. **Full screen** is available in supporting browsers and hides the controls. The Top 25 and Just missed out graphics retain their **1600 × 1000 PNG** or scalable **SVG** downloads. On smaller screens, scroll those ranking graphics horizontally to read every team; the thumbnail fits the screen at 16:9.

The presentation freezes the current board and available score data when started. It does not create history, save the board, or discard draft edits. Ranking graphs show up to 12 recent saved power rankings and a separate current-board point; no history is invented for an unsaved team. Movement compares with its latest eligible save, excluding the current week's automatic snapshot. Refresh scores or download schedules before presenting for newer results.

Presentations work offline. The portable `publish/index.html` embeds logos for offline graphic downloads. When opening the source `index.html` directly, some browsers block reading local logos for export; the downloaded graphic uses team abbreviations for unavailable logos. Localhost and the hosted version embed the downloaded logos normally.

## Playoff predictor presentation

Open **Video Tools → Open playoff predictor** and choose **YouTube** or **YouTube Shorts**. Choose contenders and a projected champion for the ACC, Big Ten, Big 12 and SEC. The **Group of 6** combines the American, Conference USA, MAC, Mountain West, Pac-12 and Sun Belt into one contender pool with one projected automatic qualifier.

**YouTube Shorts (1080 × 1920)** finishes setup after the twelve seeds are assigned; game-winner picks are not required. Its 13-slide portrait presentation goes directly to a blank bracket, reveals the five automatic qualifiers first, then the seven at-large teams in seed order, and ends with the complete field. Team slots show logos and seed numbers. It has no thumbnail, conference slides or game-result predictions. Each slide downloads as a portrait PNG or self-contained SVG. Switching formats preserves existing prediction picks.

Place twelve different teams using the dropdown beside each seed on the bracket. All 138 teams, including independents, are available; chosen teams disappear from the other dropdowns. All four projected conference champions and the Group of 6 qualifier must appear before **Predict the games** becomes available. The top four seeds receive byes; champions are not restricted to those seeds. First-round matchups are 8–9, 5–12, 6–11 and 7–10, feeding seeds 1, 4, 3 and 2 respectively.

For **YouTube**, click the winning team in each of the eleven games. A later matchup becomes selectable once both teams are known. Changing a seed or result removes subsequent picks that no longer fit. Once a champion is selected, **Create presentation** opens a 35-slide deck:

1. A gold-and-charcoal title thumbnail with an obscured, anonymous bracket. It contains no selected teams, seeds, logos or results, including in its exported SVG.
2. Two slides per conference group: the selected contenders' logos, followed by the same lineup with the projected winner circled.
3. A blank bracket, then each of the five automatic qualifiers in its assigned seed, followed by each remaining team from highest to lowest seed.
4. One game result per slide through the first round, quarterfinals, semifinals and championship. The final slide shows the completed bracket and states “[Team] wins the national championship,” using the selected winner’s name.

Click the slide or use **Next**, arrow keys, Page Up / Page Down, or Space to reveal the next pick. **Home** returns to the thumbnail; **End** goes to the completed bracket. **Full screen** hides the controls; Escape restores them on the same slide. Each slide downloads as a **1920 × 1080 PNG** or self-contained **SVG**. On narrow screens the editable bracket scrolls horizontally; presentation slides fit the screen.

Predictions save separately from ranking boards in this browser. Use **Export prediction / Import prediction** inside the tool to move a prediction between localhost and GitHub Pages. Ranking backup files do not include predictions. These are personal projections: the tool enforces the five requested qualifying picks and bracket structure, rather than calculating official committee rankings or postseason eligibility.

## Ranking history and saving

- **History starts only when you first click Save ranking on that board.** The initial alphabetical order and unsaved edits are never included in the graphs or movement indicators.
- After the first explicit save, future weeks record your latest order automatically when you use the app. Manual snapshots stay fixed, and the app does not add an automatic snapshot to a week that already has a manual save.
- Open a team to see its schedule and separate power/playoff graphs. Click a graph point, then confirm, to remove only that team's historical entry. Ranking history also lets you view or delete entire snapshots with confirmation.
- Rankings save in browser storage. **Export backup** downloads a portable JSON file with both boards, eliminations, and history. **Import backup** validates and restores it after confirmation.
- Leaving a ranking board with changes since its last explicit save offers **Save and continue**, **Continue without saving**, or **Stay on this board**. Saving records a snapshot before navigating; continuing without saving preserves the browser draft without adding history. Unchanged boards do not interrupt navigation.
- Closing or reloading a page with unsaved changes requests the browser's standard warning where supported. A browser cannot block switching to another browser tab. If browser storage is unavailable, saving also starts a JSON backup download.
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

Requests use the calendar's **explicit date ranges**, including the exclusive end date, so the final day of each week is included. Week-only requests can return just a limited selection of games. Scoreboards merge refreshed results with known schedules and cached games, using the newest available copy of each game. An incomplete refresh cannot hide a known matchup. Cached full-season schedules allow every week to be browsed offline. Times use the device's timezone. Postseason and unresolved opponents only appear once announced by the source.

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

The editable local source and GitHub distribution have separate histories. Publish only the six files from `publish/` (`index.html`, `sw.js`, `manifest.webmanifest`, `favicon.png`, `README.md` and `.nojekyll`) onto the existing GitHub `main` history. Never replace it with the local source history or force-push it. Pages uses **Deploy from a branch → main → / (root)**. The compact distribution embeds all logos, data, styles, and scripts in `index.html`, with a small separate service worker for offline web access. It can also be opened offline as a single HTML file.

Live URL: [College Football Eliminator](https://schaafconnor0-collab.github.io/CollegeFootballEliminator/). Verify that Pages finishes deploying and the live files match the build after each publication.

## Privacy and publication safeguards

Rankings and backups stay on the visitor's device. The app has no accounts, analytics, advertising, tracking pixels, or upload endpoint. Live score requests go only to ESPN and explicitly omit cookies and the page referrer. GitHub and ESPN still receive ordinary connection information, such as an IP address, when their services are contacted.

The local server binds only to the loopback interface and serves an explicit list of public website assets. Backups, project documentation, dependencies, hidden files, and development scripts cannot be requested through it. The build rejects unexpected files in `dist/` and `publish/`; keep personal backups outside those output folders. The offline worker caches only this site's listed assets, with a separate cache name per site path.

Public commits also carry author metadata. Use GitHub's private-email setting for browser commits and a no-reply email for command-line commits. A clean website package alone does not make old Git history private.

## Sources and ownership

- [ESPN teams](https://www.espn.com/college-football/teams): current team IDs, names, and logos.
- [2026–27 College Football Playoff format](https://collegefootballplayoff.com/sports/2024/5/29/12-team-format): automatic qualifiers, seeding, byes and bracket paths.
- [Pac-12 2026 football schedule](https://pac-12.com/news/2026/2/9/general-the-new-pac-12-announces-its-2026-football-schedule.aspx).
- [NDSU FBS FAQ](https://gobison.com/sports/2026/2/9/fbs-frequently-asked-questions): 2026 Mountain West membership.
- [Sacramento State joins the MAC](https://hornetsports.com/news/2026/2/16/hornet-football-to-join-the-mac-in-2026.aspx).
- [2026 Sun Belt schedule](https://sunbeltsports.org/news/2026/3/13/sun-belt-announces-2026-football-schedule.aspx): Louisiana Tech replaces Texas State.

`assets/logo-sources.json` records every local logo's actual source URL and team source page. Team names and marks belong to their respective owners. These identification assets are not represented as royalty-free stock imagery. No affiliation with ESPN, the NCAA, conferences, or teams is implied.

All project source, downloaded images, dependency files, build artifacts, and project tooling stay in the College Football Eliminator folder. No system-wide package installation is needed.
