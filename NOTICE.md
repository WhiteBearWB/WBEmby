# NOTICE

WBEmby 为第三方 Emby 客户端，与 Emby LLC 无关联。本仓库**不包含任何影视内容**。

安装包内含以下第三方组件，各自保留其原始许可：

| 组件 | 版本 | 许可 | 来源 |
|------|------|------|------|
| FFmpeg（静态链入 libffmpegJNI.so，仅音频解码） | 6.1.2 | LGPL-2.1-or-later | https://ffmpeg.org/releases/ffmpeg-6.1.2.tar.xz |
| AndroidX Media3（exoplayer / hls / ui / extractor / datasource-okhttp） | 1.11.1 | Apache-2.0 | https://github.com/androidx/media |
| Media3 decoder_ffmpeg 扩展（Apache-2.0 源码） | 1.11.1 | Apache-2.0 | https://github.com/androidx/media |
| libmpv / mpv（预编译 AAR `dev.jdtech.mpv:libmpv`） | AAR 1.0.0 | 包装层 MIT；内嵌 libmpv 原生库 GPL-2.0-or-later / LGPL-2.1-or-later（取决于上游构建） | https://github.com/jarnedemeulemeester/libmpv-android · https://mpv.io |
| libass（随 ass-kt natives） | — | ISC | https://github.com/libass/libass |
| ass-kt / ass-media | 0.5.1 | MIT | https://github.com/peerless2012/ass-kt |
| Kotlin stdlib | 2.4.21 | Apache-2.0 | https://github.com/JetBrains/kotlin |
| Jetpack Compose | BOM 2026.09.00 | Apache-2.0 | https://developer.android.com/jetpack/compose |
| AndroidX core-ktx / activity-compose / lifecycle / navigation-compose / datastore | — | Apache-2.0 | https://developer.android.com/jetpack |
| Coil 3 | 3.6.3 | Apache-2.0 | https://github.com/coil-kt/coil |
| OkHttp | 5.5.0 | Apache-2.0 | https://github.com/square/okhttp |
| kotlinx.serialization / kotlinx.coroutines | — | Apache-2.0 | https://github.com/Kotlin |
| ZXing core（仅用于生成配对二维码） | 3.5.3 | Apache-2.0 | https://github.com/zxing/zxing |

## LGPL 说明（FFmpeg）

本安装包内静态链接的 FFmpeg 仅启用音频解码器，构建时使用 `--disable-everything` 与以下开关（无 `--enable-gpl`、无 `--enable-nonfree`）：

```
--enable-decoder=aac,mp3,ac3,eac3,truehd,mlp,dca,vorbis,opus,amrnb,amrwb,flac,alac,pcm_mulaw,pcm_alaw
--enable-swresample --disable-shared --enable-static
```

对应的 FFmpeg 源码版本为 6.1.2，可从 <https://ffmpeg.org/releases/ffmpeg-6.1.2.tar.xz> 获取。
若需要可重新链接的替代方式，请通过仓库 Issues 联系。

## 关于 libmpv

`dev.jdtech.mpv:libmpv` 为预编译 AAR，本项目**不自行编译 mpv**。再分发前请自行核对上游许可条款。
