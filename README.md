<div align="center">

# ⚛️ Nuke

### 为 QQ · 微信 · 抖音增添更多可能

**Android Xposed 模块 · 多宿主扩展 · Root / 免 Root**

[![Android](https://img.shields.io/badge/Android-8.1%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white)](#-开始使用) ![Architecture](https://img.shields.io/badge/ARCH-ARM64-8B5CF6?style=for-the-badge) ![Closed source](https://img.shields.io/badge/SOURCE-CLOSED-334155?style=for-the-badge)

[![Stars](https://img.shields.io/github/stars/dartcv/Nuke?style=flat-square&logo=github&label=Stars&color=f59e0b)](https://github.com/dartcv/Nuke/stargazers) [![Downloads](https://img.shields.io/badge/Downloads-pending%20release-64748b?style=flat-square&logo=github)](https://github.com/dartcv/Nuke/releases) [![Script docs](https://img.shields.io/badge/Docs-Script%20API-0ea5e9?style=flat-square&logo=readthedocs&logoColor=white)](https://github.com/NukeDevelopers/NukeJsDocs)

**[📦 发布页面](https://github.com/dartcv/Nuke/releases) · [✨ 功能概览](#-功能概览) · [🧩 框架支持](#-框架支持) · [🚀 开始使用](#-开始使用) · [📚 脚本文档](#-脚本文档)**

</div>

<!-- 首次发布带附件的 Release 后，可将上方 Downloads 徽章替换为：
[![Downloads](https://img.shields.io/github/downloads/dartcv/Nuke/total?style=flat-square&logo=github&label=Downloads&color=22c55e)](https://github.com/dartcv/Nuke/releases)
-->

---

**Nuke 是一个支持 QQ、微信和抖音的 Android Xposed 模块**，提供宿主内功能扩展、界面定制与使用体验优化。

支持 **Vector、LSPosed 等 Root 框架**，以及 **NPatch、FPA、LSPatch 等免 Root 注入框架**。

> [!IMPORTANT]
> **Nuke 为闭源项目。** 本仓库仅用于项目介绍，不公开项目源代码。

## 🎯 支持的应用

| 应用 | 包名 | 当前支持情况 |
| --- | --- | --- |
| 微信 | `com.tencent.mm` | 当前主要支持平台，提供设置入口、聊天与朋友圈菜单扩展、界面定制等功能 |
| QQ | `com.tencent.mobileqq` | 已接入模块加载与菜单入口，功能持续完善中 |
| 抖音 | `com.ss.android.ugc.aweme` | 提供设置入口、推荐流过滤与基础体验优化功能 |

三个平台的功能覆盖程度不同，具体可用功能以当前版本的宿主内设置界面为准。

## ✨ 功能概览

### 💬 微信

- 在微信设置页加入 Nuke 入口。
- 扩展聊天消息与朋友圈的长按菜单。
- 强制启用平板模式。
- 支持圆形头像、聊天头像旋转与旋转周期设置。

### 🐧 QQ

- 支持在 QQ 中加载 Nuke，并提供菜单入口。
- 后续功能与适配持续完善。

### 🎬 抖音

- 在抖音设置页加入 Nuke 入口。
- 过滤推荐流中的直播与广告。
- 屏蔽更新检查。
- 保持高画质模式。
- 隐藏青少年模式弹窗。

### 🎨 通用能力

- 在宿主内启用、停用和配置各项功能。
- 支持浅色、深色主题及自定义主题色。
- 提供简体中文、繁体中文和英文界面。
- 提供功能状态、异常记录与宿主重启等辅助能力。
- 提供脚本扩展能力，方便按需扩展宿主功能。

## 🧩 框架支持

| 使用方式 | 支持的框架 |
| --- | --- |
| Root 环境 | Vector、LSPosed 等兼容 Xposed 的框架 |
| 免 Root 环境 | NPatch、FPA、LSPatch 等注入框架 |

实际可用性取决于 Android 版本、宿主版本和所使用框架的兼容情况。支持某个框架不代表所有宿主版本或所有功能均可正常使用。

## 🚀 开始使用

运行环境为 **Android 8.1 及以上、ARM64 设备**。

<details open>
<summary><strong>🔓 Root 环境 · Vector / LSPosed</strong></summary>


1. 安装 Nuke。
2. 在 Vector、LSPosed 等框架中启用模块。
3. 将需要使用的 QQ、微信或抖音加入模块作用域。
4. 强制停止目标应用并重新打开。
5. 从宿主内的 Nuke 入口进入设置，开启所需功能。

</details>

<details>
<summary><strong>📱 免 Root 环境 · NPatch / FPA / LSPatch</strong></summary>


1. 准备 Nuke 安装包与目标应用安装包。
2. 按 NPatch、FPA 或 LSPatch 对应的操作流程，将 Nuke 注入目标应用。
3. 安装并启动完成注入的应用。
4. 从宿主内的 Nuke 入口进入设置，开启所需功能。

</details>

> [!TIP]
> 微信和抖音首次加载时，部分功能需要先完成 Dex 分析。分析完成后应用可能退出或重启，再次打开即可继续使用。独立的 Nuke App 可用于查看模块状态和使用引导。

## 🔎 兼容性说明

> [!NOTE]
> 项目持续开发中。QQ、微信和抖音更新后，部分功能可能需要重新适配。不同平台的功能覆盖程度不同，以当前版本的宿主内设置界面为准。

## ❓ 常见问题

### 出现 `Dex分析失败：NameNotFoundException`

请调整 **Hide My Applist** 配置，使其不对微信隐藏 **Nuke**，随后重启微信。

### 出现 `Dex分析失败：IllegalStateException`

可能是设备无法从服务器下载运行文件。请尝试连接 **VPN** 后继续。

## 📚 脚本文档

脚本开发文档维护于 [NukeDevelopers/NukeJsDocs](https://github.com/NukeDevelopers/NukeJsDocs)，包含快速开始、权限模型、API 参考与迁移说明。


---

<div align="center">

**QQ · 微信 · 抖音**<br>
<sub>Nuke · Android Xposed Module</sub>

</div>




