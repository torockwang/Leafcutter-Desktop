# Leafcutter Desktop

[简体中文](README.md) | **English**

Watch tiny ants carry your desktop away, one piece at a time.

Leafcutter Desktop freezes your current desktop into a giant “leaf.” Ants explore it, cut out pieces, lift them up, and carry them away. Each completed round ends with fireworks and statistics before a new round begins.

## What’s new in 1.7.4

- **Press M to mute, then press again to restore sound.** Available on Apple Silicon, Intel Mac and Windows. Holding the key toggles only once.
- Mute covers walking, cutting, carrying and cheering. The animation continues while you toggle audio. **Esc** and mouse movement still exit.
- **Windows installer reduced by about 83.5%**: from approximately 132.7 MB to **21.9 MB**, using a native host and shared WebView2. If WebView2 is missing, first-time installation requires internet to install this separate component.

[Full 1.7.4 release notes and all three installers](https://github.com/torockwang/Leafcutter-Desktop/releases/tag/v1.7.4)

## Download

Current versions: **macOS 1.7.4 (build 30) · Windows 1.7.4 Preview**.

| Your computer | Installer | System requirements |
| --- | --- | --- |
| Apple Silicon (M-series) | [Download Apple Silicon build](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7.4/Leafcutter-Desktop-1.7.4-Installer.pkg) | macOS 14 or later |
| Intel processor | [Download Intel compatibility build](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7.4/Leafcutter-Desktop-Intel-1.7.4-Installer.pkg) | Targets macOS 10.14 Mojave or later |
| Windows, Intel / AMD 64-bit | [Download Windows x64 Preview](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7.4/Leafcutter-Desktop-Windows-1.7.4-x64-Setup.exe) | Windows 10 1903+ / 11 (x64), .NET Framework 4.8 |

The Windows preview includes the local recovery model and stereo positioning. Version 1.7.4 uses a native Windows host and shared WebView2; the installer is approximately **21.9 MB**. If WebView2 is missing, the installer downloads Microsoft’s runtime, a separate shared dependency. Installation, media playback, rendered mute audio, cutting and desktop capture checks pass. Full-round and physical-GPU validation of the new native host remain pending.

[Windows 1.7.4 release notes](https://github.com/torockwang/Leafcutter-Desktop/releases/tag/v1.7.4) · [Windows SHA-256 checksum](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7.4/SHA256SUMS.txt)

Not sure which Mac processor you have? Open the Apple menu → About This Mac and look for Chip or Processor.

The Intel build targets Mojave compatibility. **It has not been tested on a physical Mojave system.**

[View the latest release](https://github.com/torockwang/Leafcutter-Desktop/releases/latest) · [Download SHA-256 checksums](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7.4/SHA256SUMS.txt)

## Install and use

**Windows:** Run the `.exe` installer. The default location is `%LOCALAPPDATA%\Programs\Leafcutter Desktop`. Launch from the Start menu or desktop shortcut, then start from the introduction page. Press **M** to mute/unmute; move the mouse or press Esc to exit. The app does not change system screen saver or lock settings. The installer is not Windows code-signed, so Windows may show an unknown-publisher warning.

**macOS:**

1. Download the `.pkg` installer for your Mac and follow the installation prompts.
2. The app installs into `/Applications/Leafcutter Desktop.app`. Its display name is “Leafcutter Desktop” on English systems and “切叶蚁模拟器” on Simplified Chinese systems.
3. On first launch, follow the guide to allow Screen Recording access. Mojave does not require this separate permission. The app restarts after authorization.
4. Read the creation story and browse the museum photos and silent video. Select “Don’t show this again” if you prefer. Click “Let the ants get to work” to begin the three-second countdown.
5. Press **M** to mute or restore audio. Move your mouse or press **Esc** during the show to exit. Each completed round displays fireworks, elapsed time, the total number of ants, and the number of pieces cut. Another round starts unless interrupted.

Closing the story or permission window cancels that launch. This is a manually launched desktop animation; it does not automatically enable the macOS idle screen saver.

## Retained 1.7 features

- Adds a small learned model for leaf-removal strategies. The bundled Tail v14 model assists with approach, pickup and recovery actions when ants stall, while preserving existing cutting, footing and traffic checks.
- Adds stereo positioning to walking, biting and carrying sounds, with smooth panning based on screen position.
- Fixes a cutting-arrival stall that prevented stance adjustments when some feet lacked support.
- Retains bilingual onboarding, photos, silent video, fireworks and statistics.

Known limitation: some regression scenarios still fail to finish and may stall during cleanup or traffic handling. This release does not include the full-round target-selection model currently in development, and does not guarantee stutter-free operation.

The small model is trained offline during development, bundled with all three builds and evaluated locally. The app does not train itself on users’ computers or upload desktop images.

## Privacy

Screen Recording access is used to capture the desktop image so the ants can cut and carry its pieces. The desktop image stays in memory and is never saved or uploaded.

## Signing status

The macOS installers are **not yet Apple Developer ID signed or notarized**. The packages are unsigned and the apps use ad-hoc signatures. macOS may block installation or launch. Please wait for a later release if you require a signed and notarized build.

## Feedback

Report problems in [Issues](https://github.com/torockwang/Leafcutter-Desktop/issues). Include the app version, operating system version, processor and GPU. Hide personal information on your desktop before sharing screenshots.

This repository distributes compiled installers and documentation only. Application source code is maintained separately.
