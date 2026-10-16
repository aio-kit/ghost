# GHOST — Guardian Hub Of Stats & Tools

**One free app for everything around Destiny 2**: a LiveSplit-compatible speedrun timer, OBS overlays and a
streamer mode, the Oracle counter, an in-game weapon overlay, and DIM and the community sites, all signed in.

Made with ❤ by **skipalot** · [guns.lol/kirito8101](https://guns.lol/kirito8101) ·
[Discord: help, feedback and ideas](https://discord.gg/P5CfpAzByX)

> GHOST is a fan-made tool. It isn't affiliated with or endorsed by Bungie. See [Safety & privacy](#safety--privacy).

## Install

**Most people:** download **`ghost-installer.exe`** and run it. It installs GHOST for your Windows account (no
admin needed) with a Start menu shortcut.

When GHOST opens, go to **Accounts → Sign in…** once, and DIM and every site tab use that login.

**Running from source:** install Python 3.10+ (tick *Add Python to PATH*) and double-click **`start.bat`**.
It installs what it needs on the first run.

**Updating:** run the new `ghost-installer.exe`, or drop it onto the GHOST window, or use
**Settings → About → Install from a file…**. GHOST closes, updates itself and opens again. Your settings live in
`%APPDATA%\GHOST`, so they carry over. When a release page is set up, GHOST also offers **Install GHOST x.y.z**
in the sidebar as soon as a new version is out.

## Coming from LiveSplit?

1. Open **Speedrun Timer** and press **Import from LiveSplit**. GHOST looks for LiveSplit in the usual places
   (Downloads, Desktop, Documents, Program Files…). If it doesn't find it, press **Browse…** and pick the folder
   with `LiveSplit.exe` in it.
2. Tick the splits files you want (your recent ones are ticked already), and choose whether to bring over your
   hotkeys, your layout and the comparison you used last.
3. Press **Import**. That's it: your PB, golds and attempt history are all there, and your keys work the same.

Your `.lss` files stay where they are and stay up to date, so LiveSplit still has everything if you go back.
The first time GHOST saves into a file it keeps a copy of the original next to it, named `… (before GHOST).lss`.
Close LiveSplit while you run in GHOST so the two don't save over each other.

## What's inside

| Page | What it does |
|---|---|
| **Home** | Live status for every tool, quick actions and a hotkey cheat sheet. |
| **Speedrun Timer** | A LiveSplit-style timer built for runners, and built so LiveSplit runners can switch without losing anything. **Import from LiveSplit** finds your LiveSplit folder and brings over every splits file (PB, gold splits, full attempt history, custom comparisons, game times, icons and auto splitter settings), your hotkeys and how your layout looks. Imported `.lss` files stay **linked**: GHOST saves each attempt back into them and loads changes LiveSplit makes, so you can go back and forth with the same file. Compare against Personal Best, Best / Average / Median / Worst Segments, Latest Run or your own comparisons, and switch with hotkeys. The splits editor works like LiveSplit's: type split, segment and best times straight into the table. Pick the *LiveSplit classic*, *GHOST* or *Minimal* look, with live deltas, gold segments, Sum of Best, Best Possible Time and Previous Segment, plus an always-on-top overlay you can lock click-through. The overlay can show the full splits layout or just a **big clock** (like the stream's Big clock), with the current split and delta underneath if you want them. Also: templates for every raid, dungeon, exotic mission and campaign, practice mode, a start countdown, double-tap prevention, undo all pauses, two-press reset, a run that survives restarting GHOST, and one-click results for Discord and speedrun.com. |
| **Stream** | Put GHOST on your stream. The **overlay link builder** has four sources: the timer and splits, a big clock, the Oracle counter and a stats bar. Pick one, adjust its look, size and background with simple controls, and see a **live preview**. Then copy the link and the exact OBS size to use. **OBS text files** feed Text sources. **Streamer mode** hides your account names and can hide the GHOST window from OBS and Discord capture completely. |
| **Oracle Counter** | The original tool. Log numbers with the numpad, number row or custom keys, then send them as typed keys or a paste. Adds undo, a history of recent sends, and an overlay with opacity, font size and snap positions. |
| **Weapon Overlay** | Inspect a weapon in Destiny (or open/drop a screenshot) and GHOST finds the inspect screen by itself (no area to set up), reads the name and the perk icons, rates the roll for PvE, PvP, General or Custom (Roll Quality, God Roll Match, Confidence, Completeness, S–D perk tiers), shows the best roll your copy can run and other builds, and saves every copy to your roll book. A floating panel in the top-right corner opens only on the weapon's inspect screen (the perk grid and the "WEAPON PERKS" heading must be on screen, not just the name) and closes when you leave (Ctrl + wheel resizes it). Screenshots can be opened, dropped, pasted (Ctrl+V) or picked up from a watched screenshots folder. "What GHOST read" shows every read with its confidence and lets you fix it. |
| **DIM · Godroll.tv · D2TTK · D2ArmorPicker** | Full browser tabs with real logins, cookies and sessions. Each one remembers the last page you were on and its zoom. You can add your own sites in Settings → Sites. |
| **Accounts** | Several Bungie logins signed in at once. Each has its own isolated profile. You can switch per tab or globally. |
| **Settings** | 8 accent themes (plus a custom colour), drag-to-reorder or hide tabs, every global hotkey, tray and startup options, sites, and export/import/reset. |

## Streaming with GHOST

1. Open the **Stream** page and click **Start** to turn on the overlay server.
2. Pick a source on the left (timer, clock, Oracle counter or stats bar). Change its look and size, and check
   the live preview.
3. Click **Copy link**. In OBS (or Streamlabs): **Sources → + → Browser**, paste the link, and set the width
   and height GHOST shows under the link. The background is already transparent.
4. Before you go live, turn on **Streamer mode** (Ctrl+Alt+H). It hides your account names and
   hides the GHOST window from capture.

The browser-source server only listens on `127.0.0.1`, so nothing outside your PC can reach it.

## Hotkeys

Click a key and press the new one. Mouse 4/5 and middle click work too. Clashes are flagged next to the key, and a dot lights up when a hotkey fires, so you can test keys in-game.

| Action | Key |
|---|---|
| Show / hide GHOST | Ctrl+Alt+G |
| Oracle counter overlay | Ctrl+Alt+C |
| Weapon overlay | Ctrl+Alt+W |
| Scan weapon (OCR) | Ctrl+Alt+S |
| OCR auto-scan on/off | Ctrl+Alt+A |
| Pause / resume every GHOST hotkey | Ctrl+Alt+P |
| Timer: start / split | Home |
| Timer: pause / resume | End |
| Timer: undo / skip split | Page Up / Page Down |
| Timer: reset (saves golds & PB) | Ctrl+Delete |
| Timer: previous / next comparison | not set (Num 4 / Num 6 with LiveSplit's keys) |
| Timer overlay | Ctrl+Alt+T |
| Streamer mode on / off | Ctrl+Alt+H |

Inside the app:
- **Ctrl+K** opens the command palette: type to jump to any page or run any action (toggle overlays, start the timer…).
- **Ctrl+1…9** switches tabs and **Ctrl+Tab** cycles through them.
- **Ctrl+F** finds text inside web tabs.

## Tips and troubleshooting

- **Overlays need Destiny in Windowed or Borderless** mode. Exclusive fullscreen draws over them.
- **Weapon data** comes from Bungie's public manifest. Click *Download / update* once (about 100 MB). It's cached
  and quietly checked for updates.
- **TTK numbers are approximate** PvP estimates. You can edit them with *Edit TTK table*, and the D2TTK tab has
  the exact figures.
- **OCR** uses Windows' built-in text recognition. Nothing to install: GHOST uses it directly when the optional
  `winrt` packages are there, and through PowerShell otherwise. Tesseract also works
  (`pip install pytesseract pillow`, plus the Tesseract program).
- If some sign-in pages (for example Google) refuse to load in embedded browsers, sign in with Steam, Xbox,
  PlayStation, Epic or Twitch instead.
- Closing the window keeps GHOST running in the tray so hotkeys keep working. Quit from the tray menu.
- Typing in chat? Press **Ctrl+Alt+P** to pause every GHOST hotkey, and again to resume. You can also use the tray menu.
- Something not working? Open **Settings → Data → System check**. It shows what's installed and what's missing,
  and **Copy report** gives you a summary to paste when asking for help.
- After an update GHOST shows what's new once. **Settings → About → What's new** shows it again.
- Settings, logins, splits and logs live in `%APPDATA%\GHOST` (*Settings → Data* opens it).

## Safety & privacy

- **Not affiliated with Bungie.** Destiny is a trademark of Bungie, Inc.
- **No macros, no automation.** GHOST doesn't run game macros or scripts and doesn't play or click for you.
  The only thing it ever types is the Oracle counter's numbers into chat, when you press its send key. Everything
  else (timer, overlays, OBS sources, DIM and the other sites) only reads or displays information.
- **Your data stays on your PC.** Settings, Bungie logins (in GHOST's own browser profiles), splits and logs are
  stored in `%APPDATA%\GHOST`. GHOST has no account, no analytics and no telemetry.
- **Network use:**
  - The Bungie / DIM / community sites you open.
  - Bungie's public manifest, for weapon data.
  - An optional update check against this project's GitHub Releases.
- The **OBS server** binds to `127.0.0.1` only and serves read-only pages.

## For developers

```
start.bat               run GHOST from source (installs requirements on first run)
build.bat               build dist\ghost-installer.exe        (build.bat fast = quick unprotected test build)
tools\build.py          what build.bat runs (the installer script is in it too)
```

### Releasing a new version

1. Set the new version in `ghost/__init__.py` (`APP_VERSION = "4.8.0"`).
2. Add a `## 4.8.0: title` section at the top of `CHANGELOG.md` with what's new. GHOST shows it in "What's new".
3. Double-click **`build.bat`**. It builds and checks GHOST, makes **`dist\ghost-installer.exe`**, and saves the
   notes to `dist\release-notes.txt`. If that version is already on the release page, it offers to bump it for you
   (every update needs a new version, or GHOST won't offer it to anyone).
4. On GitHub (github.com/aio-kit/ghost/releases/new): tag `4.8.0`, attach `ghost-installer.exe` (keep that name),
   paste the notes, and publish it as a normal release. Everyone's GHOST then offers the update by itself.

### Tests

```
python tests/run_tests.py     matching, scoring, roll book and perk-reading tests (no Qt or internet needed)
```

### Weapon scoring

- `%APPDATA%\GHOST\scoring.json` (created on first run): tier values, the community-share cutoffs for S–D, column
  weights, label thresholds, the confidence / completeness needed before a roll is rated, synergy rules
  (`{"perks": ["A", "B"], "points": 5, "profile": "pve", "note": "why"}`) and your own perk ratings
  (`"custom_ratings": {"*": {"Perk": "S"}, "Weapon Name": {"Perk": "A"}}`; they override every profile, and Custom uses community PvE tiers for perks you haven't rated).
  Click **Reload them** on the page after editing. A broken file falls back to the defaults (it isn't overwritten).
- `%APPDATA%\GHOST\aliases.json`: OCR misreadings to fix, `"what OCR reads": "Real Name"`.
- Game data (names, hashes, perk pools, icons) comes from Bungie's manifest and is cached for offline use; tiers and
  recommended rolls come from the community wish list and are opinions. GHOST never makes up a perk or a score:
  unsure reads are shown as "to check" / Unverified.

Every build writes everything it does to `build\build-log.txt`; if a build fails, that file says why.

**What the build does:** installs anything missing, compiles GHOST to machine code with Nuitka (so the code can't
simply be unpacked; the first build takes 10-30 minutes, later ones are much faster), removes files GHOST never
uses, starts the new GHOST.exe once in a self-check mode to make sure nothing is missing, and packs the installer
with Inno Setup (installed automatically the first time). If the protected build fails, it explains the usual fix
and asks before making an unprotected build instead.

**The release page:** `APP_REPO` in `ghost/__init__.py` (`aio-kit/ghost`) is where GHOST looks for updates.

**Sharing on Discord:** without Nitro, attachments are limited to 10 MB and the installer is bigger, so post a
link to it instead.

### Project layout

```
main.py                 entry point (logging, crash handler, single instance)
ghost/config.py      settings: atomic saves, corruption recovery, Oracle Counter migration
ghost/theme.py       the 8 themes and one app-wide stylesheet
ghost/hotkeys.py     one global keyboard hook shared by every feature
ghost/winput.py      Win32 SendInput (scancodes), dark title bar, startup entry
ghost/accounts.py    per-account isolated browser profiles
ghost/weapons.py     manifest download → compact weapon DB, search, OCR matching, TTK
ghost/ocr.py         screen capture + Windows OCR / Tesseract (unchanged pictures aren't read again)
ghost/matching.py    OCR text → real names: normalising, OCR fixes, aliases, careful fuzzy matching
ghost/perkscan.py    finds the perk icons on the inspect screen and recognises them (verified / unverified)
ghost/perkicons.py   downloads and caches Bungie's perk icons
ghost/scoring.py     the roll scoring engine (no Qt): tiers, combinations, synergy, labels, explanations
ghost/godroll.py     community recommended rolls (DIM wish list), roles
ghost/rollbook.py    your saved copies of each weapon
ghost/weaponcard.py  the weapon panel shown in the overlay and on the page
tests/               python tests/run_tests.py
ghost/overlays.py    counter overlay, timer overlay, weapon panel, region picker
ghost/speedrun.py    speedrun engine: splits, PB, golds, comparisons, LiveSplit .lss / settings / layouts
ghost/streamkit.py   OBS browser-source server (127.0.0.1) and OBS text files
ghost/updates.py     GitHub Releases update check
ghost/pages/*.py     one file per page
```

## License

Copyright (c) 2026 skipalot. All rights reserved. GHOST is free to download and use, but it isn't open source:
copying, modifying, re-uploading or selling it needs permission. See [LICENSE](LICENSE). Third-party parts keep
their own licences, for example Qt for Python (LGPL).
