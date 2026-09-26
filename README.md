<div align="center">

# 🛰️ ORBIT OPTIMIZER
### AN OPTIMIZER FOR WINDOWS 11/10

![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%20Windows%2011-0078D6?style=flat-square)
![Version](https://img.shields.io/badge/Version-1.0.0-2DD4BF?style=flat-square)
![Made by](https://img.shields.io/badge/Made%20by-PRIMEx-8B98A5?style=flat-square)
[![Download](https://img.shields.io/badge/Download-Setup%20.exe-2DD4BF?style=flat-square)](https://github.com/saksham123107-pixel/ORBIT-OPTIMIZER/raw/main/ORBIT%20OPTIMIZER%20Setup.exe)

**Fast, safe and reversible system tweaks with a clean interface.**

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

1. Click the **Download** badge above — or grab `ORBIT OPTIMIZER Setup.exe` from this repo
2. Run it — that's it. No admin prompt, no extra files needed.

The installer automatically:

- installs the app to `%LocalAppData%\Programs\ORBIT OPTIMIZER`
- installs the **WebView2 Runtime** if it's missing (the UI depends on it)
- creates Start Menu + Desktop shortcuts
- registers itself in **Settings → Apps**

> The setup file is fully self-contained — share just that one file.

## ⚠️ Before You Tweak — Read This

**Create a restore point first.** One wrong registry value can destabilize Windows.

### Create a restore point (30 seconds)

1. Press `Win + S`, type **"Create a restore point"**, open it
2. Select your system drive (usually `C:`) → click **Create…**
3. Name it e.g. `before-orbit` → **Create**

Or run this in **PowerShell (Admin)**:

```powershell
Checkpoint-Computer -Description "Before ORBIT OPTIMIZER" -RestorePointType MODIFY_SETTINGS
```

> Restore points are limited by the disk space Windows allocates —
> create yours right before applying a big batch of tweaks.

### Rules of caution

- **Apply a few tweaks at a time**, not everything at once — so if something breaks,
  you know exactly which tweak did it
- **Restart after applying** — some tweaks (CPU priority, power plan) only take
  effect after a reboot
- **Read what you enable** — each card describes what it changes
- **Don't tweak what you don't recognize** — if a description is unclear, skip it
- **Keep the app's backup active** — ORBIT OPTIMIZER stores your original values
  and can revert every tweak from the card itself
- Gaming/performance gains vary by hardware — this is not a magic FPS button

### If something goes wrong

1. **First:** open ORBIT OPTIMIZER → **revert** the tweaks you applied
2. **Still broken:** boot into Safe Mode → run the app → revert everything
3. **Last resort:** boot from recovery → *System Restore* → pick your
   `before-orbit` restore point
4. **Nuclear option:** `Settings → System → Recovery → Reset this PC`
   (keep *My files* if you just want a clean Windows)

## Uninstall

**Settings → Apps → ORBIT OPTIMIZER → Uninstall**

or run `Uninstall ORBIT OPTIMIZER.exe` from the install folder.

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
```

## ❗ Disclaimer

- ORBIT OPTIMIZER modifies **system registry and Windows settings** — use it at
  **your own risk**
- The authors are **not responsible** for any damage, data loss, instability,
  activation issues or performance regressions caused by using this software
- Always create a **restore point** before applying tweaks
- Some tweaks may be flagged by antivirus software as false positives —
  the app is open source, inspect it yourself
- Not affiliated with Microsoft, Discord or any other company

## License

MIT © PRIMEx
