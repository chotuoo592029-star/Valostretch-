# ValoStretch Patch Notes

> **Latest release:** v2.1 - Any Game & App Auto Stretch  
> **Build:** Portable zip containing `ValoStretch.exe`  
> **Platform:** Windows 10/11 x64  
> **Framework:** .NET 8 self-contained, no runtime required

---

## v2.1 - Any Game & App Auto Stretch

v2.1 expands ValoStretch beyond Valorant-only automation. The main feature of this update is **Any Game & App Auto Stretch**, which lets users select additional games or apps and have ValoStretch apply the same stretch/native switching behavior automatically.

### Headline Feature

#### Any Game & App Auto Stretch

- Added a new Auto Stretch panel for selected games and apps
- Users can add currently running apps from a searchable candidate list
- Users can add any `.exe` manually
- Each selected app can be enabled, disabled, or removed independently
- ValoStretch applies stretch when any enabled selected app is running
- ValoStretch restores native resolution when all enabled tracked apps close
- Running app detection stays lightweight and avoids continuous installed-app crawling

### UI and Workflow

- Reworked the main dashboard layout around a stronger hero section
- Moved user stats and credit line into the hero area
- Reorganized automation, mouse precision, tools, settings, Discord, relaunch, and uninstall actions
- Rebuilt the Custom Resolution Center as an in-page panel
- Rebuilt Any Game & App Auto Stretch as an in-page panel
- Improved Discord and relaunch button presentation
- Added a safer uninstall reason step before the final uninstall confirmation
- Kept the interface focused on low resource usage with no heavy background UI work

### Setup Wizard

- Reworked the display type step into two clear choices:
  - Laptop internal monitor only - true stretch with monitor disable
  - PC / external monitor - direct resolution switching
- Added stronger warnings that monitor-disable mode is intended for laptop internal screens only
- Improved monitor selection labels with clearer display name, active/inactive state, and instance ID
- Enabled Start with Windows by default on the final setup step
- Fixed broken onboarding/next button text
- Allowed setup wizard final step and logs to scroll when needed

### Custom Resolution Center

- Combined create and manage behavior into a cleaner Custom Resolution Center workflow
- Added saved resolution search and management improvements
- Improved NVIDIA custom resolution cleanup before saving new modes
- Reduced duplicate custom resolution entries
- Improved handling around tested and accepted custom display modes

### Reliability and Recovery

- Added stronger display recovery behavior for interrupted sessions
- Improved restore-to-native behavior on app exit, crash, shutdown, and session ending
- Added recovery state handling so ValoStretch can recover the display after an unsafe close
- Improved relaunch and exit flows so recovery is easier to trigger
- Fixed selected app disable/remove behavior so it restores native when the tracked app should no longer control stretch

### Migration and Upgrade

- Updated configuration schema for v2.1
- Improved previous-version detection
- Improved migration cleanup safety
- Preserved current app data during import where appropriate
- Improved startup entry cleanup and registration behavior
- Cleaned up migration window text and button presentation

### Shortcut and Settings

- Added helper text explaining that `Ctrl` plus any key can be used as a shortcut
- Moved shortcut-related controls into the automation/settings workflow
- Removed duplicate relaunch placement so relaunch stays in tools/maintenance

### Bug Fixes

- Fixed disabled or removed Auto Stretch app profiles not restoring native correctly
- Fixed duplicate custom resolution creation paths
- Fixed setup wizard text rendering issues
- Fixed Start with Windows default state during first setup
- Fixed migration detection for existing users by bumping schema version
- Fixed several cramped or overlapping UI sections

### Known Notes

- NVIDIA Control Panel can sometimes show a custom resolution as unchecked even when Windows and games can use it. If the resolution appears in Windows/game resolution lists and applies correctly, the mode is available.
- Screenshots in the public repository may briefly show older v2.0 UI until the v2.1 screenshot refresh is completed.

---

## v2.0 - Major Update

v2.0 introduced the modern ValoStretch foundation: migration, rebuilt Valorant config patching, smoother WPF rendering, redesigned tray controls, onboarding, and better uninstall behavior.

### Smart Upgrade System

- Added automatic previous-version detection
- Added migration dialog for importing old settings or starting fresh
- Added schema versioning to distinguish old and new configs
- Updated auto-start entries to point to the new executable after migration

### Main Window Redesign

- Reworked tool and system areas
- Added stronger visual hierarchy for ValoConfig Patcher
- Improved Discord, relaunch, logs, and uninstall button presentation
- Added usage stats to the main UI

### Valorant Config Patcher

- Rebuilt path detection for Valorant config files
- Fixed editing behavior so existing keys are updated in place
- Added account/config detection UI
- Added editable patch values
- Added read-only protection option after patching

### Uninstall

- Rebuilt uninstall confirmation
- Added clearer removal details
- Removed ValoStretch config, logs, stats, startup entries, shortcuts, app copy, and Valorant config patch where applicable
- Kept unrelated files and apps untouched

### Setup Wizard and Onboarding

- Added Start menu pin option
- Added first-launch onboarding
- Enabled the global hotkey by default
- Improved setup flow for new users

### Performance and Smoothness

- Restored hardware rendering by removing transparent software-rendered window behavior
- Paused UI polling while hidden to tray
- Increased runtime check intervals
- Added startup memory compaction

### System Tray

- Redesigned right-click tray menu
- Added live mode, resolution, session, switch, and stretch-time details
- Improved quick controls for native, stretch, automation, open, and exit

### Stats

- Added usage stats stored locally in `%LocalAppData%\ValoStretch\stats.json`
- Tracked sessions, total switches, stretch activations, native restorations, total stretch time, and last switch time

### v2.0 Bug Fixes

- Fixed Valorant config patcher path detection
- Fixed patching values being appended instead of edited in place
- Fixed old executable auto-starting after migration
- Fixed migration dialog not appearing for old configs
- Fixed laggy window animations caused by software rendering
- Reduced unnecessary polling while minimized

---

## File Locations

| File | Path |
|------|------|
| Config | `%LocalAppData%\ValoStretch\config.json` |
| Stats | `%LocalAppData%\ValoStretch\stats.json` |
| Logs | `%LocalAppData%\ValoStretch\logs\app.log` |
| Selected app profiles | Stored inside ValoStretch local config |
| Onboarding marker | `%LocalAppData%\ValoStretch\.onboarding-done` |
| Registered app copy | `%LocalAppData%\Programs\ValoStretch\` |
| Start Menu shortcut | `%AppData%\Microsoft\Windows\Start Menu\Programs\ValoStretch.lnk` |

---

## Distribution

ValoStretch is distributed as a portable zip:

```text
ValoStretch.zip
+-- ValoStretch.exe
```

Extract the zip, run `ValoStretch.exe`, and complete setup. No installer and no separate .NET runtime are required.
