# Changelog

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
