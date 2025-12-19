---
title: "DroidDock：在 macOS 上浏览 Android 文件的轻量级 ADB 文件管理器 - A姐分享"
source: "https://www.ahhhhfs.com/77508/"
author:
  - "[[ahhhhfs]]"
published: 2025-11-15
created: 2025-12-08
description: "DroidDock 是一款原生风格的 macOS ADB 文件管理器，支持多设备自动识别、网格/列表/分栏视图、缩略图、搜索、上传下载、批量删除、暗黑模式与自动更新，让你在 Mac 上高效管理 Android 文件。"
tags:
  - "clippings"
---
## DroidDock概览

DroidDock 是一款专为 macOS 打造的 ADB（Android Debug Bridge）文件管理工具。连接设备后即可在 Mac 上直观浏览 Android 文件系统，完成搜索、预览、上传、下载与删除等操作。界面简洁、响应迅速，满足创作者与开发者的日常文件处理需求。

[![DroidDock：在 macOS 上浏览 Android 文件的轻量级 ADB 文件管理器](https://www.ahhhhfs.com/wp-content/uploads/2025/11/DroidDock%EF%BC%9A%E5%9C%A8-macOS-%E4%B8%8A%E6%B5%8F%E8%A7%88-Android-%E6%96%87%E4%BB%B6%E7%9A%84%E8%BD%BB%E9%87%8F%E7%BA%A7-ADB-%E6%96%87%E4%BB%B6%E7%AE%A1%E7%90%86%E5%99%A8.jpg "DroidDock：在 macOS 上浏览 Android 文件的轻量级 ADB 文件管理器 1")](https://www.ahhhhfs.com/wp-content/uploads/2025/11/DroidDock%EF%BC%9A%E5%9C%A8-macOS-%E4%B8%8A%E6%B5%8F%E8%A7%88-Android-%E6%96%87%E4%BB%B6%E7%9A%84%E8%BD%BB%E9%87%8F%E7%BA%A7-ADB-%E6%96%87%E4%BB%B6%E7%AE%A1%E7%90%86%E5%99%A8.jpg)

## 关键亮点

- **即插即用的设备识别** ：自动检测已连接的 Android 设备。
- **直观文件浏览** ：支持表格、网格、列表、分栏（Miller）等多种视图与快捷键切换。
- **高效文件操作** ：上传/下载一键完成，支持多选、勾选框、Ctrl/Cmd 与 Shift 范围选择。
- **智能预览** ：图片/视频自动缩略图与懒加载。
- **安全删除** ：删除前弹出确认对话框，并阻止关键系统目录误删。
- **精准搜索** ：名称不区分大小写，可递归子目录，结果展示完整路径。
- **信息面板** ：快速查看权限、大小、修改时间与设备存储占用。
- **便捷导航** ：“内部存储”标签与面包屑路径，清晰回溯。
- **暗黑模式** ：原生质感的深色主题，长时间操作更舒适。
- **ADB 智能检测** ：自动在常见路径查找 ADB，亦可自定义路径。
- **版本更新** ：启动时检查更新并提醒。

## 截图界面

[![DroidDock：在 macOS 上浏览 Android 文件的轻量级 ADB 文件管理器](https://www.ahhhhfs.com/wp-content/uploads/2025/11/DroidDock%EF%BC%9A%E5%9C%A8-macOS-%E4%B8%8A%E6%B5%8F%E8%A7%88-Android-%E6%96%87%E4%BB%B6%E7%9A%84%E8%BD%BB%E9%87%8F%E7%BA%A7-ADB-%E6%96%87%E4%BB%B6%E7%AE%A1%E7%90%86%E5%99%A8-grid-view.jpg "DroidDock：在 macOS 上浏览 Android 文件的轻量级 ADB 文件管理器 2")](https://www.ahhhhfs.com/wp-content/uploads/2025/11/DroidDock%EF%BC%9A%E5%9C%A8-macOS-%E4%B8%8A%E6%B5%8F%E8%A7%88-Android-%E6%96%87%E4%BB%B6%E7%9A%84%E8%BD%BB%E9%87%8F%E7%BA%A7-ADB-%E6%96%87%E4%BB%B6%E7%AE%A1%E7%90%86%E5%99%A8-grid-view.jpg) [![DroidDock：在 macOS 上浏览 Android 文件的轻量级 ADB 文件管理器](https://www.ahhhhfs.com/77508/www.w3.org/2000/svg'%20viewBox='0%200%202224%201624'%3E%3C/svg%3E "DroidDock：在 macOS 上浏览 Android 文件的轻量级 ADB 文件管理器 3")](https://www.ahhhhfs.com/wp-content/uploads/2025/11/DroidDock%EF%BC%9A%E5%9C%A8-macOS-%E4%B8%8A%E6%B5%8F%E8%A7%88-Android-%E6%96%87%E4%BB%B6%E7%9A%84%E8%BD%BB%E9%87%8F%E7%BA%A7-ADB-%E6%96%87%E4%BB%B6%E7%AE%A1%E7%90%86%E5%99%A8-main-interface.jpg)

## 安装与启动

### 方式一：下载预构建应用（推荐）

1. 下载最新的 `.dmg` 安装包（官网或 Releases 页面）。
2. 双击打开 DMG，将 **DroidDock** 拖入 **Applications** 。
3. 首次启动因未签名需 **右键 → Open** 并在安全对话框中选择 **Open** 。
4. 连接启用 USB 调试的 Android 设备后即可使用。

> 安全说明：当前版本未签名，macOS 会在首次启动显示安全提示。后续版本计划提供代码签名。

### 方式二：从源码构建（开发者）

```bash
git clone https://github.com/rajivm1991/DroidDock.git
cd droiddock
npm install
# 开发调试
npm run tauri dev
# 生产构建
npm run tauri build
# 产物位置：src-tauri/target/release/bundle/
```

## 运行前提

- **ADB** （Android Platform Tools）
	- Homebrew 安装： `brew install android-platform-tools`
	- 典型路径自动检测：
		- `/opt/homebrew/bin/adb` （Apple Silicon Homebrew）
		- `/usr/local/bin/adb` （Intel Mac Homebrew）
		- `/opt/local/bin/adb` （MacPorts）
		- `~/Library/Android/sdk/platform-tools/adb` （Android Studio）
- **启用 USB 调试的 Android 设备与数据线**
- （开发者） **Node.js** 20.19+/22.12+、 **Rust** （通过 `rustup.rs` 安装）

## 基本用法

1. 在 Android 设备 **设置 → 关于手机** 连续点击 **版本号** 以启用开发者选项，再在 **开发者选项** 中打开 **USB 调试** ，用数据线连接 Mac。
2. 终端执行 `adb devices` ，确认设备已被识别。
3. 打开 DroidDock，选择设备，即可从 `/storage/emulated/0` 开始浏览。
4. 通过视图切换按钮或 `Cmd+1/2/3/4` 在表格、网格、列表、分栏之间切换。
5. 在设置中切换 **显示隐藏文件** 与 **缩略图** ；使用 **搜索栏** 支持递归检索；勾选文件后出现底部操作栏，可 **下载** 或 **删除** 。

## 系统与兼容

- **平台** ：macOS 10.13（High Sierra）及以上
- **架构** ：Apple Silicon（M1/M2/M3）与 Intel
- **空间** ：≈50 MB 可用磁盘空间

## 适合人群

- 需要在 Mac 与 Android 间频繁传输素材的内容创作者、摄影/短视频团队。
- 依赖 ADB 进行测试与拉取日志的移动开发与测试工程师。
- 希望替代命令行 ADB 操作、追求更直观文件管理体验的用户。

## 技术栈

- 前端：React + TypeScript + Vite
- 后端：Rust + Tauri
- 样式：自定义 CSS（原生暗黑模式支持）

## 下载与源码

下载地址： [网盘](https://pan.quark.cn/s/4c9a2c6562b0)

官网： [`https://rajivm1991.github.io/DroidDock/`](https://rajivm1991.github.io/DroidDock/ "https://rajivm1991.github.io/DroidDock/")

GitHub： [`https://github.com/rajivm1991/DroidDock`](https://github.com/rajivm1991/DroidDock "https://github.com/rajivm1991/DroidDock")

本文链接： [https://www.ahhhhfs.com/77508/](https://www.ahhhhfs.com/77508/ "DroidDock：在 macOS 上浏览 Android 文件的轻量级 ADB 文件管理器")

1. 转载请保留原文链接谢谢！
- 本站所有资源文章出自互联网收集整理，本站不参与制作，如果侵犯了您的合法权益，请联系本站我们会及时删除。
- 本站发布资源来源于互联网，可能存在水印或者引流等信息，请用户擦亮眼睛自行鉴别，做一个有主见和判断力的用户。
- 本站资源仅供研究、学习交流之用，若使用商业用途，请购买正版授权，否则产生的一切后果将由下载用户自行承担。
- 联系方式（#替换成@）：feedback#abskoop.com[上一篇

实体强效率方法：AI批量产出获客文案，2025年普通人拥抱AI，实现实体创收

](https://www.ahhhhfs.com/77501/ "实体强效率方法：AI批量产出获客文案，2025年普通人拥抱AI，实现实体创收")[下一篇

AICoding基地：AI编程工具导航与开发者资讯聚合平台

](https://www.ahhhhfs.com/77515/ "AICoding基地：AI编程工具导航与开发者资讯聚合平台")