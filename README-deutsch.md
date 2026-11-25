# Lector Nexus: Webtoons, Mangas und Comics komfortabel lesen

Entwickelt mit Kotlin und Jetpack Compose; kompatibel mit Android 7 bis 16. Enthält einen integrierten Browser, einen automatischen Dark Mode für Webseiten, eine private Favoriten- und Verlauf-Verwaltung (lokal via Room) sowie RSS-Benachrichtigungen, die alle 15 Minuten im Hintergrund aktualisiert werden.

# Lector Nexus — Offizielle Landingpage und Download-Portal (`nexus.apk`)

Offizielle Landingpage für **Nexus (Lector Nexus)** – eine native Android-Anwendung, entwickelt mit **Kotlin** und **Jetpack Compose (Material Design 3)**. Die App dient zum Lesen von Mangas, Webtoons und Comics und bietet einen automatischen Dark Mode für Webseiten, eine private Favoriten- und Verlauf-Verwaltung (lokal via Room), RSS-Benachrichtigungen im Hintergrund (alle 15 Minuten) sowie eine Funktion zur Überprüfung auf Updates.

## Technische Daten der Android-Anwendung

| Eigenschaft | Wert |
| --- | --- |
| **Name / Interner Titel** | Nexus (`Lector Nexus`) |
| **Paket-ID (`applicationId`)** | `com.henfluxdevelopments.nexus` |
| **GitHub-Repository** | [justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons](https://github.com/justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons) |
| **Aktuelle Version** | `1.0a` (Start bei `1.0-beta`, `versionCode: 1`) |
| **Installationsdatei** | `nexus.apk` |
| **Android-Kompatibilität** | Android 7.0 Nougat (`API 24`) bis Android 16 (`API 36`) |
| **Android-Technologie-Stack** | Kotlin, Jetpack Compose (Material 3), Room (SQLite), DataStore, OkHttp, Coil |
| **Dark-Mode-Farbpalette** | `#0B0B10` (Hintergrund), `#13141C` (Oberflächen), `#FF2E63` (primärer Akzent), `#00E5FF` (sekundärer Akzent) |
| **Schriftarten** | Space Grotesk, Plus Jakarta Sans, JetBrains Mono, systemeigene Sans-Serif-Schrift (`11sp`) |

### In der `AndroidManifest.xml` deklarierte Berechtigungen

- `INTERNET` und `ACCESS_NETWORK_STATE`: Integriertes Browsing, Lesen des RSS-Feeds und Überprüfung auf Updates.
- `POST_NOTIFICATIONS`: Wird unter Android 13+ zur Laufzeit angefordert – jedoch nur, wenn der Nutzer RSS-Benachrichtigungen aktiviert lässt.
- `RECEIVE_BOOT_COMPLETED`: Reaktiviert die regelmäßige Überprüfung des RSS-Feeds (alle 15 Minuten) nach einem Neustart des Geräts.
- **Keine invasiven Berechtigungen**: Es werden weder Kamera, Mikrofon oder GPS angefordert, noch gibt es einen umfassenden Zugriff auf den Speicher.

---

## Integritätsprüfung der `nexus.apk`

Überprüfen Sie die Dateigröße und den SHA-256-Hash der signierten Binärdatei, bevor Sie diese weitergeben oder installieren:

```powershell
# Windows (PowerShell)
(Get-Item nexus.apk).Length
Get-FileHash nexus.apk -Algorithm SHA256
```

```bash
# Linux / macOS
ls -lh nexus.apk && sha256sum nexus.apk

# Signaturzertifikat
keytool -printcert -jarfile nexus.apk
```

---

## Zukünftige Versionen und Umfang des Projekts

Die Idee ist simpel: Warum Dutzende separater Apps nutzen, um eure Lieblingscomics zu lesen, wenn man alles in einer einzigen Sammlung vereinen kann? Diese umfasst über 2 Millionen Werke und wird täglich mit neuen Inhalten aktualisiert. Es werden Server-Last- und Stresstests durchgeführt, um den optimalen Entwicklungsplan für ein solches Projekt zu erarbeiten – ein Projekt, das ursprünglich lediglich als Zugang zu einigen tausend Comics begann und sich künftig zu einer Plattform mit Millionen von Beiträgen entwickeln soll, die man online lesen oder als PDF- bzw. CBR-Datei herunterladen kann.

---
