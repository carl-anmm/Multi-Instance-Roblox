# Changelog

All notable changes to Roblox Multi-Instance are listed here.

## [1.0.6] - 2026-10-23

### Fixed

- **Multi-instance could fail when Roblox was already open.** It now works reliably.
- **Turning multi-instance off now really turns it off** when Roblox is already running. Previously, Roblox's lock stayed blocked until every Roblox client was closed.
- **Quitting the app now releases Roblox's lock properly.**
- Turning multi-instance off at the same moment as the automatic status refresh could switch it back on.
- Settings are saved more safely, so a crash during a save can't wipe the backup of Roblox's startup entry.
- Restoring Roblox's "start with Windows" entry now keeps it working exactly as before.
- A failed settings save no longer changes the setting anyway.
- "Start with Windows" now stays correct if you move the exe to another folder.
- **Tray → Launch Roblox** now shows an error message if it fails, instead of doing nothing.
- Clicking two settings quickly no longer loses the first change.
- Launching many clients in one session no longer risks two of them colliding.

### Changed

- The license is now freeware: free to use, closed source.

## [1.0.5] - 2026-10-23

First release.

### Added

- Multi-instance toggle with an on / waiting / off status and a running-client counter.
- Works even if Roblox is already open.
- **Launch Roblox** and **Close all Roblox** buttons. Close all asks for confirmation.
- System tray icon with a menu. Closing the window keeps the app running in the tray.
- Confirmation before quitting, so multi-instance isn't turned off by accident.
- Detects Roblox's "start with Windows" tray process, which can block multi-instance, and offers to turn it off. The entry is backed up and can be restored.
- Settings: turn on at start, keep running in tray, and start with Windows.
- Portable: a single `.exe` with settings saved in `settings.json` next to it.
- Version shown in the window title, the app heading and the exe's file properties.
- Light and dark theme that follows Windows.
