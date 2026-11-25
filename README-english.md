# Nexus Reader: Read Webtoons, Manga, and Comics with Ease

Developed using Kotlin and Jetpack Compose, and compatible with Android 7 through 16, this app features an integrated browser, automatic dark mode for web content, private bookmarks and history stored locally via Room, and background RSS alerts that check for updates every 15 minutes.

# Nexus Reader — Official Landing Page and Download Portal (`nexus.apk`)

The official landing page for **Nexus (Nexus Reader)**—a native Android application built with **Kotlin** and **Jetpack Compose (Material Design 3)**. Designed for exploring manga, webtoons, and comics, it includes automatic dark mode for web content, private bookmarks and history stored locally in Room (SQLite), background RSS alerts (checking every 15 minutes), and an update checker.

## Android Application Technical Specifications

| Detail | Value |
| --- | --- |
| **Name / Internal Title** | Nexus (`Nexus Reader`) |
| **Package ID (`applicationId`)** | `com.henfluxdevelopments.nexus` |
| **GitHub Repository** | [justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons](https://github.com/justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons) |
| **Current Version** | `1.0a` (starting at `1.0-beta`, `versionCode: 1`) |
| **Installer File** | `nexus.apk` |
| **Android Compatibility** | Android 7.0 Nougat (`API 24`) through Android 16 (`API 36`) |
| **Android Tech Stack** | Kotlin, Jetpack Compose (Material 3), Room (SQLite), DataStore, OkHttp, Coil |
| **Dark Style Palette** | `#0B0B10` (background), `#13141C` (surfaces), `#FF2E63` (primary accent), `#00E5FF` (secondary accent) |
| **Typefaces** | Space Grotesk, Plus Jakarta Sans, JetBrains Mono, system sans-serif (`11sp`) |

### Permissions declared in `AndroidManifest.xml`

- `INTERNET` and `ACCESS_NETWORK_STATE`: For integrated browsing, reading RSS feeds, and checking for updates.
- `POST_NOTIFICATIONS`: Requested at runtime on Android 13+ only if the user keeps RSS alerts enabled.
- `RECEIVE_BOOT_COMPLETED`: Re-enables periodic RSS feed checks (every 15 minutes) after the device restarts.
- **No intrusive permissions**: Does not request access to the camera, microphone, GPS, or broad storage access.

---

## Integrity verification for `nexus.apk`

Verify the file size and SHA-256 hash of the signed binary before distributing or installing it:

```powershell
# Windows (PowerShell)
(Get-Item nexus.apk).Length
Get-FileHash nexus.apk -Algorithm SHA256
```

```bash
# Linux / macOS
ls -lh nexus.apk && sha256sum nexus.apk

# Signing certificate
keytool -printcert -jarfile nexus.apk
```

---

## Future Versions and Project Scope

The concept is simple: why use dozens of separate apps to read your favorite comics when everything could be unified into a single repository containing over 2 million titles, updated daily with new content? Server load and stress testing are currently underway to devise the optimal development plan for this project—an initiative that began simply as a way to provide access to a few thousand comics, with the long-term goal of offering millions of posts available for online reading or download in PDF or CBR format.

---
