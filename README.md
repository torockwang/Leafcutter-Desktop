# Leafcutter Desktop · 切叶蚁桌面漫游

切叶蚁把你的桌面当作叶片，探索、切割并搬运图像碎片。完成后播放烟花、显示统计，然后开始下一轮。

Leafcutter ants explore your desktop, cut out pieces of its image, and carry them away. Each completed round ends with fireworks and statistics before a new round begins.

## 下载 / Downloads

前往 [最新发行版 / Latest release](https://github.com/torock-netizen/Leafcutter-Desktop/releases/latest)，在 **Assets** 中选择安装包：

| Mac | 安装包 / Installer | 最低系统 / Minimum OS |
| --- | --- | --- |
| Apple Silicon (ARM64) | `Leafcutter-Desktop-1.4-Installer.pkg` | macOS 14 |
| Intel (x86_64) | `Leafcutter-Desktop-Mojave-1.4.1-Installer.pkg` | macOS 10.14 Mojave |

Intel 兼容版已在 Rosetta 环境验证，尚未在真实 Mojave 设备上验证。The Intel build has been tested under Rosetta, but not on actual Mojave hardware.

## 使用 / Usage

首次启动请按引导设置屏幕录制权限（系统需要时）。倒计时后开始运行；移动鼠标或按 Esc 退出。应用为手动启动的桌面模拟，不会自动启用系统闲置屏保。

Follow the first-launch guide to grant Screen Recording permission where required. The animation starts after a countdown. Move the mouse or press Esc to exit. This is a manually launched desktop animation; it does not enable an automatic idle screen saver.

## 当前签名状态 / Signing status

这两个版本尚未完成 Apple Developer ID 正式签名和公证。安装包未签名，内部应用采用临时签名，macOS 可能阻止安装或启动。需要正式签名版本的用户请等待后续发行版。

These builds are not Developer ID signed or notarized. The installer packages are unsigned and the apps use ad-hoc signatures. macOS may block installation or launch. Please wait for a later release if you require a signed and notarized build.

This repository distributes compiled installers and documentation only. Application source code is maintained separately.
