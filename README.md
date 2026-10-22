<p align="center">
  <img src="app-icon.png" width="96" alt="Roblox Multi-Instance icon">
</p>

<h1 align="center">Roblox Multi-Instance</h1>

<p align="center">
  Run more than one Roblox client at the same time on Windows.<br>
  One small portable <code>.exe</code>. No installer.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.6-2f6fed" alt="Version 1.0.6">
  <img src="https://img.shields.io/badge/license-Freeware-orange" alt="Freeware">
  <img src="https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-0078D6?logo=windows&logoColor=white" alt="Windows 10 | 11">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Tauri-2-24C8DB?logo=tauri&logoColor=white" alt="Built with Tauri 2">
  <img src="https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white" alt="Rust">
  <img src="https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white" alt="TypeScript">
</p>

<p align="center">
  <a href="https://github.com/carl-anmm/Multi-Instance-Roblox/stargazers"><img src="https://img.shields.io/github/stars/carl-anmm/Multi-Instance-Roblox?style=social" alt="GitHub stars"></a>
</p>

<p align="center">
  <a href="../../releases/latest"><b>⬇ Download the latest version</b></a>
</p>

---

## About

Normally, opening a second Roblox client closes the first one, or hands it off to the client that's already open. Roblox Multi-Instance turns that check off, so several clients can stay open side by side. For example, you can play on your main account and an alt at the same time.

It does not modify Roblox's files and does not inject anything into the game.

## Features

- **One-click toggle** with a status light. Green means on, amber means waiting for Roblox to close, and grey means off.
- **Works even if Roblox is already open.** You don't have to close Roblox first.
- **Launch Roblox** button that opens a new client.
- **Close all Roblox** button, with a confirmation step.
- **Stays in the system tray.** Closing the window keeps multi-instance running.
- **Asks before quitting**, so you don't turn it off by accident.
- **Detects Roblox's "start with Windows" entry**, which can block multi-instance, and offers to turn it off. The entry is backed up and can be restored.
- **Optional:** start with Windows and turn on automatically.
- **Portable.** Settings are saved in `settings.json` next to the `.exe`.
- **Light and dark theme** that follows Windows.

## Requirements

- Windows 10 or 11, 64-bit
- Microsoft Edge WebView2, which is already included with Windows 10 and 11

## How to use

1. [Download](../../releases/latest) `roblox-multi-instance.exe` and put it in any folder.
2. Run it. The status light should turn **green**.
3. Open Roblox as many times as you want. Use the **Launch Roblox** button, or join games from the website.
4. Leave the app running in the tray while you play. To quit, right-click the tray icon and choose **Quit**.

> **Use a different account in each client.** Roblox only allows one account to be in a game once at a time. If the same account joins in two clients, one of them gets kicked.
>
> An easy way to use different accounts is a separate browser profile for each one. Click **Play** on the website from each profile.

## FAQ

**Windows says "Windows protected your PC". Is it safe?**
The app isn't code-signed, so Windows SmartScreen warns about it the first time it runs. Click **More info**, then **Run anyway**. Only download the app from this page's [Releases](../../releases).

**Can I get banned?**
The app doesn't touch the game itself or Roblox's files. However, running several clients is a gray area under Roblox's Terms of Use, so use it at your own risk.

**It stopped working after a Roblox update.**
Roblox sometimes changes how its single-client check works. Check [Releases](../../releases) for an update.

**Does it work with Bloxstrap?**
Yes. Clients you start from the website work as usual. Clients started with the app's **Launch Roblox** button open the Roblox player directly, so Bloxstrap mods aren't applied to them.

**What if the app is force-closed from Task Manager?**
Multi-instance stays on until you close all Roblox windows, then everything resets by itself. Quitting from the tray menu cleans up straight away.

**How do I uninstall it?**
If you turned on **Start with Windows**, turn it off in the app first. Then quit the app and delete the `.exe` and `settings.json`.

## How it works

Roblox makes sure only one client runs by creating a named Windows object. A new client that finds it hands off to the existing one and closes. This app claims that name before Roblox can. If Roblox is already running, the app locks the existing object so new clients can't see it. When you turn the app off or quit it, everything goes back to normal.

## ⭐ Like it?

If Roblox Multi-Instance is useful to you, please **give it a star** ⭐ at the top of this page. It's free, takes one click, and helps other players find the app.

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## Disclaimer

This project is not affiliated with, endorsed by or sponsored by Roblox Corporation. "Roblox" is a trademark of Roblox Corporation.

## Credits

The technique is based on these open-source projects: [BloxNest](https://github.com/bloxnest/BloxNest), [MultiBloxy](https://github.com/Zgoly/MultiBloxy) and [MultiRoblox](https://github.com/techbobkl-web/MultiRoblox).

## License

Freeware. It's free to use, but it isn't open source, and redistributing, modifying or selling it isn't allowed. See [LICENSE](LICENSE) for the full terms.

© 2026 Carl Mayorga. All rights reserved.
