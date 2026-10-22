<p align="center"><img src="docs/img/icon.png" width="128" alt="App icon: a sand-stone tower with a crimson pennant"></p>

<h1 align="center">Strong Hold</h1>

<p align="center"><b>A native Mac engine for Stronghold Crusader: Definitive Edition.</b><br>
No Windows, no CrossOver: open the app, sign in to Steam once, play.</p>

<p align="center"><a href="https://github.com/YannickAaron/Strong-Hold/releases/latest/download/Strong-Hold.dmg"><b>Download for Mac</b></a> · <a href="https://yannickaaron.github.io/Strong-Hold/">Website</a></p>

![A skirmish on Crater Lake running in the native engine](docs/img/game.jpg)

**Built in Rust, native on Apple Silicon.** The original game is a Unity front end driving a Windows-only
simulation library. This project rebuilds that simulation from scratch in Rust and draws it with Metal: no Windows,
no CrossOver, no emulation. Your castles, your economy and the lords you fight run as native code, checked tick by
tick against the original.

| 120 fps | 12× fast-forward | ~1 s | 41 MB |
|:---:|:---:|:---:|:---:|
| steady frame rate | about 500 ticks a second (normal: 40) | to load a save | download, engine only |

[▶ Watch it run](https://yannickaaron.github.io/Strong-Hold/#video) · measured on an M1 Max

## You need

- A Mac with Apple Silicon (M1 or newer), macOS 12 or newer
- [Stronghold Crusader: Definitive Edition](https://store.steampowered.com/app/3024040/) on your Steam account
- About 9.5 GB of free disk space
- Optional: the Steam app on your phone, to sign in by scanning a code

## Install

1. [Download the app](https://github.com/YannickAaron/Strong-Hold/releases/latest/download/Strong-Hold.dmg) (always the newest version; older ones: [Releases](https://github.com/YannickAaron/Strong-Hold/releases)).
2. Open it and drag **Strong Hold** into Applications.
3. The first time only, because the app isn't notarized by Apple yet:
   - macOS 14: right-click the app and choose **Open**.
   - macOS 15 or newer: open it once, then go to System Settings › Privacy & Security and click **Open Anyway**.
4. Follow the setup window. Afterwards the app opens straight to the main menu.

## First start

The app brings the engine, not the game. The first time you open it, a setup window gets the graphics, sounds, maps
and videos from **your own copy** of the game, once:

| | |
|---|---|
| ![Setup before the download](docs/img/setup-steam.jpg) | **Check, then sign in to Steam.** Setup checks for a Steam account that owns the game, about 9.5 GB free and an internet connection. Then scan a code with the Steam app on your phone, or use your user name, password and Steam Guard code. The Steam app for Mac doesn't need to be installed. |
| ![Setup with a copy found](docs/img/setup.jpg) | **Already on this Mac?** A copy of the game found on the Mac (for example in CrossOver) is used directly: one click, no download. |
| ![Setup preparing the assets](docs/img/setup-progress.jpg) | **Download and prepare.** Your copy downloads (about 6.2 GB), then its assets are prepared for the native engine in a few minutes. |

Your Steam sign-in goes to Steam through Valve's open-source DepotDownloader, which the app carries. Your password is
passed to it once and never saved. The game's files go to `~/Library/Application Support/Strong Hold`.

## What's there

Skirmish against AI lords, the historical campaigns, the Crusader Trail, sandbox, local network multiplayer, saving
and loading, the original music, speech and videos, and Mac touches: menu bar, trackpad zoom and rotate, full-screen
Spaces. The port is in active development; parts of the simulation are still being checked against the original.

Something wrong? [Open an issue](https://github.com/YannickAaron/Strong-Hold/issues) and attach
`~/Library/Logs/Strong Hold.log`.

## Legal

Strong Hold is an unofficial, free, non-commercial fan project. It is not affiliated with, endorsed or sponsored by
Firefly Studios. Stronghold and Stronghold Crusader are trademarks of Firefly Studios; they are used here only to say
which game this engine works with. The app contains no files from the game: it needs your own copy of Stronghold
Crusader: Definitive Edition, bought on Steam, and reads the graphics, sounds and maps from that copy on your Mac.

Firefly Studios, or anyone with a concern about this project: please
[open an issue](https://github.com/YannickAaron/Strong-Hold/issues) and it will be answered promptly.

The app includes [DepotDownloader](https://github.com/SteamRE/DepotDownloader) 3.4.0 by SteamRE, licensed GPL-2.0;
its licence is inside the app (`Contents/Resources/LICENSE-DepotDownloader.txt`) and its source is at
https://github.com/SteamRE/DepotDownloader/tree/DepotDownloader_3.4.0 (also attached to every release).

The app also includes open-source Rust libraries and libvpx; their licences are in
`Contents/Resources/THIRD-PARTY-NOTICES.txt` inside the app.
