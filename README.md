# ORBIT-OPTIMIZER
<div align="center">

# 🛰️ ORBIT OPTIMIZER
### AN OPTIMIZER FOR WINDOWS 11/10

![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%20Windows%2011-0078D6?style=flat-square)
![Version](https://img.shields.io/badge/Version-1.0.0-2DD4BF?style=flat-square)
![Made by](https://img.shields.io/badge/Made%20by-PRIMEx-8B98A5?style=flat-square)

**Fast, safe and reversible system tweaks with a clean glass interface.**

</div>

---

## About

ORBIT OPTIMIZER is a lightweight Windows tuning suite. It gives you one-click access to
hundreds of carefully organized system tweaks — CPU scheduling, power plan tuning,
privacy hardening, personalization and input tweaks — without digging through
regedit or Group Policy.

- **300+ tweak cards** in categorized groups
- **One-click apply / revert** — every tweak is tracked and reversible
- **Freemium** — core tweaks are free, premium unlocks the full pack
- **No admin rights required** — installs and runs per-user

## Installation

1. Download **`ORBIT OPTIMIZER Setup.exe`** from [Releases](../../releases)
2. Run it — that's it. No admin prompt, no extra files needed.

The installer automatically:
- installs the app to `%LocalAppData%\Programs\ORBIT OPTIMIZER`
- installs the **WebView2 Runtime** if it's missing (the UI depends on it)
- creates Start Menu + Desktop shortcuts
- registers itself in **Settings → Apps**

> The setup file is fully self-contained — share just that one file.

## Uninstall

**Settings → Apps → ORBIT OPTIMIZER → Uninstall**

or right-click the desktop shortcut → *Open file location* → run
`Uninstall ORBIT OPTIMIZER.exe`

Removes all program files, shortcuts and the Apps & features entry.

## System Requirements

| | Requirement |
|---|---|
| OS | Windows 10 (1803+) or Windows 11, 64-bit |
| Runtime | WebView2 Runtime (installed automatically) |
| Disk | ~40 MB |
| Internet | Only required for signing in |

## Usage

1. Launch **ORBIT OPTIMIZER**
2. Sign in with your license key / Discord account
3. Browse categories → toggle the tweaks you want → hit **Apply**
4. Revert any tweak at any time from the same card

## Build from source

```bash
# Frontend (Vite + TypeScript)
cd frontend
npm install
npm run build

# Native host (C++17 / MinGW-w64)
cd ../native
cmake -B build3 -G "MinGW Makefiles" -DCMAKE_BUILD_TYPE=Release
cmake --build build3 --config Release

# Installer
cd ../installer
./build_setup.ps1
