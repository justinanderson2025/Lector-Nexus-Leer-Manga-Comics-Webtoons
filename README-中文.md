# Nexus Reader：便捷阅读网络漫画、日本漫画和日本漫画 

采用 Kotlin 和 Jetpack Compose 开发，兼容 Android 7 至 16，内置浏览器，支持自动深色模式、本地房间的私密收藏和历史记录，以及每 15 分钟的后台 RSS 推送。

# Nexus Reader — 官方主页和下载入口 (`nexus.apk`)

**Nexus (Nexus Reader)** 的官方主页，这是一款采用 **Kotlin** 和 **Jetpack Compose (Material Design 3)** 开发的原生 Android 应用，用于浏览日本漫画、网络漫画和日本漫画，支持自动深色模式、本地房间（SQLite 数据库）的私密收藏和历史记录、每 15 分钟的后台 RSS 推送，以及更新检查。

## Android 应用技术规格

| 数据 | 值 |

| --- | --- |

**名称/内部标题** | Nexus（`Nexus Reader`）|

| **软件包 ID（`applicationId`）** | `com.henfluxdevelopments.nexus` |

**GitHub 仓库** | [justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons](https://github.com/justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons) |

**当前版本** | `1.0a`（始于 `1.0-beta`，`versionCode: 1`）|

**安装文件** | `nexus.apk` |

**Android 兼容性** | Android 7.0 Nougat (`API 24`) 至 Android 16 (`API 36`) |

**Android 技术栈** | Kotlin、Jetpack Compose（Material 3）、Room（SQLite）、DataStore、OkHttp、Coil |

**深色风格调色板** | `#0B0B10`（背景色）、`#13141C`（表面）、`#FF2E63`（主强调色）、`#00E5FF`（辅助强调色） |

**字体** | Space Grotesk、Plus Jakarta Sans、JetBrains Mono、System Sans-Serif (`11sp`) |

### 在 `AndroidManifest.xml` 中声明的权限

- `INTERNET` 和 `ACCESS_NETWORK_STATE`：内置浏览、RSS 源读取和检查更新。

- `POST_NOTIFICATIONS`：仅当用户启用 RSS 通知时，才会在 Android 13 及更高版本上运行时请求。

- `RECEIVE_BOOT_COMPLETED`：设备重启后，每 15 分钟重新启用定期 RSS 源检查。

**无侵入性权限**：不会请求摄像头、麦克风、GPS 或大量存储空间访问权限。

---

## 验证 `nexus.apk` 的完整性

在分发或安装之前，请检查已签名二进制文件的大小和 SHA-256 哈希值：

```powershell
# Windows (PowerShell)

(Get-Item nexus.apk).Length

Get-FileHash nexus.apk -Algorithm SHA256

```

```bash
# Linux / macOS

ls -lh nexus.apk && sha256sum nexus.apk

# 签名证书

keytool -printcert -jarfile nexus.apk

```

---

## 未来版本和项目范围

理念很简单：既然可以将所有内容整合到一个拥有超过 200 万部作品、每日更新的单一资源库中，为什么还要使用几十个不同的应用程序来阅读您喜爱的漫画呢？

我们正在进行服务器负载和压力测试，以制定该项目的最佳开发方案。该项目最初只是提供几千部漫画的访问权限，最终将扩展到数百万篇漫画，用户可以在线阅读或下载PDF或CBR格式的文件。

--
