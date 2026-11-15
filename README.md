# Super Smash Bros. Melee (Dolphin) – true 16:9 widescreen

A Dolphin game-settings file that makes **Melee NTSC v1.02 (GALE01, revision 2)** render real 16:9 widescreen, with correct proportions (shields are round), instead of Dolphin's widescreen hack or a stretched 4:3 picture.

It uses the community **"16:9 Aspect Ratio Fix v1.02"** Gecko code by Dan Salvato, mirrorbender, Achilles1515 and UnclePunch (from the Dolphin wiki), plus the matching Dolphin video settings. I didn't write the code; this repo just packages the working setup.

## Why the custom aspect ratio

The code widens the game's camera from Melee's native 73:60 to 16:9. Dolphin's "Force 16:9" treats Melee's 640-pixel frame as 73:60 and adds side bars plus a slight squeeze, so the picture has to be **stretched to 16:9** instead (Aspect Ratio = Custom (Stretch), 16:9). Checked in game: shields measure round (217 x 218 px).

## Install

1. Download `MeleeWidescreen-v1.0.zip` from [Releases](https://github.com/Ma77i7yahu/melee-dolphin-widescreen/releases/latest) (or copy `ini/GALE01.ini` from this repo).
2. Find Dolphin's user folder (Dolphin: **File > Open User Folder**), then open `GameSettings`.
3. If there's no `GALE01.ini` there, copy this one in. If there is one, add this file's `[Gecko]`, `[Gecko_Enabled]` and `[Video_Settings]` sections to it (keep your other sections, such as `[Controls]`).
4. In Dolphin, make sure **Config > General > Enable Cheats** is ticked.
5. Start the game. In Melee's game properties you should see "16:9 Aspect Ratio Fix v1.02" ticked under Gecko Codes.

Turn off any other widescreen code (e.g. "Widescreen Support") and Dolphin's widescreen hack.

**Gotcha:** Dolphin strips the `[authors]` part from Gecko code names, so the `[Gecko_Enabled]` line must be exactly `$16:9 Aspect Ratio Fix v1.02`, without the bracketed names, or the code silently stays off.

## Known

- Training mode's on-screen overlay isn't covered by the code, so it stays stretched, and its normally hidden menu shows partly at the left edge.
- Tested with Dolphin 2609 on NTSC v1.02 only. Other regions/revisions need a different code.

## Disclaimer

Unofficial; not affiliated with Nintendo, HAL Laboratory or the Dolphin project. No game files are included.
