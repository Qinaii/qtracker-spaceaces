# qTracker - Space Aces

HUD stat tracker for Space Aces. Reads on-screen HUD values via OCR. No memory access, no injection, no game files modified.

Made by **[Qinaii Labs](https://qinaii.de)**

[![Releases](https://img.shields.io/github/v/release/Qinaii/qtracker-spaceaces?label=latest)](https://github.com/Qinaii/qtracker-spaceaces/releases)

**Pre-release.** Expect rough edges. Feedback welcome via [Issues](https://github.com/Qinaii/qtracker-spaceaces/issues).

## Download

**[Latest release](https://github.com/Qinaii/qtracker-spaceaces/releases/latest)** · Windows 10/11 · `qtracker_v0.0.5-alpha.exe`

Tesseract OCR is bundled. No separate install needed for the release build.

## Quick start

1. Download and run `qtracker_v0.0.5-alpha.exe` from Releases
2. Open **Settings**
3. Click **Calibrate** on **Uridium** and draw a box around the **icon and full number**
4. Check the OCR readout (`OK. Check against game.`). Adjust the box if needed
5. Calibrate **EP**, **Credits**, and **Honor** for the full dashboard and analytics
6. Click **Scan All** (qTracker minimizes briefly so the game HUD stays visible)
7. Open **Dashboard** and click **Start** to begin session tracking

**Tip:** EP and Credits need wider boxes than Uridium. Include every digit and the thousands dots.

If reads are unstable, check **Settings → OCR tips** (e.g. Map Background off, Window Background on in game).

## Features

| Area | What you get |
|------|----------------|
| **Dashboard** | Live values, net session Uri (farming minus shop spend), Uri/h, farming goal with ETA |
| **Overlay** | Always-on-top logo + stats; click-through rows, drag logo, right-click menu |
| **Analytics** | Daily, weekly, monthly charts (after all four stats are calibrated) |
| **Settings** | Per-stat calibration, Scan All, OCR tips, debug snapshots |
| **Session** | Start sets baseline; Uri session can go negative after shop purchases; Pause pauses tracking; Reset Hud clears session counters |

Tracked stats: **Uridium**, **EP (XP)**, **Credits**, **Honor**.

### Overlay quick guide

- **Click logo:** show or hide stats
- **Hold logo:** drag overlay
- **Right-click logo:** Start, Pause, Dashboard, Check for Updates, Exit
- **Logo color:** blue = idle, green = running, orange = paused, red = scan or error
- Configure visible rows under **Overlay** in the sidebar

## Demo

[![Watch qTracker on YouTube](https://img.youtube.com/vi/Adqg2KXiF1w/hqdefault.jpg)](https://www.youtube.com/watch?v=Adqg2KXiF1w)

Short walkthrough: calibration, dashboard, overlay, and session tracking.

## HUD layout (Space Aces)

| Left column | Right column |
|-------------|--------------|
| XP | Credits |
| Level | Uridium |
| Honor | Jackpot |
| Booty Keys | |

Numbers use German thousands separators (e.g. `1.678.182`).

## Requirements

- Windows 10 or 11 (64-bit)
- Space Aces visible on screen (windowed or borderless recommended)
- HUD stats readable at your resolution and UI scale

## Data and privacy

All config and history stay on your PC:

`%APPDATA%\qTracker\`

- `config.json` - calibration and settings
- `history.jsonl` / `sessions.json` - analytics data
- `debug/` - OCR debug snapshots (only when debug mode is on)

Nothing is uploaded to Qinaii Labs or third parties.

## Troubleshooting

| Problem | Try this |
|---------|----------|
| Wrong or `n/a` readings | Recalibrate with a tighter box around icon + full number |
| EP/Credits cut off | Widen the ROI to the right |
| Unstable OCR | See OCR tips in Settings; adjust game HUD background |
| Spike in Uridium | qTracker filters bad OCR jumps; shop spending is tracked as negative session Uri |
| Analytics empty | Calibrate Uridium, EP, Credits, and Honor first |
| Tesseract error (dev build only) | Release build includes Tesseract; use the GitHub release EXE |

## Support

- **[Report a bug](https://github.com/Qinaii/qtracker-spaceaces/issues/new/choose)** (this repository)
- **[Qinaii Labs](https://qinaii.de)** · **[Discord](https://discord.gg/UDyN94HSGx)**
- Optional: **[Ko-fi](https://ko-fi.com/qinaiilabs)** if you want to support maintenance

## Other Qinaii Labs tools

- **[Qiana](https://qiana.dev)** - Discord bot with web dashboard
- **[qUtils](https://qinaii.de)** - Windows utility suite

## License

Distributed as a free binary release. Source code is not public.

See [CHANGELOG.md](CHANGELOG.md) for version history.
