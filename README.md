<div align="center">

<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/main-window.png" alt="ValoStretch Main Window" width="800"/>

# ValoStretch

**Automatic stretched resolution switching for Valorant â€” runs silently in your system tray**

[![Release](https://img.shields.io/github/v/release/chotuoo592029-star/Valostretch-?style=for-the-badge&color=A78BFA&labelColor=0C0C0F)](https://github.com/chotuoo592029-star/Valostretch-/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-blue?style=for-the-badge&color=5865F2&labelColor=0C0C0F)](https://github.com/chotuoo592029-star/Valostretch-/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/chotuoo592029-star/Valostretch-/total?style=for-the-badge&color=34D399&labelColor=0C0C0F)](https://github.com/chotuoo592029-star/Valostretch-/releases/latest)
[![Discord](https://img.shields.io/badge/Discord-Join%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white&labelColor=0C0C0F)](https://discord.gg/uA3sMpFAuG)

[**â¬‡ Download Latest**](https://github.com/chotuoo592029-star/Valostretch-/releases/latest) Â· [**ðŸ“‹ Changelog**](CHANGELOG.md) Â· [**ðŸ› Report Bug**](https://github.com/chotuoo592029-star/Valostretch-/issues/new?template=bug_report.md) Â· [**ðŸ’¡ Request Feature**](https://github.com/chotuoo592029-star/Valostretch-/issues/new?template=feature_request.md)

</div>

---

## What is ValoStretch?

ValoStretch is a free Windows tool that **automatically switches your monitor to a stretched resolution when Valorant launches**, and restores your native resolution when you close the game.

No more manually changing display settings before every game. No more forgetting to switch back. It just works â€” silently, in the background, using near-zero CPU and RAM.

> **Portable** â€” single `.exe` file, no installer, no admin rights needed for basic use.  
> **Free** â€” always has been, always will be.

---

## Features

| Feature | Description |
|---------|-------------|
| ðŸ”„ **Auto-Switch** | Detects Valorant launch/close and switches resolution automatically |
| ðŸ–¥ **Full Stretch Mode** | Briefly disables monitor to force true stretched resolution (recommended for laptops) |
| ðŸ“ **Resolution Only Mode** | Changes resolution without monitor toggle â€” no flicker (ideal for desktops) |
| âŒ¨ **Global Hotkey** | Press `Ctrl+Shift+F6` anytime to manually toggle stretch/native |
| ðŸŽ® **ValoConfig Patcher** | Writes stretch resolution directly into Valorant's `GameUserSettings.ini` |
| ðŸ“Š **Custom Resolution Maker** | Create and inject custom resolutions via NVAPI (NVIDIA GPUs) |
| ðŸ“ˆ **Usage Stats** | Tracks sessions, switches, and total stretch time |
| ðŸ”” **System Tray** | Lives in your tray â€” right-click for quick controls |
| ðŸš€ **Start with Windows** | Auto-starts minimized so it's always ready |
| â™» **Smart Upgrade** | Detects previous versions and handles migration automatically |

---

## Screenshots

<details>
<summary><b>Main Window</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/main-window.png" alt="Main Window" width="800"/>
</details>

<details>
<summary><b>Setup Wizard â€” Step 1: Monitor Selection</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/setup-wizard-step1.png" alt="Setup Wizard Step 1" width="700"/>
</details>

<details>
<summary><b>Setup Wizard â€” Step 2: Native Resolution</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/setup-wizard-step2.png" alt="Setup Wizard Step 2" width="700"/>
</details>

<details>
<summary><b>Setup Wizard â€” Step 3: Stretch Resolution</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/setup-wizard-step3.png" alt="Setup Wizard Step 3" width="700"/>
</details>

<details>
<summary><b>Setup Wizard â€” Step 4: Stretch Mode</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/setup-wizard-step4.png" alt="Setup Wizard Step 4" width="700"/>
</details>

<details>
<summary><b>Setup Wizard â€” Step 5: Startup & Registration</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/setup-wizard-step5.png" alt="Setup Wizard Step 5" width="700"/>
</details>

<details>
<summary><b>Automation Settings</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/automation-settings.png" alt="Automation Settings" width="700"/>
</details>

<details>
<summary><b>Valorant Config Patcher</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/valoconfig-patcher.png" alt="ValoConfig Patcher" width="800"/>
</details>

<details>
<summary><b>Custom Resolution Maker</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/custom-resolution-maker.png" alt="Custom Resolution Maker" width="600"/>
</details>

<details>
<summary><b>Update Detection (upgrading from v1)</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/update-detected.png" alt="Update Detected" width="600"/>
</details>

---

## Download & Install

### Fresh Install

1. Go to [**Releases**](https://github.com/chotuoo592029-star/Valostretch-/releases/latest)
2. Download `ValoStretch.exe`
3. Run it â€” the setup wizard opens automatically
4. Follow the 5 steps (takes about 2 minutes)
5. Done â€” ValoStretch is running in your tray

> No installation required. Place the exe anywhere you want.

### Upgrading from v1

Just run the new `ValoStretch.exe`. It will automatically detect your previous installation and ask whether to:
- **Import your settings** â€” keeps your monitor ID, resolutions, and preferences. No re-setup needed.
- **Fresh install** â€” wipes old data and runs the setup wizard from scratch.

Your auto-start entry is automatically updated to point to the new exe.

---

## Setup Guide

### Step 1 â€” Monitor Selection
ValoStretch needs to know which monitor to control. Click **Detect Monitors** and select your display from the dropdown. The one marked `[ACTIVE]` is usually correct.

### Step 2 â€” Native Resolution
Set your normal desktop resolution (the one you use outside Valorant). Example: `2560 Ã— 1440` for a 1440p display.

### Step 3 â€” Stretch Resolution
Set the resolution you want in Valorant. Example: `2100 Ã— 1440` gives a ~4:3 stretched look on a 1440p display.

### Step 4 â€” Stretch Mode
Choose how the switch happens:

| Mode | Best For | How It Works |
|------|----------|-------------|
| **Full Stretch Mode** | Laptops / built-in screens | Briefly disables monitor to force true stretch |
| **Resolution Only** | Desktop PCs / external monitors | Changes resolution without monitor toggle |

### Step 5 â€” Startup Options
- **Register on this PC** â€” copies the exe to `%LocalAppData%\Programs\ValoStretch\` so it persists if you move the original file. Required for reliable auto-start.
- **Start with Windows** â€” launches ValoStretch minimized on every boot.
- **Pin to Start menu** â€” creates a Start menu shortcut.

---

## How It Works

```
Valorant launches
      â†“
ValoStretch detects the process (via WMI events)
      â†“
Switches display to stretch resolution
      â†“
You play Valorant in stretched
      â†“
Valorant closes
      â†“
ValoStretch restores native resolution automatically
```

The app uses **WMI process events** (zero polling overhead) to detect Valorant. When WMI is unavailable, it falls back to 3-second polling. A watchdog checks every 8 seconds that the resolution hasn't drifted (Valorant's anti-cheat can reset it).

---

## ValoConfig Patcher

The ValoConfig Patcher writes your stretch resolution directly into Valorant's `GameUserSettings.ini` file so the game itself requests the correct resolution on launch.

**How to use:**
1. Open ValoStretch â†’ Tools â†’ **ValoConfig Patcher**
2. Your Valorant account is detected automatically
3. Review the current vs. after-patch values
4. Click **Apply Patch**
5. The file is saved as read-only to prevent Valorant from overwriting it

> Requires Valorant to have been launched at least once so the config file exists.

---

## Custom Resolution Maker

For NVIDIA GPU users â€” create custom resolutions that aren't in Windows' default list.

1. Open ValoStretch â†’ Tools â†’ **Custom Resolution Maker**
2. Select your display adapter
3. Enter width, height, and refresh rate
4. Click **Test Resolution** â€” a 12-second preview lets you confirm before saving
5. The resolution is injected via NVAPI and added to your available resolutions list

---

## Hotkey

The global hotkey `Ctrl+Shift+F6` toggles between native and stretched resolution at any time â€” even when ValoStretch is minimized to tray.

To change it: open ValoStretch â†’ **Quick Switch** tile â†’ click **Change** â†’ press your desired key combination.

---

## System Requirements

| Requirement | Details |
|-------------|---------|
| **OS** | Windows 10 or Windows 11 (64-bit) |
| **Runtime** | None â€” fully self-contained |
| **GPU** | Any (Custom Resolution Maker requires NVIDIA) |
| **Valorant** | Must be installed and launched at least once |
| **Disk** | ~75 MB (single exe) |
| **RAM** | ~30â€“50 MB at idle |
| **CPU** | Negligible â€” event-driven, not polling-based |

---

## Troubleshooting

**Resolution doesn't switch when Valorant launches**
- Make sure automation is enabled (toggle in the main window)
- Check that the correct monitor is selected in Automation Settings
- Try switching to Resolution Only mode if Full Stretch Mode causes issues

**App doesn't start with Windows after moving the exe**
- Open ValoStretch â†’ Automation Settings â†’ Save Settings
- Or run the setup wizard again and enable "Register on this PC"

**ValoConfig Patcher says "config not found"**
- Launch Valorant and play at least one game, then try again
- Make sure you're logged into your Riot account

**Custom resolutions not showing in Valorant**
- NVIDIA GPU required for NVAPI injection
- Try restarting your PC after creating a custom resolution
- Vanguard may require a reboot after NVAPI changes

**Old version keeps starting after upgrade**
- Run the new `ValoStretch.exe` â€” it will detect the old version and fix the auto-start entry automatically

---

## Privacy

ValoStretch does not:
- Connect to the internet
- Collect any data
- Send telemetry
- Require an account

All data (config, logs, stats) is stored locally in `%LocalAppData%\ValoStretch\`.

---

## Uninstalling

Open ValoStretch â†’ System tile â†’ **Uninstall ValoStretch**

Type `uninstall` to confirm. The app will:
- Remove all config, logs, and stats
- Remove the auto-start entry
- Remove the Start menu shortcut
- Restore Valorant's config to native resolution
- Delete itself

---

## Changelog

See [**CHANGELOG.md**](CHANGELOG.md) for the full patch notes.

**Latest â€” v2.0**
- Smart upgrade system with migration dialog
- Rebuilt ValoConfig Patcher with correct path detection
- Hardware rendering restored (major smoothness improvement)
- System tray redesign with live stats
- First-launch onboarding overlay
- Resolution stats tracking
- Hotkey enabled by default with auto-restart on toggle
- Uninstall now fully cleans everything including Valorant config patch

---

## Support & Community

- **Bug reports** â†’ [GitHub Issues](https://github.com/chotuoo592029-star/Valostretch-/issues/new?template=bug_report.md)
- **Feature requests** â†’ [GitHub Issues](https://github.com/chotuoo592029-star/Valostretch-/issues/new?template=feature_request.md)
- **Discord** â†’ [Join the server](https://discord.gg/uA3sMpFAuG)

---

## Disclaimer

ValoStretch is an independent tool not affiliated with Riot Games. It operates at the Windows display API level and does not modify game files or memory. Use at your own discretion.

---

<div align="center">

Made with ðŸ’œ by **Vibe** Â· Â© 2026

</div>

