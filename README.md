<div align="center">

<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/main-window.png" alt="ValoStretch Main Window" width="800"/>

# ValoStretch

**Automatic stretched resolution switching for Valorant, selected games, and selected apps**

[![Release](https://img.shields.io/github/v/release/chotuoo592029-star/Valostretch-?style=for-the-badge&color=A78BFA&labelColor=0C0C0F)](https://github.com/chotuoo592029-star/Valostretch-/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-blue?style=for-the-badge&color=5865F2&labelColor=0C0C0F)](https://github.com/chotuoo592029-star/Valostretch-/releases/latest)
[![Downloads](https://img.shields.io/badge/Downloads-648-green?style=for-the-badge&color=34D399&labelColor=0C0C0F)](https://github.com/chotuoo592029-star/Valostretch-/releases/latest)
[![Discord](https://img.shields.io/badge/Discord-Join%20Server-5865F2?style=for-the-badge&logo=discord&logoColor=white&labelColor=0C0C0F)](https://discord.gg/uA3sMpFAuG)

[**Download Latest**](https://github.com/chotuoo592029-star/Valostretch-/releases/latest) &nbsp;&middot;&nbsp; [**Changelog**](CHANGELOG.md) &nbsp;&middot;&nbsp; [**Report Bug**](https://github.com/chotuoo592029-star/Valostretch-/issues/new?template=bug_report.md) &nbsp;&middot;&nbsp; [**Request Feature**](https://github.com/chotuoo592029-star/Valostretch-/issues/new?template=feature_request.md)

</div>

---

## What is ValoStretch?

ValoStretch is a lightweight Windows tray app that switches your display to a stretched resolution when Valorant, or another selected game/app, is running. When the tracked game or app closes, ValoStretch restores your native resolution automatically.

No manual display switching before every session. No forgetting to switch back. It stays in the tray, keeps resource usage low, and focuses on fast, predictable resolution recovery.

> **Portable** - distributed as a zip containing `ValoStretch.exe`.
> **Free** - always has been, always will be.

---

## v2.1 Highlight

### Any Game & App Auto Stretch

ValoStretch is no longer limited to Valorant automation. In v2.1, you can add other games and apps to Auto Stretch.

- Add currently running games/apps from a searchable candidate list
- Add any `.exe` manually
- Enable or disable each selected app independently
- Refresh running candidates only when you need to
- Restore native resolution when all tracked apps close
- Keep the system light by checking saved process names instead of crawling every installed app

Valorant automation is still built in, and the ValoConfig Patcher remains focused on Valorant.

---

## Features

| Feature | Description |
|---------|-------------|
| Any Game & App Auto Stretch | Apply stretch automation to selected games and apps, not only Valorant |
| Valorant Auto-Switch | Detects Valorant launch/close and switches resolution automatically |
| Full Stretch Mode | Briefly disables the internal laptop monitor to force true stretch |
| Resolution Only Mode | Changes resolution directly without monitor disable, ideal for desktops and external monitors |
| Global Hotkey | Press `Ctrl+Shift+F6` anytime to manually toggle stretch/native |
| ValoConfig Patcher | Writes stretch resolution directly into Valorant's `GameUserSettings.ini` |
| Custom Resolution Center | Create, test, search, and manage NVIDIA custom resolutions |
| Recovery Safety | Restores native resolution after app exit, crash, shutdown, or interrupted sessions |
| Usage Stats | Tracks sessions, switches, and total stretch time |
| System Tray | Lives in your tray with quick controls |
| Start with Windows | Auto-starts minimized so it is always ready |
| Smart Upgrade | Detects previous versions and handles migration automatically |

---

## Screenshots

Screenshots are being refreshed for v2.1. The current images may still show the v2.0 layout until the screenshot pass is complete.

<details>
<summary><b>Main Window</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/main-window.png" alt="Main Window" width="800"/>
</details>

<details>
<summary><b>Setup Wizard - Step 1: Monitor Selection</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/setup-wizard-step1.png" alt="Setup Wizard Step 1" width="700"/>
</details>

<details>
<summary><b>Setup Wizard - Step 2: Native Resolution</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/setup-wizard-step2.png" alt="Setup Wizard Step 2" width="700"/>
</details>

<details>
<summary><b>Setup Wizard - Step 3: Stretch Resolution</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/setup-wizard-step3.png" alt="Setup Wizard Step 3" width="700"/>
</details>

<details>
<summary><b>Setup Wizard - Step 4: Stretch Mode</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/setup-wizard-step4.png" alt="Setup Wizard Step 4" width="700"/>
</details>

<details>
<summary><b>Setup Wizard - Step 5: Startup and Registration</b></summary>
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
<summary><b>Update Detection</b></summary>
<br>
<img src="https://raw.githubusercontent.com/chotuoo592029-star/Valostretch-/main/screenshots/update-detected.png" alt="Update Detected" width="600"/>
</details>

---

## Download and Install

### Fresh Install

1. Go to [**Releases**](https://github.com/chotuoo592029-star/Valostretch-/releases/latest)
2. Download `ValoStretch.zip`
3. Extract the zip
4. Run `ValoStretch.exe`
5. Complete the setup wizard

No installer is required.

### Upgrading from v2.0 or Older

Run the new `ValoStretch.exe`. ValoStretch detects previous versions and offers to import your existing settings.

- **Import your settings** - keeps monitor, resolutions, preferences, stats, and startup behavior where possible
- **Fresh install** - clears old ValoStretch data and opens setup from scratch
- **Cancel** - exits without changing anything

Your auto-start entry is updated to point to the new app when migration is completed.

---

## Setup Guide

### Step 1 - Monitor Selection

Select the display ValoStretch should control. The monitor list shows clearer display names, active/inactive status, and instance ID details.

### Step 2 - Native Resolution

Set your normal desktop resolution, such as `2560 x 1440`.

### Step 3 - Stretch Resolution

Set the resolution you want for stretch mode, such as `2100 x 1440` or `1280 x 960`.

### Step 4 - Display Type

| Option | Best For | Behavior |
|--------|----------|----------|
| Laptop internal monitor only | Built-in laptop displays that need true stretch | Uses monitor disable/re-enable during switching |
| PC / external monitor | Desktop PCs and external displays | Direct resolution switching, no monitor disable |

**Important:** monitor-disable mode is intended for laptop internal screens only. For desktop PCs and external monitors, use direct resolution switching.

### Step 5 - Startup Options

- **Register on this PC** - keeps the portable app path stable
- **Start with Windows** - enabled by default for new setup
- **Pin to Start menu** - creates a Start menu shortcut

---

## How It Works

```
Valorant or a selected app/game starts
      |
ValoStretch detects the running process
      |
Display switches to the configured stretch resolution
      |
You play or use the selected app in stretch mode
      |
All tracked apps close
      |
ValoStretch restores native resolution automatically
```

ValoStretch keeps resource usage low by using event-driven detection where possible and saved process-name checks for selected apps. It does not scan your installed programs continuously.

---

## Any Game & App Auto Stretch

Open ValoStretch and choose **Any Game & App Auto Stretch**.

From there you can:

- Search running app candidates in real time
- Add a visible running app/game
- Use **Refresh** to reload currently running apps
- Use **Add .exe manually** for apps that are not currently running
- Toggle selected apps on or off
- Remove apps you no longer want to track

When any enabled selected app is running, ValoStretch applies the same stretch behavior used for Valorant. When all enabled tracked apps close, it restores native resolution.

---

## ValoConfig Patcher

The ValoConfig Patcher writes your stretch resolution directly into Valorant's `GameUserSettings.ini` file so Valorant requests the correct resolution on launch.

1. Open ValoStretch
2. Open **ValoConfig Patcher**
3. Review the detected account and config path
4. Confirm the target resolution
5. Apply the patch

Requires Valorant to have been launched at least once so the config file exists.

---

## Custom Resolution Center

For NVIDIA GPU users, ValoStretch can create and manage custom resolutions through NVAPI.

1. Open **Custom Resolution Center**
2. Select the target display
3. Enter width, height, and refresh rate
4. Test the resolution before saving
5. Manage saved custom resolutions from the same panel

Note: NVIDIA Control Panel may show a custom resolution checkbox differently from Windows availability. If the resolution is selectable and works in Windows/game settings, the mode has been registered successfully.

---

## Hotkey

The default global hotkey is `Ctrl+Shift+F6`.

To change it, open settings and press a new shortcut. `Ctrl` plus any key is accepted as a shortcut.

---

## System Requirements

| Requirement | Details |
|-------------|---------|
| OS | Windows 10 or Windows 11 64-bit |
| Runtime | None, self-contained |
| GPU | Any GPU for switching, NVIDIA required for Custom Resolution Center |
| Valorant | Required only for Valorant automation and ValoConfig Patcher |
| Disk | About 75 MB |
| RAM | Designed to stay lightweight at idle |
| CPU | Low usage, event-driven where possible |

---

## Troubleshooting

**Resolution does not switch when an app starts**
- Make sure automation is enabled
- Make sure the app is enabled inside Any Game & App Auto Stretch
- Use Refresh while the app is open, then add it from the candidate list
- If needed, add the app's `.exe` manually

**Resolution does not restore after closing an app**
- Disable or remove apps you no longer want tracked
- Make sure no other enabled tracked app is still running
- Use Relaunch or Exit to trigger recovery if the app was closed unexpectedly

**Monitor blanks or behaves strangely**
- Use PC / external monitor mode for desktop PCs and external displays
- Use laptop internal monitor mode only when you specifically need monitor-disable true stretch

**ValoConfig Patcher says config not found**
- Launch Valorant at least once, then try again
- Make sure you are logged into your Riot account

**Custom resolutions do not appear**
- NVIDIA GPU is required for NVAPI custom resolution injection
- Restart Windows if the driver needs to refresh available modes
- Verify the resolution is available in Windows display settings or the target game

---

## Privacy

ValoStretch does not:

- Connect to the internet for telemetry
- Collect personal data
- Require an account
- Upload your app list
- Modify game memory

All config, logs, stats, and selected app profiles are stored locally in `%LocalAppData%\ValoStretch\`.

---

## Uninstalling

Open ValoStretch and choose **Uninstall ValoStretch**.

The app asks for a reason, then opens a confirmation window. You must type `uninstall` before removal continues.

Uninstall removes ValoStretch data, startup entries, shortcuts, and app-owned custom settings. It does not remove unrelated system files or other apps.

---

## Changelog

See [**CHANGELOG.md**](CHANGELOG.md) for the full patch notes.

**Latest - v2.1**

- Added Any Game & App Auto Stretch
- Reworked dashboard, Custom Resolution Center, and Auto Stretch panels
- Improved startup/setup flow and migration behavior
- Improved shutdown/crash/session recovery back to native resolution
- Fixed selected app disable/remove behavior so native restoration works correctly
- Improved NVIDIA custom resolution cleanup to avoid duplicate entries

---

## Support and Community

- **Bug reports** - [GitHub Issues](https://github.com/chotuoo592029-star/Valostretch-/issues/new?template=bug_report.md)
- **Feature requests** - [GitHub Issues](https://github.com/chotuoo592029-star/Valostretch-/issues/new?template=feature_request.md)
- **Discord** - [Join the server](https://discord.gg/uA3sMpFAuG)

---

## Disclaimer

ValoStretch is an independent tool not affiliated with Riot Games. It operates at the Windows display API level and does not modify game files or memory. Use at your own discretion.

---

<div align="center">

Made with passion by **Vibe** &nbsp;&middot;&nbsp; &copy; 2026

</div>
