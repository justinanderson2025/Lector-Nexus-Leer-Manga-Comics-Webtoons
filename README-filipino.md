# Nexus Reader: Magbasa ng mga Webtoon, Manga, at Komiks nang Maginhawa

Binuo sa Kotlin at Jetpack Compose, tugma sa Android 7 hanggang 16, na may integrated browser, awtomatikong dark mode, mga pribadong paborito at history sa isang lokal na Kwarto, at mga background na alerto sa RSS bawat 15 minuto.

# Nexus Reader — Opisyal na Landing Page at Download Portal (`nexus.apk`)

Opisyal na landing page para sa **Nexus (Nexus Reader)**, isang katutubong Android application na binuo sa **Kotlin** at **Jetpack Compose (Material Design 3)** para sa paggalugad ng manga, webtoon, at komiks, na may awtomatikong dark mode, mga pribadong paborito at history sa isang Kwarto (lokal na SQLite), mga background na alerto sa RSS bawat 15 minuto, at isang update checker.

## Mga Teknikal na Detalye ng Aplikasyon ng Android

| Data | Halaga |

| --- | --- |

**Pangalan / Panloob na Pamagat** | Nexus (`Nexus Reader`) |

| **Package ID (`applicationId`)** | `com.henfluxdevelopments.nexus` |

**GitHub Repository** | [justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons](https://github.com/justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons) |

**Kasalukuyang Bersyon** | `1.0a` (nagsimula sa `1.0-beta`, `versionCode: 1`) |

**File ng Installer** | `nexus.apk` |

**Kakayahan sa Android** | Android 7.0 Nougat (`API 24`) hanggang Android 16 (`API 36`) |

**Android Stack** | Kotlin, Jetpack Compose (Material 3), Room (SQLite), DataStore, OkHttp, Coil |

**Darkstyle Palette** | `#0B0B10` (background), `#13141C` (mga surface), `#FF2E63` (pangunahing accent), `#00E5FF` (pangalawang accent) |

**Mga Font** | Space Grotesk, Plus Jakarta Sans, JetBrains Mono, System Sans-Serif (`11sp`) |

### Mga Pahintulot na idineklara sa `AndroidManifest.xml`

- `INTERNET` at `ACCESS_NETWORK_STATE`: Built-in na pag-browse, pagbabasa ng RSS feed, at pagsuri para sa mga update.

- `POST_NOTIFICATIONS`: Hinihiling lamang sa runtime sa Android 13+ kung naka-enable ang mga alerto sa RSS ng user.

- `RECEIVE_BOOT_COMPLETED`: Muling ina-activate ang pana-panahong pagsusuri ng RSS feed bawat 15 minuto pagkatapos mag-restart ang device.

**Walang Mapanghimasok na Pahintulot**: Hindi humihiling ng camera, mikropono, GPS, o malawak na access sa storage.

---

## Pag-verify sa integridad ng `nexus.apk`

Suriin ang laki at SHA-256 hash ng nilagdaang binary bago ito ipamahagi o i-install:

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

## Mga Bersyon sa Hinaharap at Saklaw ng Proyekto

Simple lang ang ideya: bakit kailangan ng dose-dosenang magkakahiwalay na app para basahin ang iyong mga paboritong komiks kung maaari mong pag-isahin ang lahat sa isang repository na may higit sa 2 milyong gawa, na ina-update araw-araw gamit ang mga bagong materyal?

Isinasagawa ang mga pagsubok sa pagkarga at stress ng server upang makabuo ng pinakamahusay na plano sa pag-unlad para sa proyektong ito, na nagsimula bilang access lamang sa ilang libong komiks at kalaunan ay lalawak sa milyun-milyong mga post na handa nang basahin online o i-download sa PDF o CBR format.

--
