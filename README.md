# qTracker - Space Aces

HUD and session tracker for Space Aces. Shows your pilot stats from the **official Space Aces website** while you play. No screen OCR, no memory access, no injection, no game files modified.

Made by **[Qinaii Labs](https://qinaii.de)**

Want to be up to date on any changes? join **[[ΛoR] Λge of Revenge]([https://qinaii.de](https://discord.gg/9wD5Tgxpr9))**

[![Releases](https://img.shields.io/github/v/release/Qinaii/qtracker-spaceaces?label=latest)](https://github.com/Qinaii/qtracker-spaceaces/releases)

## Download

**[Latest release](https://github.com/Qinaii/qtracker-spaceaces/releases/latest)** · Windows 10/11 · `qtracker_v2.0.2.exe`

Space Aces must be installed and logged in on this PC. Each release includes a `qtracker_vX.Y.Z.sha256` checksum file. Compare it to the file you downloaded before running.

## Quick start

1. Download and run `qtracker_v2.0.2.exe` from Releases
2. Start **Space Aces** and log in
3. Open **Dashboard** and click **Start** to begin session tracking
4. Optional: open **Overlay** and click **Activate Overlay** for an always-on-top HUD
5. Optional: in **Settings**, enable **Start qTracker when Space Aces launches**
6. Optional: open **Notifications** for Pirate Map / CBS desktop toasts (click-through)

If status shows an error, click **Retry** after Space Aces is logged in.

## Features

| Area | What you get |
|------|----------------|
| **Dashboard** | Account (pilot, level, rank, ship), live Uri / EP / Credits / Honor, session deltas, Uri/h, Start / Pause / Reset Hud |
| **Overlay** | Always-on-top logo + stats panel; click-through rows; drag logo; right-click menu; farming goal with ETA; height shrinks when rows are off |
| **Analytics** | Mob kills, resources (ores / bonus boxes), Uri spend from your pilot log |
| **Dailys Best** | Daily top gains by date (leaderboard snapshot) |
| **Leaderboard** | Ranking, Events, Clans, Gates; faction and rank icons; Pilot Lookup by leaderboard alias |
| **Faction Change** | Recent faction switches from the world feed |
| **Pirate Map** | Open / energy / timer when the world feed has data |
| **Clan Battle Station** | Live Free / occupied CBS slots by map, clan tag, construction timer |
| **Global Chat** | Recent public chat from the world feed |
| **Notifications** | Optional desktop toasts (click-through) for Pirate Map and CBS; sound + volume; per-category and per-event toggles |
| **Settings** | Connection status, Retry, diagnostics log, optional auto-start with Space Aces |
| **About / Privacy** | Updates check, Qinaii Labs links, privacy policy and terms |

Tracked stats: **Uridium**, **EP (XP)**, **Credits**, **Honor**, **Level**.

### Overlay quick guide

- **Click logo:** show or hide stats
- **Hold logo:** drag overlay
- **Right-click logo:** Start, Pause, Reset Hud, Dashboard, Check for Updates, Exit
- **Logo color:** blue = idle, green = running, orange = paused, red = connection error
- Configure visible rows and the farming goal under **Overlay** in the sidebar

### Notifications quick guide

- Master enable under **General**, plus category switches for **Pirate Map** and **CBS**
- Pirate Map: open / closing soon / closed
- CBS: build (under construction), spawn finished, destroyed
- Toasts appear top-center and are click-through (same idea as the HUD stats panel)
- Preview sound and send a test toast from the Notifications page

## Demo

https://youtu.be/dFN2aiPsmNI

## Requirements

- Windows 10 or 11 (64-bit)
- Space Aces installed and logged in (same website session as the game client)
- Internet access for Space Aces services (leaderboards and world feed may use the Qinaii cache)

## Data and privacy

All config and history stay on your PC:

`%APPDATA%\qTracker\`

qTracker uses your local Space Aces login session to show your own stats. Leaderboard lists and world-feed pages (Dailys Best, Faction Change, Pirate Map, CBS, Global Chat) may go through the Qinaii cache so the game API is not overloaded. Nothing is sent to Qinaii Labs for analytics, advertising, or resale.

See **Privacy** in the app for policy and terms.

## Antivirus / Windows SmartScreen

Release builds may be **unsigned**. Windows Defender, SmartScreen, or a few VirusTotal engines may warn on a fresh download. That is common for new desktop apps and does **not** mean the file is a trojan.

What qTracker does:

- Uses the same Space Aces login session already on this PC to call official Space Aces services
- Stores settings and history only under `%APPDATA%\qTracker\`
- Optionally caches public leaderboard / world-feed data via Qinaii (`api.qinaii.de`)

What qTracker does **not** do:

- No game memory reading
- No injection into Space Aces
- No game file changes
- No upload of your account data to Qinaii Labs for analytics or ads

## Troubleshooting

| Problem | Try this |
|---------|----------|
| Connection error | Start Space Aces, log in, then **Retry** in Settings |
| Stats stay `n/a` | Wait a few seconds after login |
| Overlay missing | **Overlay** tab → **Activate Overlay** |
| Analytics empty | Play with tracking running; data fills from the pilot log |
| World pages empty | Check internet; those tabs use the Qinaii world feed |
| No notification toast | Enable notifications + the matching Pirate Map / CBS event; volume not muted |
| Second window warning | Only one qTracker instance is allowed |

## Support

- **[Report a bug](https://github.com/Qinaii/qtracker-spaceaces/issues/new/choose)**
- **[Antivirus false positive](https://github.com/Qinaii/qtracker-spaceaces/issues/new?template=antivirus_false_positive.yml)**
- **[Qinaii Labs](https://qinaii.de)** · **[Discord](https://discord.gg/UDyN94HSGx)**
- Optional: **[Ko-fi](https://ko-fi.com/qinaiilabs)**

## Other Qinaii Labs tools

- **[Qiana](https://qiana.dev)** - Discord bot with web dashboard
- **[qUtils](https://qinaii.de)** - Windows utility suite

## License

Distributed as a free binary release. Source code is not public.
