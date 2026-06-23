# Jebediah’s Totally Safe Console

<p align="center">
  <img src="assets/demo.gif" alt="Jebediah’s Totally Safe Console Demo" width="800">
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

## Demo

### GIF Preview

```text
assets/demo.gif
```

<p align="center">
  <img src="assets/demo.gif" alt="Mod Menu Demo" width="800">
</p>

### Screenshots


<p align="center">
  <img src="assets/main_menu.png" alt="Main Menu" width="32%">
  <img src="assets/resources.png" alt="Resources Tab" width="32%">
  <img src="assets/visuals.png" alt="Visuals Tab" width="32%">
</p>

<p align="center">
  <img src="assets/black_box.png" alt="Black Box Tab" width="32%">
  <img src="assets/readiness.png" alt="Readiness Scanner" width="32%">
  <img src="assets/chaos.png" alt="Chaos Tab" width="32%">
</p>

---

## Features

### Dashboard

- Active vessel overview
- Scene and vessel status
- Resource snapshot
- Active toggle summary
- Basic flight information

### Resource Tools

- Refill all resources
- Drain all resources
- Infinite common resources
- Individual resource toggles
- Fuel and oxidizer presets
- Electric charge tools
- Custom resource editor
- Resource percentage tools

### Vessel Tools

- Kill vessel velocity
- Kill horizontal velocity
- Kill vertical velocity
- Stabilize rotation
- Panic stabilize
- Soft landing assist
- Hover assist
- Velocity dampener
- Launch upward
- Prograde and retrograde velocity nudges
- No overheating
- Unbreakable-ish parts

### Orbit Tools

- Circularize at current altitude
- Set approximate circular speed
- Prograde / retrograde nudges
- Radial and normal nudges
- Orbit data display
- Panic circular-ish stabilize

### Visual Tools

- Vessel paint presets
- Random vessel colors
- Reset vessel colors
- Smooth rainbow mode
- Red pulse mode
- Emergency flashing mode
- Emergency strobe mode
- Heat warning visualizer
- Active vessel highlight
- Light controls
- Solar panel controls

### Black Box Report

The black box system records flight data and helps explain what happened during a mission.

Tracks:

- Max speed
- Max altitude
- Max G-force
- Hottest part
- Highest temperature event
- Staging timeline
- Situation changes
- Crash / explosion timeline
- Part loss events
- Basic “what killed the vessel?” report
- Simple flight path trail
- Basic replay ghost marker

### Launch Readiness Scanner

The readiness scanner automatically checks your craft on the launch pad or runway and warns about common problems before launch.

It can warn about:

- No parachutes
- No solar panels
- No batteries
- No antenna
- No control source
- No reaction wheels
- No landing legs or wheels
- No engines
- Engine staging issues
- Blocked or inactive engines
- Weird staging setup
- TWR too low
- TWR too high
- No heat shield for likely reentry craft

### Crew Tools

- View current vessel crew
- Edit courage
- Edit stupidity
- Jeb mode
- Randomized crew personality options

### World Tools

- Fake extra gravity
- Time scale controls
- Gravity presets
- Body information display

### Chaos Tools

- Random velocity events
- Vessel spin
- Chaos launch
- Random resource effects
- Random orbit nudges
- Timed chaos events
- Emergency resource refill
- Kraken-style experiment buttons

### Debug Tools

- Scene information
- Active vessel data
- Orbit data
- Active toggle dump
- Internal console log
- Copy debug summary

---

## Installation

1. Download the latest release `.zip`.
2. Unzip the downloaded file.
3. Open the unzipped folder.
4. Drag the included mod folder into your Kerbal Space Program `GameData` folder.
5. Launch Kerbal Space Program.
6. Load a save.
7. Press **F8** in-game to open the menu.

Your install should look like this:

```text
Kerbal Space Program/
└── GameData/
    └── JebediahsTotallySafeConsole/
        └── Plugins/
            └── JebediahsTotallySafeConsole.dll
```

Do **not** place only the `.dll` directly into `GameData`.

Use the full folder:

```text
GameData/JebediahsTotallySafeConsole/Plugins/JebediahsTotallySafeConsole.dll
```

---

## Controls

| Key | Action |
| --- | --- |
| `F8` | Open / close the menu |

---

## Recommended Use

This mod is best used for:

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
