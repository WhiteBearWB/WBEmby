# WBEmby
适用于 Android TV 的第三方 Emby 客户端，针对遥控器操作与本地解码兼容性实现。

<img width="400" alt="左图" src="https://github.com/user-attachments/assets/cc9598c8-3f2f-4f83-95ef-91adcbdc5a55" /> <img width="400" alt="右图" src="https://github.com/user-attachments/assets/9c4162a4-478f-4371-81d8-62c18eab63b9" />


## 系统要求

| 项 | 要求 |
| --- | --- |
| 系统版本 | Android 8.0（API 26）及以上 |
| ABI | armeabi-v7a |
| 服务端 | Emby Server 4.x |
| 网络 | 可访问自建 Emby 服务器；可选用 HTTP / SOCKS5 代理 |

## 安装

从 Releases 下载最新版本 APK 并安装

## 功能

### 播放
- 默认使用硬件解码；解码或渲染失败时自动降级至备用播放引擎，并保留播放位置
- 音频解码支持 AC3、E-AC3、DTS、DTS-HD、TrueHD
- 支持 4K、HDR10 片源；Dolby Vision Profile 7 按 HEVC 基底层播放（可关闭）
- 倍速 0.5×–3.0×；长按 OK 临时加速；快进步长可配置
- 片头片尾打点跳过；剧集自动连播；播放进度与观看状态回传服务器

### 字幕
- ASS 字幕按原始样式渲染，保留字体、定位与特效
- 进入播放时自动选择字幕轨，按条目记忆
- 字幕与音轨可在播放面板内切换

### 浏览与操作
- 全流程遥控器操作，焦点移动与页面滚动均按方向键语义处理
- 搜索支持最近历史记录

### 服务器与网络
- 支持添加多台服务器；同一服务器可配置多条线路并测速优选
- 局域网内扫码添加：电视端显示二维码，手机扫码后填写上传回电视端

## 许可证
本项目仅供学习交流使用
