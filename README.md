# 切叶蚁模拟器

**简体中文** | [English](README.en.md)

看小小蚂蚁，一片片搬走你的桌面。

切叶蚁模拟器（Leafcutter Desktop）把当前桌面定格成一整片“叶子”。蚂蚁会探索、切割，并把图像碎片举起来搬走。完成一轮后，烟花和统计数据会庆祝它们的工作，然后开始下一轮。

## 下载

当前版本：**1.5.7（构建号 27）**。

| 你的 Mac | 安装包 | 系统要求 |
| --- | --- | --- |
| Apple 芯片（M 系列） | [下载 Apple 芯片版](https://github.com/torock-netizen/Leafcutter-Desktop/releases/download/v1.5.7/Leafcutter-Desktop-1.5.7-Installer.pkg) | macOS 14 或更新版本 |
| Intel 处理器 | [下载 Intel 兼容版](https://github.com/torock-netizen/Leafcutter-Desktop/releases/download/v1.5.7/Leafcutter-Desktop-Intel-1.5.7-Installer.pkg) | 目标兼容 macOS 10.14 Mojave 或更新版本 |

不确定处理器类型？打开苹果菜单 → “关于本机”，查看“芯片”或“处理器”。

Intel 版已在 Apple 芯片 Mac 的 Rosetta 环境下通过启动及视频播放检查，**尚未在 Mojave 实机上验证**。

[查看最新发行版](https://github.com/torock-netizen/Leafcutter-Desktop/releases/latest) · [下载 SHA-256 校验值](https://github.com/torock-netizen/Leafcutter-Desktop/releases/download/v1.5.7/SHA256SUMS.txt)

## 安装与使用

1. 下载适合你的 Mac 的 `.pkg` 安装包，按提示安装。
2. 应用安装到 `/Applications/Leafcutter Desktop.app`。中文系统显示“切叶蚁模拟器”，英文系统显示“Leafcutter Desktop”。
3. 首次运行时，按引导允许屏幕录制权限；Mojave 无需单独设置这项权限。授权后应用会重新启动。
4. 阅读创作故事，浏览参观照片和静音视频。可以勾选“下次不再显示”。点击“让蚂蚁开工”进入三秒倒计时。
5. 演示中移动鼠标或按 **Esc** 即可退出。每轮完成后会展示烟花、总时长、蚂蚁总数和切片数量，未被打断则进入下一轮。

关闭介绍或权限窗口会取消本次启动。应用是手动启动的桌面演示，不会自动启用 macOS 的闲置屏幕保护程序。

## 1.5.7 更新

- 中英文权限引导、创作故事和独立鸣谢页。
- 博物馆参观照片与压缩后的静音视频。
- 修复视频加载及播放问题。
- 已授权启动不再闪现权限引导；关闭窗口后取消待启动的倒计时。
- 中文应用名称“切叶蚁模拟器”，两个版本均安装到标准“应用程序”目录。

## 隐私

屏幕录制权限用于取得桌面图像，让蚂蚁切割和搬运图像碎片。桌面图像仅在内存中使用，不保存、不上传。

## 签名状态

当前安装包**尚未完成 Apple Developer ID 签名和公证**。安装包未签名，内部应用采用临时签名，macOS 可能阻止安装或启动。如需正式签名和公证的版本，请等待后续发行版。

## 反馈

请在 [Issues](https://github.com/torock-netizen/Leafcutter-Desktop/issues) 中反馈问题，注明应用版本、macOS 版本和 Mac 处理器类型。截图前请遮挡桌面上的个人信息。

本仓库仅提供编译后的安装包和使用说明，应用源码单独维护。
