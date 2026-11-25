# Nexus Reader: Baca Webtoon, Manga, dan Komik dengan Mudah

Dikembangkan dengan Kotlin dan Jetpack Compose, kompatibel dengan Android 7 hingga 16, dengan browser terintegrasi, mode gelap otomatis, favorit pribadi dan riwayat dalam Ruang lokal, dan peringatan RSS latar belakang setiap 15 menit.

# Nexus Reader — Halaman Utama Resmi dan Portal Unduhan (`nexus.apk`)

Halaman utama resmi untuk **Nexus (Nexus Reader)**, aplikasi Android asli yang dikembangkan dengan **Kotlin** dan **Jetpack Compose (Material Design 3)** untuk menjelajahi manga, webtoon, dan komik, dengan mode gelap otomatis, favorit pribadi dan riwayat dalam Ruang (SQLite lokal), peringatan RSS latar belakang setiap 15 menit, dan pemeriksa pembaruan.

## Spesifikasi Teknis Aplikasi Android

| Data | Nilai |

| --- | --- |

**Nama / Judul Internal** | Nexus (`Nexus Reader`) |

| **ID Paket (`applicationId`)** | `com.henfluxdevelopments.nexus` |

**Repositori GitHub** | [justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons](https://github.com/justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons) |

**Versi Saat Ini** | `1.0a` (dimulai dari `1.0-beta`, `versionCode: 1`) |

**File Installer** | `nexus.apk` |

**Kompatibilitas Android** | Android 7.0 Nougat (`API 24`) hingga Android 16 (`API 36`) |

**Stack Android** | Kotlin, Jetpack Compose (Material 3), Room (SQLite), DataStore, OkHttp, Coil |

**Palet Darkstyle** | `#0B0B10` (latar belakang), `#13141C` (permukaan), `#FF2E63` (aksen utama), `#00E5FF` (aksen sekunder) |

**Font** | Space Grotesk, Plus Jakarta Sans, JetBrains Mono, System Sans-Serif (`11sp`) |

### Izin yang dideklarasikan dalam `AndroidManifest.xml`

- `INTERNET` dan `ACCESS_NETWORK_STATE`: Penjelajahan bawaan, membaca umpan RSS, dan memeriksa pembaruan.

- `POST_NOTIFICATIONS`: Diminta saat runtime di Android 13+ hanya jika pengguna mengaktifkan peringatan RSS.

- `RECEIVE_BOOT_COMPLETED`: Mengaktifkan kembali pemeriksaan umpan RSS berkala setiap 15 menit setelah perangkat dimulai ulang.

**Tanpa Izin yang Mengganggu**: Tidak meminta akses kamera, mikrofon, GPS, atau penyimpanan yang ekstensif.


---

## Memverifikasi integritas `nexus.apk`

Periksa ukuran dan hash SHA-256 dari biner yang ditandatangani sebelum mendistribusikan atau menginstalnya:

```powershell
# Windows (PowerShell)
(Get-Item nexus.apk).Length
Get-FileHash nexus.apk -Algorithm SHA256
```

```bash
# Linux / macOS
ls -lh nexus.apk && sha256sum nexus.apk

# Menandatangani sertifikat
keytool -printcert -jarfile nexus.apk
```

---

## Versi Mendatang dan Lingkup Proyek

Idenya sederhana: mengapa memiliki lusinan aplikasi terpisah untuk membaca komik favorit Anda ketika Anda dapat menyatukan semuanya dalam satu repositori dengan lebih dari 2 juta karya, yang diperbarui setiap hari dengan materi baru?

Pengujian beban dan stres server sedang dilakukan untuk merancang rencana pengembangan terbaik untuk proyek ini, yang awalnya hanya berupa akses ke beberapa ribu komik dan pada akhirnya akan berkembang menjadi jutaan postingan yang siap dibaca secara online atau diunduh dalam format PDF atau CBR.

--
