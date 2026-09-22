# 切叶蚁模拟器

**简体中文** | [English](README.en.md)

看小小蚂蚁，一片片搬走你的桌面。

切叶蚁模拟器（Leafcutter Desktop）把当前桌面定格成一整片“叶子”。蚂蚁会探索、切割，并把图像碎片举起来搬走。完成一轮后，烟花和统计数据会庆祝它们的工作，然后开始下一轮。

## 下载

当前版本：**macOS 1.7.4（构建号 30） · Windows 1.7.4 预览版**。

| 你的电脑 | 安装包 | 系统要求 |
| --- | --- | --- |
| Apple 芯片（M 系列） | [下载 Apple 芯片版](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7.4/Leafcutter-Desktop-1.7.4-Installer.pkg) | macOS 14 或更新版本 |
| Intel 处理器 | [下载 Intel 兼容版](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7.4/Leafcutter-Desktop-Intel-1.7.4-Installer.pkg) | 目标兼容 macOS 10.14 Mojave 或更新版本 |
| Windows，Intel / AMD 64 位 | [下载 Windows x64 预览版](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7.4/Leafcutter-Desktop-Windows-1.7.4-x64-Setup.exe) | Windows 10 1903+ / 11（x64），.NET Framework 4.8 |

Windows 版包含本地小模型和立体声摆位。1.7.4 使用原生 Windows 外壳与共享 WebView2，安装包约 **21.9 MB**。系统缺少 WebView2 时，安装程序会联网安装微软提供的运行时；该共享组件不计入本安装包体积。新版通过安装、媒体播放、静音音频采样、切割与桌面捕捉检查，尚未完成原生外壳的整局及实体显卡性能验收。

[Windows 1.7.4 发布说明](https://github.com/torockwang/Leafcutter-Desktop/releases/tag/v1.7.4) · [Windows SHA-256 校验值](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7.4/SHA256SUMS.txt)

不确定 Mac 处理器类型？打开苹果菜单 → “关于本机”，查看“芯片”或“处理器”。

Intel 版目标兼容 Mojave，**尚未在 Mojave 实机上验证**。

[查看最新发行版](https://github.com/torockwang/Leafcutter-Desktop/releases/latest) · [下载 SHA-256 校验值](https://github.com/torockwang/Leafcutter-Desktop/releases/download/v1.7.4/SHA256SUMS.txt)

## 安装与使用

**Windows：**运行 `.exe` 安装包，默认安装到 `%LOCALAPPDATA%\Programs\Leafcutter Desktop`。从开始菜单或桌面快捷方式启动，在介绍页点击开始，倒计时后演示。按 **M** 静音，再按一次恢复；移动鼠标或按 Esc 退出。程序不会自动修改系统屏保或锁屏设置。安装包尚未进行 Windows 代码签名，系统可能提示未知发布者。

**macOS：**

1. 下载适合你的 Mac 的 `.pkg` 安装包，按提示安装。
2. 应用安装到 `/Applications/Leafcutter Desktop.app`。中文系统显示“切叶蚁模拟器”，英文系统显示“Leafcutter Desktop”。
3. 首次运行时，按引导允许屏幕录制权限；Mojave 无需单独设置这项权限。授权后应用会重新启动。
4. 阅读创作故事，浏览参观照片和静音视频。可以勾选“下次不再显示”。点击“让蚂蚁开工”进入三秒倒计时。
5. 演示中按 **M** 静音，再按一次恢复。移动鼠标或按 **Esc** 即可退出。每轮完成后会展示烟花、总时长、蚂蚁总数和切片数量，未被打断则进入下一轮。

关闭介绍或权限窗口会取消本次启动。应用是手动启动的桌面演示，不会自动启用 macOS 的闲置屏幕保护程序。

## 1.7.4 更新

- 三个平台均增加 **M 键静音切换**，长按只切换一次，原有退出操作保持不变。
- Windows 改用原生外壳与共享 WebView2，安装包从约 132.7 MB 缩小至 21.9 MB。
- 沿用 1.7 的行为规则与小模型，本次没有加入实验中的全程选点策略。

## 沿用的 1.7 功能

- 增加小模型学习叶片切除策略：内置 Tail v14 模型，在停滞时辅助选择接近、夹取和恢复动作，保留现有切割、站位与交通检查。
- 增加蚂蚁音效的立体声摆位：行走、咬叶和搬运声音随蚂蚁的屏幕位置平滑变化。
- 修复到达切割位置后，部分足部缺少支撑时无法调整站位的问题。
- 保留中英文引导、照片、静音视频、烟花与统计。

已知限制：回归验证中仍有部分场景未能完成，可能出现收尾或交通停滞。此版本不包含正在开发的全程选点模型，不保证消除所有卡顿。

小模型在开发期间离线训练，三个版本均随包提供并在本地运行；不会在用户电脑上自行训练，也不会上传桌面图像。

## 隐私

屏幕录制权限用于取得桌面图像，让蚂蚁切割和搬运图像碎片。桌面图像仅在内存中使用，不保存、不上传。

## 签名状态

macOS 安装包**尚未完成 Apple Developer ID 签名和公证**。安装包未签名，内部应用采用临时签名，macOS 可能阻止安装或启动。如需正式签名和公证的版本，请等待后续发行版。

## 反馈

请在 [Issues](https://github.com/torockwang/Leafcutter-Desktop/issues) 中反馈问题，注明应用版本、操作系统版本、处理器和显卡类型。截图前请遮挡桌面上的个人信息。

本仓库仅提供编译后的安装包和使用说明，应用源码单独维护。
