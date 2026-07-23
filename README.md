# qTracker - Space Aces

HUD and session tracker for Space Aces. Reads your pilot stats from the **official Space Aces** while you play. No screen OCR, no memory access, no injection, no game files modified.

Made by **[Qinaii Labs](https://qinaii.de)**

[![Releases](https://img.shields.io/github/v/release/Qinaii/qtracker-spaceaces?label=latest)](https://github.com/Qinaii/qtracker-spaceaces/releases)

## Download

**[Latest release](https://github.com/Qinaii/qtracker-spaceaces/releases/latest)** · Windows 10/11 · `qtracker_v1.0.0.exe`

No Tesseract or extra OCR install. Space Aces must be running and logged in so qTracker can read your session token.

## Quick start

1. Download and run `qtracker_v1.0.0.exe` from Releases
2. Start **Space Aces** and log in
3. Open **Dashboard** and click **Start** to begin session tracking
4. Optional: open **Overlay** and click **Activate Overlay** for an always-on-top HUD
5. Optional: in **Settings**, enable **Start qTracker when Space Aces launches**

If status shows **Error**, click **Retry** after Space Aces is logged in.

## Features

| Area | What you get |
|------|----------------|
| **Dashboard** | Account (pilot, level, rank, ship), live Uri/EP/Credits/Honor, session deltas, Uri/h, farming goal with ETA |
| **Overlay** | Always-on-top logo + stats panel with icons; click-through rows; drag logo; right-click menu; height shrinks when rows are off |
| **Analytics** | Daily / weekly / monthly charts for Uri, EP, Credits, Honor; Mob kills; Resources (ores and bonus boxes from your pilot log) |
| **Leaderboard** | Ranking, Competitive, Events, Clans, Gates; faction and rank icons; pilot search on Ranking |
| **Settings** | Connection status, Retry, optional auto-start with Space Aces |
| **Session** | Start sets baseline; Uri session can go negative after shop spend; Pause pauses tracking; Reset Hud clears session counters |

Tracked stats: **Uridium**, **EP (XP)**, **Credits**, **Honor**, **Level**.

### Overlay quick guide

- **Click logo:** show or hide stats
- **Hold logo:** drag overlay
- **Right-click logo:** Start, Pause, Dashboard, Check for Updates, Exit
- **Logo color:** blue = idle, green = running, orange = paused, red = connection error
- Configure visible rows under **Overlay** in the sidebar

## Demo

https://youtu.be/dFN2aiPsmNI

## Requirements

- Windows 10 or 11 (64-bit)
- Space Aces installed and logged in (token is read from local Space Aces storage)

## Data and privacy

All config and history stay on your PC:

`%APPDATA%\qTracker\`
See **Privacy** in the app for policy and terms.

## Troubleshooting

| Problem | Try this |
|---------|----------|
| Status **Error** | Start Space Aces, log in, then **Retry** in Settings |
| Stats stay `n/a` | Wait a few seconds after login; confirm you are on a valid server session |
| Overlay missing | **Overlay** tab → **Activate Overlay**; check Windows focus / multi-monitor |
| Analytics empty | Play with tracking running; charts fill from history and pilot log sync |
| Second window warning | Only one qTracker instance is allowed |

## Support

- **[Report a bug](https://github.com/Qinaii/qtracker-spaceaces/issues/new/choose)** (this repository)
- **[Qinaii Labs](https://qinaii.de)** · **[Discord](https://discord.gg/UDyN94HSGx)**
- Optional: **[Ko-fi](https://ko-fi.com/qinaiilabs)** if you want to support maintenance

## Other Qinaii Labs tools

- **[Qiana](https://qiana.dev)** - Discord bot with web dashboard
- **[qUtils](https://qinaii.de)** - Windows utility suite

## License

Distributed as a free binary release. Source code is not public.
