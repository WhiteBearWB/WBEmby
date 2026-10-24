# WBEmby

Android TV 上的第三方 Emby 客户端，为遥控器操作设计。

> 本仓库**只用于分发安装包**，不包含源代码。安装包请到 [Releases](../../releases/latest) 下载。
> This repository hosts **binary releases only**.

## 下载 / Download

前往 [Releases](../../releases/latest) 页面下载最新 APK（文件名 `WBEmby-<版本号>.apk`）。

| ABI | 说明 |
|-----|------|
| `armeabi-v7a` | 32 位 ARM（本版仅提供这一个 ABI，绝大多数电视盒子/掌机适用） |

- 最低系统：**Android 8.0（API 26）**
- 安装前需允许「安装未知来源应用」
- 卸载旧版会清空登录状态与设置；覆盖安装（`adb install -r`）不会

## 功能 / Features

- **播放**：ExoPlayer 为默认引擎（MediaCodec 硬解），内置自编译的 Media3 FFmpeg 音频扩展，可直接软解 AC3 / E-AC3 / DTS / TrueHD / DTS-HD；libmpv 作为兜底引擎
- **字幕**：ASS 用 libass 渲染（保留原样式与特效）；默认自动选择中文字幕，可手动切换或关闭；按片记忆选择
- **HDR / 杜比视界**：识别 HDR10/HLG 并按设备能力选择路径；Dolby Vision Profile 7 自动降级为 HEVC 基底层播放（可关）
- **详情页三列抽屉**：片源 / 字幕 / 音轨 三列并排，就地展开选择；只有一个选项的列自动置灰
- **首页**：横向滚动贴边留白 + 弹簧跟随；上下换行时目标行落在视口固定位置；焦点列记忆
- **服务器**：多服务器 + 备用线路测速优选；局域网扫码添加（电视显示二维码，手机扫码填地址即可，一次性 token，5 分钟或离开页面即失效）
- **诊断**：播放器内诊断页（引擎/错误码/解码策略/DV 降级/卡顿归因）+ 一键复制；日志只写本机，不上传

## 权限说明 / Permissions

- `INTERNET`：连接你自己的 Emby 服务器
- 无广告、无统计、无后台服务

## 免责声明 / Disclaimer

- 本项目是第三方客户端，与 Emby LLC 无任何关系
- **不包含任何影视内容**，需自备 Emby 服务器与合法媒体
- 仅供学习交流使用；使用产生的任何后果由使用者自行承担

## 第三方组件 / Third-party

安装包内含的第三方组件与许可见 [NOTICE.md](NOTICE.md)。其中 FFmpeg 以 LGPL-2.1-or-later 静态链接（仅音频解码），
其源码可从 <https://ffmpeg.org/releases/ffmpeg-6.1.2.tar.xz> 获取，构建参数随附于 NOTICE。
