# Leafcutter Desktop

[简体中文](README.md) | **English**

Watch tiny ants carry your desktop away, one piece at a time.

Leafcutter Desktop freezes your current desktop into a giant “leaf.” Ants explore it, cut out pieces, lift them up, and carry them away. Each completed round ends with fireworks and statistics before a new round begins.

## Download

Current version: **1.6 (build 28)**.

| Your Mac | Installer | System requirements |
| --- | --- | --- |
| Apple Silicon (M-series) | [Download Apple Silicon build](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.6/Leafcutter-Desktop-1.6-Installer.pkg) | macOS 14 or later |
| Intel processor | [Download Intel compatibility build](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.6/Leafcutter-Desktop-Intel-1.6-Installer.pkg) | Targets macOS 10.14 Mojave or later |

Not sure which processor you have? Open the Apple menu → About This Mac and look for Chip or Processor.

The Intel build passed startup and video playback checks under Rosetta on an Apple Silicon Mac. **It has not been tested on a physical Mojave system.**

[View the latest release](https://github.com/torockwang/Leafcutter-Desktop/releases/latest) · [Download SHA-256 checksums](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.6/SHA256SUMS.txt)

## Install and use

1. Download the `.pkg` installer for your Mac and follow the installation prompts.
2. The app installs into `/Applications/Leafcutter Desktop.app`. Its display name is “Leafcutter Desktop” on English systems and “切叶蚁模拟器” on Simplified Chinese systems.
3. On first launch, follow the guide to allow Screen Recording access. Mojave does not require this separate permission. The app restarts after authorization.
4. Read the creation story and browse the museum photos and silent video. Select “Don’t show this again” if you prefer. Click “Let the ants get to work” to begin the three-second countdown.
5. Move your mouse or press **Esc** during the show to exit. Each completed round displays fireworks, elapsed time, the total number of ants, and the number of pieces cut. Another round starts unless interrupted.

Closing the story or permission window cancels that launch. This is a manually launched desktop animation; it does not automatically enable the macOS idle screen saver.

## What’s new in 1.6

- Reuses leaf-surface and route checks to reduce repeated geometry work.
- Compacts grid adjacency caches and reuses Metal geometry and compute buffers.
- Prepares carrying audio and adapts rendering cadence to the display refresh rate.
- Preserves cutting and traffic rules; no machine-learning model is included.
- Retains bilingual onboarding, photos, silent video, fireworks, and statistics, with installation into the standard Applications folder.

This release improves performance but does not claim to eliminate all stutter; occasional scene-update spikes remain under investigation.

## Privacy

Screen Recording access is used to capture the desktop image so the ants can cut and carry its pieces. The desktop image stays in memory and is never saved or uploaded.

## Signing status

These installers are **not yet Apple Developer ID signed or notarized**. The packages are unsigned and the apps use ad-hoc signatures. macOS may block installation or launch. Please wait for a later release if you require a signed and notarized build.

## Feedback

Report problems in [Issues](https://github.com/torockwang/Leafcutter-Desktop/issues). Include the app version, macOS version, and Mac processor type. Hide personal information on your desktop before sharing screenshots.

This repository distributes compiled installers and documentation only. Application source code is maintained separately.
