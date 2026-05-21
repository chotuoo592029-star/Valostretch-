# ValoStretch — Patch Notes

> **Release:** v2.0 — Major Update  
> **Build:** Portable Single-File (`ValoStretch.exe`)  
> **Platform:** Windows 10/11 x64  
> **Framework:** .NET 8.0 (self-contained, no runtime needed)

---

## What is ValoStretch?

ValoStretch is a lightweight Windows tray app that automatically switches your monitor to a stretched resolution when Valorant launches, and restores your native resolution when you close the game. It runs silently in the background using near-zero CPU and RAM.

---

## v2.0 — Full Changelog

### Upgrading from v1?

The new exe handles everything automatically. Just run `ValoStretch.exe` — it will detect your previous installation, show you what it found, and ask whether to import your old settings or start fresh. No manual steps needed.

---

## 1. Smart Upgrade System

### Problem with v1
Users who had v1 installed had to manually delete old files before installing v2. If they forgot, the old version would still auto-start on reboot instead of the new one.

### What's new
The new exe detects previous installations automatically on first launch. It scans for:

- Old config files in `%LocalAppData%\ValoStretch\` or `%LocalAppData%\VALtrueSTREACH\`
- Registered portable copy in `%LocalAppData%\Programs\ValoStretch\`
- Windows auto-start registry entry and Task Scheduler task
- Start Menu shortcut
- Running old ValoStretch process

When found, a **Migration Dialog** appears showing exactly what was detected and giving the user two choices:

**Option A — Import previous settings**
Keeps your monitor ID, native resolution, stretch resolution, and all preferences. Cleans up the old installation, writes a fresh config, and re-registers auto-start pointing to the new exe. The setup wizard is skipped — you're running immediately.

**Option B — Fresh installation**
Wipes everything from the old version and runs the setup wizard from scratch. Use this if you want a clean slate.

**Option C — Cancel**
Exits without touching anything.

### Auto-start fix
After importing, if your old config had "Start with Windows" enabled, the new exe automatically re-registers the auto-start entry pointing to itself. The old exe path is removed. After reboot, the new version starts correctly.

### Schema versioning
Configs now carry a `SchemaVersion` field. Old configs have version `0` (field absent). New configs are stamped with version `2` on every save. This is how the app knows whether to show the migration dialog — it won't appear again once you're on the new version.

---

## 2. UI Redesign — Main Window

### Tools Tile
All three tool buttons have been redesigned with proper icons and visual hierarchy:

- **Custom Resolution Maker** — purple MDL2 icon + label
- **Manage Resolutions** — purple MDL2 icon + label
- **ValoConfig Patcher** — premium styled button with purple tinted background, title, subtitle ("Patch game settings"), and hover glow effect. Stands out clearly from the other tools.

### System Tile
- **Discord button** — replaced the generic icon with the actual Discord logo (SVG path). Blurple branded (`#5865F2`) with hover effect.
- **Uninstall button** — no longer a tiny icon-only square. Now a full-width labeled button: trash icon + "Uninstall ValoStretch" with red danger styling.
- **Layout** — reorganized into two rows: Logs + Discord + Relaunch on top, Uninstall on its own row below for safety.

### Footer Bar
The credits footer has been replaced with a live stats bar showing:
- Valorant sessions count
- Total resolution switches
- Total time spent in stretch mode
- Credits on the right side

---

## 3. Valorant Config Patcher — Rebuilt

The old patcher was using the wrong file path and appending values at the bottom of the file instead of editing them in place.

### Correct path logic
1. Reads `%LocalAppData%\VALORANT\Saved\Config\WindowsClient\RiotLocalMachine.ini` to find the last logged-in user ID (e.g. `409461cc-73d4-5ea3-bbb7-d9675f671057`)
2. Finds the matching folder `{userId}-{region}` (e.g. `-ap`, `-na`, `-eu`) in `%LocalAppData%\VALORANT\Saved\Config\`
3. Opens `WindowsClient\GameUserSettings.ini` inside that folder
4. Edits `ResolutionSizeX`, `ResolutionSizeY`, and `FullscreenMode` **in-place** wherever they appear in the file
5. Only inserts new lines if the keys genuinely don't exist anywhere in the file

### New overlay UI
Clicking "ValoConfig Patcher" now opens a full slide-up overlay panel (same style as the Settings and Logs overlays) with:

- **Detected Account section** — shows user ID, region badge, config file path
- **Refresh button** — re-scans if you switch accounts
- **Open Folder button** — opens Explorer directly to the config file location
- **Resolution Patch section** — side-by-side comparison of current values vs. after patch
- **Editable fields** — you can manually override the ResolutionSizeX and ResolutionSizeY values before patching
- **Read-Only checkbox** — ticked by default. When checked, the file is set to read-only after patching so Valorant can't overwrite it
- **Status feedback** — green success or red error message after patching

---

## 4. Uninstall — Rebuilt

### What it now removes
- App configuration and logs (`%LocalAppData%\ValoStretch\`)
- Custom resolutions injected via NVAPI
- Windows auto-start registry entry and Task Scheduler task
- Start Menu shortcut
- Registered portable copy (`%LocalAppData%\Programs\ValoStretch\`)
- Valorant config patch — restores `GameUserSettings.ini` to native resolution and removes read-only flag
- The running exe itself (scheduled via temp batch script after app exits)

### What it does NOT touch
Nothing outside of ValoStretch's own data. No `%ProgramFiles%` changes, no system files, no other apps.

### Confirmation dialog — redesigned
The uninstall confirmation window has been completely rebuilt. It now shows a clear list of everything that will be removed before you confirm, with icons for each item. You still need to type `uninstall` to confirm — this prevents accidental clicks.

---

## 5. Setup Wizard — Pin to Start

The last page of the setup wizard now includes a **"Pin ValoStretch to Start menu"** checkbox, ticked by default. When checked, a `.lnk` shortcut is created in `%StartMenu%\Programs\` so ValoStretch appears in your Start menu for quick access.

---

## 6. Hotkey — Enabled by Default

The global hotkey (Ctrl+Shift+F6) is now **enabled by default** for all new installations. Previously it was disabled and required manual opt-in.

### Auto-restart on toggle
When you check or uncheck the hotkey enable/disable checkbox, the app automatically saves the setting and starts a **5-second countdown** then restarts itself to apply the change. The status bar shows "Hotkey enabled/disabled — restarting in 5s…" with a live countdown.

---

## 7. Performance & Smoothness

### Hardware rendering restored
The biggest performance fix in this release. The previous version used `AllowsTransparency="True"` on the main window, which forces WPF to render the entire window in software mode (CPU-based compositing). This caused:
- Sluggish window dragging
- Laggy button hover animations
- Higher idle CPU usage

This has been removed. The window now uses hardware GPU rendering, making everything noticeably smoother.

### Timer optimizations
- Runtime polling interval increased from 5s to 8s (resolution and mouse precision checks)
- The polling timer is **paused** when the window is hidden (minimized to tray) — zero CPU overhead from UI polling when you're not looking at the app
- Timer resumes and immediately refreshes when you open the window

### Memory compaction
After startup, the app runs an aggressive GC pass and trims the working set (`SetProcessWorkingSetSize`) to return unused memory to the OS. This runs 3 seconds after launch to let startup settle first.

### Explicit GPU mode
`RenderOptions.ProcessRenderMode = Default` is set at startup to ensure the GPU compositor is used.

---

## 8. System Tray — Redesigned

The right-click tray menu has been completely redesigned. It now shows:

```
● Idle
Mode: Native
Resolution: 2560 x 1440
─────────────────────────
Sessions: 5 | Switches: 12 | 3h 24m
─────────────────────────
🖥  Open ValoStretch
─────────────────────────
◀  Switch to Native
▶  Switch to Stretch
⚡ Automation: ON
─────────────────────────
✕  Exit
```

- **Live status** — current mode and resolution update in real-time
- **Stats line** — session count, total switches, total stretch time
- **Cleaner layout** — proper section separators, purple hover highlight
- **Exit is red** — visually distinct from other actions
- **Darker theme** — matches the main app's `#13131A` background

---

## 9. First-Launch Onboarding

On first launch after setup, a 3-step guided overlay appears explaining the core features:

- **Step 1** — Automatic resolution switching (what the app does)
- **Step 2** — The Ctrl+Shift+F6 hotkey for manual toggling
- **Step 3** — System tray usage (how to access the app when minimized)

Each step has a purple icon, clear description, and "Next →" / "Got it ✓" buttons. A "Skip" option is available. Once dismissed, a marker file prevents it from showing again.

---

## 10. Resolution Stats Tracking

The app now tracks your usage statistics, stored in `%LocalAppData%\ValoStretch\stats.json`:

| Stat | Description |
|------|-------------|
| Valorant Sessions | How many times Valorant was detected launching |
| Total Switches | Total resolution changes made |
| Stretch Activations | Times stretch mode was applied |
| Native Restorations | Times native mode was restored |
| Total Stretch Time | Cumulative time spent in stretch mode |
| Last Switch | Timestamp of the most recent resolution change |

Stats are displayed in:
- The footer bar of the main window
- The system tray right-click menu

Stats persist across app restarts and are never reset unless you uninstall.

---

## 11. Bug Fixes

| Bug | Fix |
|-----|-----|
| ValoConfig patcher appended values at bottom of file instead of editing in place | Rewrote to scan entire file and update keys wherever they appear |
| ValoConfig patcher used wrong folder path (looked in `Valorant\` instead of `VALORANT\`) | Fixed to use correct case-sensitive path and proper user ID detection |
| After migration, old exe would auto-start on reboot instead of new exe | Migration now re-registers auto-start pointing to the new exe path |
| Migration dialog never appeared for users with existing config | Added `SchemaVersion` field — old configs (version 0) now trigger migration |
| Window animations felt laggy | Removed `AllowsTransparency` to restore hardware rendering |
| App polled resolution every 5s even when minimized to tray | Timer now pauses when window is hidden |

---

## File Locations

| File | Path |
|------|------|
| Config | `%LocalAppData%\ValoStretch\config.json` |
| Stats | `%LocalAppData%\ValoStretch\stats.json` |
| Logs | `%LocalAppData%\ValoStretch\logs\app.log` |
| Onboarding marker | `%LocalAppData%\ValoStretch\.onboarding-done` |
| Start Menu shortcut | `%AppData%\Microsoft\Windows\Start Menu\Programs\ValoStretch.lnk` |

---

## Distribution

This release is distributed as a **single portable exe** — no installer, no dependencies, no .NET runtime required.

```
ValoStretch.exe  (~75 MB, self-contained)
```

Place it anywhere. Run it. That's it.

For "Start with Windows" to work reliably on portable builds, use the **"Register on this PC"** option in the setup wizard (Step 5). This copies the exe to `%LocalAppData%\Programs\ValoStretch\` and registers that path for auto-start, so it works even if you move or rename the original file.

---

## Known Limitations

- Custom resolution injection (NVAPI) requires an NVIDIA GPU
- "Start with Windows" via Task Scheduler requires the app to be registered on the PC (see above)
- Valorant config patching requires Valorant to have been launched at least once (so the config file exists)
- The app must be running for automatic resolution switching to work — it does not install a driver or kernel component

---

*ValoStretch — Crafted with passion by Vibe © 2026*
