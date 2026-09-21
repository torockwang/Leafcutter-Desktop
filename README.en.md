# Leafcutter Desktop

[简体中文](README.md) | **English**

Watch tiny ants carry your desktop away, one piece at a time.

Leafcutter Desktop freezes your current desktop into a giant “leaf.” Ants explore it, cut out pieces, lift them up, and carry them away. Each completed round ends with fireworks and statistics before a new round begins.

## Download

Current versions: **macOS 1.7 (build 29) · Windows 1.7.2 Preview**.

| Your computer | Installer | System requirements |
| --- | --- | --- |
| Apple Silicon (M-series) | [Download Apple Silicon build](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7/Leafcutter-Desktop-1.7-Installer.pkg) | macOS 14 or later |
| Intel processor | [Download Intel compatibility build](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7/Leafcutter-Desktop-Intel-1.7-Installer.pkg) | Targets macOS 10.14 Mojave or later |
| Windows, Intel / AMD 64-bit | [Download Windows x64 Preview](https://github.com/torockwang/Leafcutter-Desktop/releases/download/windows-v1.7.2/Leafcutter-Desktop-Windows-1.7.2-x64-Setup.exe) | Windows 10 / 11 (x64) |

The Windows preview includes the local recovery model and stereo positioning. One full round passed in a Windows 11 VM. Physical Intel/AMD PCs and Windows 10 still need full validation; stutter or stalls remain possible.

[Windows 1.7.2 release notes](https://github.com/torockwang/Leafcutter-Desktop/releases/tag/windows-v1.7.2) · [Windows SHA-256 checksum](https://github.com/torockwang/Leafcutter-Desktop/releases/download/windows-v1.7.2/SHA256SUMS-Windows-1.7.2.txt)

Not sure which Mac processor you have? Open the Apple menu → About This Mac and look for Chip or Processor.

The Intel build targets Mojave compatibility. **It has not been tested on a physical Mojave system.**

[View the latest release](https://github.com/torockwang/Leafcutter-Desktop/releases/latest) · [Download SHA-256 checksums](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7/SHA256SUMS.txt)

## Install and use

**Windows:** Run the `.exe` installer. The default location is `%LOCALAPPDATA%\Programs\Leafcutter Desktop`. Launch from the Start menu or desktop shortcut, then start from the introduction page. Move the mouse or press Esc to exit. The app does not change system screen saver or lock settings. The installer is not Windows code-signed, so Windows may show an unknown-publisher warning.

**macOS:**

1. Download the `.pkg` installer for your Mac and follow the installation prompts.
2. The app installs into `/Applications/Leafcutter Desktop.app`. Its display name is “Leafcutter Desktop” on English systems and “切叶蚁模拟器” on Simplified Chinese systems.
3. On first launch, follow the guide to allow Screen Recording access. Mojave does not require this separate permission. The app restarts after authorization.
4. Read the creation story and browse the museum photos and silent video. Select “Don’t show this again” if you prefer. Click “Let the ants get to work” to begin the three-second countdown.
5. Move your mouse or press **Esc** during the show to exit. Each completed round displays fireworks, elapsed time, the total number of ants, and the number of pieces cut. Another round starts unless interrupted.

Closing the story or permission window cancels that launch. This is a manually launched desktop animation; it does not automatically enable the macOS idle screen saver.

## What’s new in 1.7

- Adds a small learned model for leaf-removal strategies. The bundled Tail v14 model assists with approach, pickup and recovery actions when ants stall, while preserving existing cutting, footing and traffic checks.
- Adds stereo positioning to walking, biting and carrying sounds, with smooth panning based on screen position.
- Fixes a cutting-arrival stall that prevented stance adjustments when some feet lacked support.
- Retains bilingual onboarding, photos, silent video, fireworks and statistics.

Known limitation: some regression scenarios still fail to finish and may stall during cleanup or traffic handling. This release does not include the full-round target-selection model currently in development, and does not guarantee stutter-free operation.

The small model is trained offline during development, bundled with both builds and evaluated locally. The app does not train itself on users’ computers or upload desktop images.

## Privacy

Screen Recording access is used to capture the desktop image so the ants can cut and carry its pieces. The desktop image stays in memory and is never saved or uploaded.

## Signing status

The macOS installers are **not yet Apple Developer ID signed or notarized**. The packages are unsigned and the apps use ad-hoc signatures. macOS may block installation or launch. Please wait for a later release if you require a signed and notarized build.

## Feedback

Report problems in [Issues](https://github.com/torockwang/Leafcutter-Desktop/issues). Include the app version, operating system version, processor and GPU. Hide personal information on your desktop before sharing screenshots.

This repository distributes compiled installers and documentation only. Application source code is maintained separately.
