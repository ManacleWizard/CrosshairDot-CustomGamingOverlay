<p align="center">
  <img src="https://i.postimg.cc/C1NKFZhy/banner.png" alt="CrosshairDot Overlay — Lightweight Custom Screen Crosshair & PNG Reticle for Windows" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-Custom%20Crosshair%20Overlay-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-crosshair--dot--v1.3-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# CrosshairDot Overlay — Lightweight Custom Screen Crosshair & PNG Reticle for Windows

**Playing survival games, tactical shooters, or bow/hip-fire titles with no center reticle—or stuck with a giant blurry in-game crosshair? Overlay a razor-sharp, click-through Dot, Cross, Circle, or custom PNG reticle at exact screen center with one hotkey.**

CrosshairDot Overlay renders a hardware-composited `WS_EX_TRANSPARENT` click-through reticle above Borderless Windowed games: **supporting customizable thickness, gap, length, 1px dark contrast outline, custom `.png` reticles, and instant hotkey toggling with under 10 MB RAM**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) PC gamers** playing in Borderless Windowed or Windowed mode who want a clean visual center-screen reticle.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| Survival or tactical game hides reticle during hip-fire or bow draw | Games omit center dots or use dynamic bloom circles | Display a crisp `2px–4px` **Center Dot** or **Static Cross** on screen |
| Bright snow/sky backgrounds wash out thin colored crosshairs | Unoutlined crosshairs disappear against bright environments | Enable **1px Black Contrast Outline** for visibility on any background |
| Built-in monitor hardware crosshairs look chunky and off-center | Monitor OSD crosshairs use low-res sprites with no sub-pixel tuning | Use **1px X/Y Nudge Arrows** to align with exact game bullet/arrow center |
| Need to hide the crosshair quickly during cutscenes or inventory | Alt-tabbing to close an overlay interrupts gameplay | Press global hotkey (`Ctrl+Alt+X`) to toggle visibility instantaneously |

## Download for Windows

[**Download CrosshairDot.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/CrosshairDot.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `CrosshairDot.exe`? (Key features)

- Built-in parametric shapes: **Center Dot**, **Classic Cross**, **T-Shape**, **Circle Ring**, plus custom **Transparent PNG** import.
- Full customization: size, thickness, center gap, color (`HEX`/RGB picker), opacity, and **1px Black Outline**.
- Sub-pixel **X / Y Offset Nudge** (`±1 px`) and multi-monitor selector.
- 100% external click-through overlay—zero game DLL injection and instant `Ctrl+Alt+X` toggle.

### Sample Output

```text
[CrosshairDot] Overlay Active on Monitor [1] (2560x1440 | Center: 1280, 720)
[OK]   Reticle Style    : Center Dot (Size: 4px | Color: #84E041 | 1px Black Outline)
[OK]   Window Flags     : WS_EX_TOPMOST | WS_EX_TRANSPARENT (Click-Through, 0 DLL hooks)
[INFO] Toggle Hotkey    : Press Ctrl+Alt+X to show/hide anytime
```

The release ZIP is named `CrosshairDot.zip`; the Windows executable inside is named `CrosshairDot.exe`.

1. Close CrosshairDot before updating or replacing executable files.
2. Click **Download CrosshairDot.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `CrosshairDot.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit).

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `CrosshairDot.exe` runs locally without uploading your personal files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Razor-sharp visibility on both dark caves and bright skies

Automatic 1px dark outline keeps neon green/cyan reticles legible in every scene.

### Zero game file modification or memory injection

Renders purely as a standard click-through Windows layered window.

### Custom PNG reticle support

Load any transparent `.png` scope or custom reticle sprite.

### Saveable per-game reticle presets

Switch between a tiny 2px rifle dot and a bow rangefinder reticle in one click.

## Default folders and configuration paths

CrosshairDot stores saved reticle presets and custom PNGs in `%APPDATA%\CrosshairDot`:

```text
%APPDATA%\CrosshairDot\presets.json
```

Typical directory layout:

```text
%APPDATA%\CrosshairDot\
├── presets.json
└── custom_png\
    └── reticle_dot.png
```

Run games in **Borderless Windowed** mode so external overlays render cleanly on top of the game frame.

## Quick start guide

Follow these steps to get started:

1. **Extract `CrosshairDot.zip` and launch `CrosshairDot.exe`.** Select your primary gaming monitor.
2. **Pick a shape (**Dot**, **Cross**, **Circle**, or **Custom PNG**) and color.** Enable **1px Black Outline** for maximum contrast.
3. **Launch your game in Borderless Windowed mode.** Use `Ctrl+Alt+X` anytime to toggle the crosshair on or off.

### Data safety note

CrosshairDot never injects into game executables or alters game files.

## What the status summary shows

CrosshairDot displays **target monitor resolution, exact center coordinates, active reticle preset, and toggle hotkey**.

## FAQ

**Is CrosshairDot safe to use on Windows?**

Yes—it is a pure external click-through overlay window (similar to monitor built-in crosshairs) and does not touch game files or memory.

**Why isn't the crosshair visible in my game?**

Make sure your game is set to **Borderless Windowed** (not Exclusive Fullscreen), as Windows only draws desktop overlays over windowed/borderless surfaces.

**Can I import my own PNG crosshair image?**

Yes—click 'Load Custom PNG' to use any transparent PNG reticle.

## Useful reading

- [Microsoft Docs — Layered Windows (WS_EX_TRANSPARENT)](https://learn.microsoft.com/en-us/windows/win32/winmsg/window-features#layered-windows)

## More Windows Gaming Utilities

- [MiniHUD-LightweightFPSOverlay](../MiniHUD-LightweightFPSOverlay) — Compact borderless FPS, frametime & GPU temp overlay
- [BorderlessForce-WindowScaler](../BorderlessForce-WindowScaler) — Force borderless windowed fullscreen & dual-monitor cursor lock
- [PinTop-WindowAlwaysOnTop](../PinTop-WindowAlwaysOnTop) — Pin any window Always-on-Top & adjust transparency on Windows
- [PadDrift-ControllerPollingTest](../PadDrift-ControllerPollingTest) — Gamepad stick drift & mouse polling rate (1000-8000 Hz) tester

*Independent open-source desktop utility for Windows.*
