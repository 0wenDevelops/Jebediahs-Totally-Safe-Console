# Jebediah's Totally Safe Console

<p align="center">
  <strong>A single-player Kerbal Space Program utility console for testing, debugging, launch checks, visual experiments, and controlled chaos.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Game-Kerbal%20Space%20Program-blue?style=for-the-badge" alt="Kerbal Space Program">
  <img src="https://img.shields.io/badge/Type-KSP%20DLL%20Mod-green?style=for-the-badge" alt="KSP DLL Mod">
  <img src="https://img.shields.io/badge/Install-GameData-orange?style=for-the-badge" alt="GameData Install">
  <img src="https://img.shields.io/badge/Use-Single%20Player-red?style=for-the-badge" alt="Single Player Only">
</p>

---

## Overview

**Jebediah's Totally Safe Console** is a Kerbal Space Program mod menu made for single-player sandbox testing and debugging.

It gives you quick in-game tools for vessel testing, resources, launch readiness checks, black box style mission reports, visual effects, world tools, crew tools, and experimental chaos features.

The menu opens in-game with **F8**.

> Back up your saves before using experimental tools. KSP mods can break saves, craft files, missions, or active vessels if something goes wrong.

---

## Features

Current and planned tool categories include:

- **Resource tools** for testing craft behavior with different resource states
- **Vessel tools** for debugging active craft problems
- **Orbit and flight assists** for sandbox testing
- **Visual tools** for overlays, effects, and presentation testing
- **Launch readiness checks** for common launch pad issues
- **Black box reports** for reviewing mission failure data
- **Crew tools** for Kerbal-related testing
- **World tools** for scene and environment testing
- **Chaos tools** for intentionally unsafe experiments
- **Settings and debug tools** for menu behavior and troubleshooting

---

## Controls

| Key | Action |
| --- | --- |
| `F8` | Open or close the console |

---

## Installation

1. Download the latest release package from the repository releases page.
2. Extract the archive.
3. Copy the mod folder into your KSP `GameData` folder.
4. Confirm the DLL is inside the mod's `Plugins` folder.
5. Launch KSP and press **F8** in-game.

Expected install layout:

```text
Kerbal Space Program/
└── GameData/
    └── JebediahsTotallySafeConsole/
        └── Plugins/
            └── JebediahsTotallySafeConsole.dll
```

Do not place the DLL directly in `GameData`. KSP mods should stay inside their own mod folder.

---

## Building From Source

Create a C# class library project and reference the required KSP and Unity assemblies from your local KSP install.

Common reference folder:

```text
Kerbal Space Program/KSP_x64_Data/Managed/
```

Common references:

```text
Assembly-CSharp.dll
Assembly-CSharp-firstpass.dll
UnityEngine.dll
UnityEngine.CoreModule.dll
UnityEngine.IMGUIModule.dll
UnityEngine.InputLegacyModule.dll
UnityEngine.PhysicsModule.dll
UnityEngine.TextRenderingModule.dll
```

After building, place the compiled DLL here:

```text
GameData/JebediahsTotallySafeConsole/Plugins/JebediahsTotallySafeConsole.dll
```

---

## Suggested Repository Layout

This is the preferred structure for keeping the repo clean:

```text
Jebediahs-Totally-Safe-Console/
├── GameData/
│   └── JebediahsTotallySafeConsole/
│       └── Plugins/
│           └── JebediahsTotallySafeConsole.dll
├── src/
│   └── JebediahsTotallySafeConsole.cs
├── assets/
│   ├── screenshots/
│   └── demo/
├── docs/
│   └── RELEASE_CHECKLIST.md
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── PULL_REQUEST_TEMPLATE.md
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── README.md
└── SECURITY.md
```

Use `src/` for source code, `assets/` for images or demo media, `docs/` for extra documentation, and `GameData/` only for install-ready KSP files.

---

## Troubleshooting

### The menu does not open

Check that:

- The mod folder is inside `GameData`
- The DLL is inside the mod's `Plugins` folder
- You are pressing **F8**
- You built against assemblies from the same KSP install you are testing with
- The game was restarted after installing the mod

### Some buttons do nothing

Some tools only work when:

- You are in flight
- A vessel is active
- The vessel has the required parts or modules
- The current KSP scene supports the feature
- The feature has already been implemented in the current build

### Readiness warnings are not showing

The readiness scanner is mainly meant for craft on the launch pad or runway. Open the **Readiness** tab and run a manual scan if automatic checks do not appear.

### Black box data is empty

The black box system needs flight data. Launch a vessel, fly for a bit, stage, overheat, crash, recover, or revert, then check the black box report again.

---

## Roadmap

Possible future additions:

- Saved black box reports
- Exportable mission reports
- Better replay or ghost systems
- Cinematic camera markers
- More launch readiness checks
- More visual presets
- More vessel diagnostics
- Config file support
- Custom keybind support
- Better modded-part detection

---

## License

This project uses a custom **source-available personal-use license**.

You may view and use the project for personal single-player use, but you may not repost, redistribute, sell, reupload, publish modified versions, or claim the project as your own.

See [`LICENSE`](LICENSE) for the full terms.

---

## Disclaimer

This mod is intended for **single-player Kerbal Space Program** use only.

Use it at your own risk. The author is not responsible for broken saves, destroyed rockets, lost progress, mod conflicts, stranded Kerbals, unexpected Kraken activity, or questionable engineering decisions.

Jeb will not read this warning.