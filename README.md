# Jebediah’s Totally Safe Console

<p align="center">
  <img src="demo.gif" alt="Jebediah’s Totally Safe Console Demo" width="800">
</p>

<p align="center">
  <b>A single-player Kerbal Space Program utility, debug, visual, chaos, launch-check, and black box report mod menu.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Game-Kerbal%20Space%20Program-1f6feb?style=for-the-badge" alt="Kerbal Space Program">
  <img src="https://img.shields.io/badge/Type-DLL%20Mod-2ea043?style=for-the-badge" alt="DLL Mod">
  <img src="https://img.shields.io/badge/Install-GameData-f0883e?style=for-the-badge" alt="GameData Install">
  <img src="https://img.shields.io/badge/Use-Single%20Player-d73a49?style=for-the-badge" alt="Single Player">
</p>

---

## Overview

**Jebediah’s Totally Safe Console** is a single-player Kerbal Space Program mod menu built for sandbox testing, vessel debugging, resource control, visual effects, launch readiness checks, mission chaos, and post-flight black box reports.

The menu is organized into tabs for resources, vessel tools, orbit assists, visuals, black box reports, launch readiness warnings, crew tools, world tools, chaos effects, settings, and debugging.

Press **F8** in-game to open or close the menu.

---

![Demo](DemoGif.gif)

---

## Controls

| Key | Action |
| --- | --- |
| `F8` | Open / close the menu |

---

## Recommended Use

This mod is best used for:

- Single-player sandbox testing
- Debugging broken craft
- Testing staging setups
- Learning why rockets fail
- Reentry testing
- Landing practice
- Visual experiments
- Cinematic chaos
- Mission failure reports
- General KSP messing around

---

## Compatibility

This is a normal KSP DLL mod.

It is installed like most classic KSP mods:

```text
GameData/ModFolder/Plugins/ModName.dll
```

Best compatibility is expected with standard KSP 1.x installs.

Compatibility may depend on:

- Your KSP version
- Installed mods
- Craft part modules
- Save mode
- Build references
- Whether the feature is being used in the correct scene

---

## Building From Source

Create a C# class library project and reference the required KSP and Unity assemblies from your KSP install.

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

## Project Layout

```text
JebediahsTotallySafeConsole/
├── GameData/
│   └── JebediahsTotallySafeConsole/
│       └── Plugins/
│           └── JebediahsTotallySafeConsole.dll
├── assets/
│   ├── demo.gif
│   ├── main_menu.png
│   ├── resources.png
│   ├── visuals.png
│   ├── black_box.png
│   ├── readiness.png
│   └── chaos.png
├── src/
│   └── JebediahsTotallySafeConsole.cs
├── README.md
└── LICENSE
```

---

## Troubleshooting

### The menu does not open

Check that:

- The mod folder is inside `GameData`
- The `.dll` is inside the mod’s `Plugins` folder
- You are pressing **F8**
- The DLL was built against your KSP install’s assemblies
- You launched the game after installing the mod

### Some buttons do nothing

Some tools only work when:

- You are in flight
- A vessel is active
- The vessel has the required parts
- The required KSP system is available
- The current scene supports the feature

### Readiness warnings are not showing

The readiness scanner is mainly designed to run when the active vessel is on the launch pad or runway.

You can also open the **READINESS** tab and run a manual scan.

### Black box data is empty

The black box recorder needs flight data.

Launch a vessel, fly for a bit, stage, overheat, crash, recover, or revert, then check the **BLACK BOX** tab.

### Visual effects are stuck on my craft

Open the **VISUALS** tab and use:

```text
Reset Vessel Colors / Clear Visual Overlays
```

---

## Roadmap

Possible future additions:

- Saved black box reports
- Exportable mission reports
- Better replay ghost system
- Cinematic camera markers
- More launch readiness checks
- More visual presets
- More vessel diagnostics
- Config file support
- Custom keybind support
- Better modded-part detection

---

## Disclaimer

This mod is intended for **single-player Kerbal Space Program** use only.

Back up your saves before using save-affecting or experimental tools.

The author is not responsible for broken saves, destroyed rockets, unexpected Kraken activity, failed missions, stranded Kerbals, or questionable engineering decisions.

Use responsibly. Jeb will not.
