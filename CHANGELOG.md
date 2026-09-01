# Changelog

Download builds from [Releases](https://github.com/Qinaii/qtracker-spaceaces/releases).

## v2.1.1

Saturn Expansion ready: new quests, Saturn maps, CBS destroy history.

### App
- Ace Quests includes the Saturn Expansion quests (Age of Saturn and the new chain)
- Saturn maps show as S-1, S-2, and S-3 in quest tasks (no more raw Map 34 / 35 / 36)
- Notifications: Saturn station system open, closing soon, and closed (Saturn segment next to Pirate Map)
- Clan Battle Station now lists CBS Destroy History at the bottom (last 20 destroys: who, loser, station, map)

### Data
- Quest titles refreshed from current Space Aces English texts (542 titled quests)
- Quests without an official title stay hidden in Active / All, same as before
- Map IDs 34, 35, 36 labeled S-1, S-2, S-3 everywhere qTracker shows a map

### Packaging
- `qtracker_v2.1.1.exe` plus matching `.sha256` checksum asset

Download builds from [Releases](https://github.com/Qinaii/qtracker-spaceaces/releases).

## v2.1.0

Ace Gates, Ace Quests, and richer notifications.

### App
- Ace Gates: live gate progress, parts, average DMF, and finish rewards
- Ace Quests: Active Quests, Ace Pass tasks, and All Quests with search
- Quest cards show task progress, ship lock, target, and map when the game provides them
- Notifications for Ace Quests: quest complete, optional rewards with icons, optional task complete on multi-task quests
- Notification duration (5 to 30 seconds) under General
- Notification sounds play again (Preview and Test included)
- Sidebar links: Discord and Ko-fi next to Settings / About / Privacy

### Data
- Ace Gates and Ace Quests use your local Space Aces login session
- Reward names use Space Aces item labels (LPC-11, PCC-25, and so on)

### Packaging
- `qtracker_v2.1.0.exe` plus matching `.sha256` checksum asset
- Builds may still be unsigned

Download builds from [Releases](https://github.com/Qinaii/qtracker-spaceaces/releases).

## v2.0.2

Clan Battle Station tracker and notification toggles.

### App
- Clan Battle Station: live Free / occupied slots by map (Battle, home maps), clan tag and build timer
- Under construction vs finished build shown separately when the world feed reports it
- Added Notifications, select sound, adjust volume and enable or disable it
- Notifications page split into General, Pirate Map, and CBS
- Master enable plus per-category enable; each event can be turned on or off on its own
- CBS toasts: build (who + map), spawn finished, destroyed (destroyer when known)
- Pirate Map notification toggles moved into the Pirate Map segment

Download builds from [Releases](https://github.com/Qinaii/qtracker-spaceaces/releases).

## v2.0.1

Full .NET 9 + WPF client (replaces the Python builds). Portable EXE for Windows 10/11.

### App
- Dashboard with live session stats, Overlay HUD (goal, toggles, logo menu), Analytics (mobs / resources / Uri spend)
- Leaderboard (Ranking, Events, Clans, Gates) and Pilot Lookup
- Dailys Best: daily top gains by date
- Faction Change: recent faction switches
- Pirate Map: open / energy / timer when available
- Global Chat: recent public chat from the world feed
- Custom window chrome and themed controls (no default Windows look)
- Optional start with Space Aces, single instance, GitHub update check

### Data
- Your own wallet, log, and rank still come from Space Aces with your local login session
- Leaderboards, Pilot Lookup, Dailys Best, Faction Change, Pirate Map, and Global Chat go through Qinaii's own API server

### Packaging
- `qtracker_v2.0.1.exe` plus matching `.sha256` checksum asset
- Builds may still be unsigned; see AV notes in the README if SmartScreen warns

## v1.0.2

First public .NET packaging line (see tag assets / notes).

## Earlier releases

Python-era tags remain on older releases for history only.

Download builds from [Releases](https://github.com/Qinaii/qtracker-spaceaces/releases).

## v1.0.1

Patch release. Windows 10/11, portable EXE.

### API reliability
- Fixed silent API freeze after session errors (401 with unchanged token no longer loops without UI feedback)
- Stale-poll watchdog while engine or overlay is active: HUD and status show connection issues when polls stop succeeding
- Settings connection status reflects last successful API poll, not only a token on disk
- Settings Retry runs a live probe request
- Diagnostics log in Settings with copy-to-clipboard (no tokens in log)

### Tracking
- Uri shop spend no longer reduces session earned or Uri/h (wallet drop shifts session base)
- Uri/h uses session average (pause excluded), not a rolling poll window

### Analytics
- Uri tab: spend summary for the active period (Today / Weekly / Monthly) from pilot log `item_purchased`
- Summary stat cards use a 3-column layout
- Removed Recent Sessions section from stat charts

### App
- Live UI language switch without restart (incl. Turkish)
- Dev startup hints when PyQt6 is missing outside the project venv

Download builds from [Releases](https://github.com/Qinaii/qtracker-spaceaces/releases).

## qTracker v1.0.0
First stable release. Windows 10/11, portable EXE.

> ### Tracking
- Reads Uri, EP, Credits, Honor, and Level from the official Space Aces website API
- **Screen OCR, Tesseract, and per-stat calibration are removed**
- No ROI boxes, Scan All, or OCR tips
- Session Start / Pause / Reset Hud; Uri session stays net vs. Start (can go negative after shop spend)
- Rates keep the last known value when a poll briefly fails
>### Dashboard
- Account card: pilot name, level (EXP tooltip), rank / rank points, ship preview
- Live values, session deltas, Uri/h, farming goal with ETA
- Engine controls: Start, Pause, Reset Hud
>### Overlay
- Redesigned HUD panel with per-stat icons
- Hex logo; blue idle, green running, orange paused, red on error
- Panel height shrinks when overlay rows are turned off
- Click logo to collapse; hold to drag; right-click menu
- Overlay tab for toggles and auto-start
>### Analytics
- Charts for Uri, EP, Credits, Honor (daily / weekly / monthly)
- Mob kills from the pilot logbook (with ship icons where available)
- Resources: ores and bonus boxes from the pilot log
>### Leaderboard
- Ranking, Competitive, Events, Clans, and Gates boards on demand
- Faction and rank icons
- Pilot search on Ranking boards
>### Settings
- Connection status: System ready or Error, with Retry
- Optional: Start qTracker when Space Aces launches (background watch, no console window)
>### App
- Single instance guard
- Update check from GitHub Releases
- Privacy page in the app
- Data under `%APPDATA%\qTracker\`
### Requirements
- Space Aces running and logged in

Download builds from [Releases](https://github.com/Qinaii/qtracker-spaceaces/releases).

## v0.0.5-alpha

Pre-release update. Windows 10/11, portable EXE.

### Tracking
- Session Uri is net vs. your value at Start: positive when farming, negative when you spent more than you gained
- Shop purchases no longer break OCR (Uri drops accepted instead of rejected as spikes)
- Uri per hour stays stable after shop spending (no bogus jumps like 500.000/h)
- Rate window resets on Uri spend; last known rate kept until new farming data arrives
- Negative session values shown in dashboard and overlay (e.g. `-50K`)

### Dashboard
- Farming goal progress supports negative session (spent more than gained this session)

### Settings
- Calibration hint text centered on screen (top-left stays free for in-game Uri HUD)

## v0.0.4-alpha

Pre-release update. Windows 10/11, portable EXE.

### Overlay
- Split overlay: logo window plus click-through stats panel
- Logo color: blue idle, green running, orange paused, red on scan or engine error
- Right-click logo: Start, Pause, Dashboard, Check for Updates, Exit
- Session time row (`TIME`), pauses when tracking is paused
- EP, Credits, and Honor show per-hour rates with full numbers (no K/M/B)
- New Overlay tab for toggles, auto-start, and usage hints

### Dashboard
- Buttons renamed: Start, Pause, Reset Hud
- Loading banner on startup before optional overlay auto-start
- Reset Hud and overlay stay clickable after scans

### Tracking
- Stricter OCR validation on all stats, not only Uridium
- Better spike filtering for bad reads
- Credits and Honor rates work with larger per-read gains
- Rates keep last known value when OCR briefly fails
- Old config ROI keys no longer block Start

### Settings
- OCR tips: transparent HUD and map background can hurt reads; try Map Background off or Window Background on in game
- About me and Support me use the same page layout as Dashboard and Overlay

### App
- Single instance: second launch shows a notice
- Update check on startup, About, and overlay menu

## v0.0.3-alpha

First pre-release. Windows 10/11, portable EXE.

### Tracking
- Screen OCR for Uridium, EP, Credits, and Honor
- Per-stat calibration in Settings (box around icon + full number)
- Dashboard session stats with Start, Pause, and Reset Hud
- Uridium farming goal with progress and ETA
- Uridium spike filter for bad OCR reads

### Overlay
- Separate overlay with logo and stats panel
- Click logo to show or hide stats; hold to drag
- Overlay tab for stat toggles and auto-start on launch

### Analytics
- Daily, weekly, and monthly charts after all four core stats are calibrated
- Credits tab fixed (no crash on empty history)

### App
- Qinaii Labs branding and app icon
- Scan progress when reading the game HUD
- Debug snapshots optional in Settings

### Data
- Config and history under `%APPDATA%\qTracker\`
- Imports older `%APPDATA%\UriMeter\` data when present
- Tesseract bundled in the release build

### Known limits (pre-release)
- OCR depends on HUD visibility, resolution, and calibration quality
- EP and Credits need wider calibration boxes than Uridium
- Updates are detected automatically; you download and replace the EXE yourself
