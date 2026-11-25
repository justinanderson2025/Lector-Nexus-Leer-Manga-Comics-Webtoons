# Nexus Reader: 웹툰, 만화, 코믹스를 편리하게 읽으세요

Kotlin과 Jetpack Compose로 개발되었으며, Android 7부터 16까지 호환됩니다. 내장 브라우저, 자동 다크 모드, 로컬 Room에 저장되는 개인 즐겨찾기 및 방문 기록, 15분마다 전송되는 백그라운드 RSS 알림 기능을 제공합니다.

# Nexus Reader — 공식 랜딩 페이지 및 다운로드 포털 (`nexus.apk`)

만화, 웹툰, 코믹스를 편리하게 탐색할 수 있는 네이티브 Android 애플리케이션인 **Nexus (Nexus Reader)**의 공식 랜딩 페이지입니다. **Kotlin**과 **Jetpack Compose (Material Design 3)**로 개발되었으며, 자동 다크 모드, Room(로컬 SQLite)에 저장되는 개인 즐겨찾기 및 방문 기록, 15분마다 전송되는 백그라운드 RSS 알림, 업데이트 확인 기능 등을 제공합니다.

## Android 애플리케이션 기술 사양

| 데이터 | 값 |

| --- | --- |

**이름 / 내부 명칭** | Nexus (`Nexus Reader`) |

| **패키지 ID (`applicationId`)** | `com.henfluxdevelopments.nexus` |

**GitHub 저장소** | [justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons](https://github.com/justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons) |

**현재 버전** | `1.0a` (`1.0-beta`, `versionCode: 1`에서 시작) |

**설치 파일** | `nexus.apk` |

**안드로이드 호환성** | Android 7.0 Nougat (`API 24`)부터 Android 16 (`API 36`)까지 |

**안드로이드 스택** | Kotlin, Jetpack Compose (Material 3), Room (SQLite), DataStore, OkHttp, Coil |

**다크 스타일 팔레트** | `#0B0B10` (배경), `#13141C` (표면), `#FF2E63` (기본 강조 색상), `#00E5FF` (보조 강조 색상) |

**폰트** | Space Grotesk, Plus Jakarta Sans, JetBrains Mono, System Sans-Serif (`11sp`) |

### `AndroidManifest.xml`에 선언된 권한

- `INTERNET` 및 `ACCESS_NETWORK_STATE`: 내장 웹 브라우징, RSS 피드 읽기 및 업데이트 확인에 필요합니다.

- `POST_NOTIFICATIONS`: 사용자가 RSS 알림을 활성화한 경우에만 Android 13 이상에서 런타임에 요청됩니다.

- `RECEIVE_BOOT_COMPLETED`: 기기 재부팅 후 15분마다 주기적인 RSS 피드 확인을 다시 활성화합니다.

**권한 침해 없음**: 카메라, 마이크, GPS 또는 광범위한 저장소 접근 권한을 요청하지 않습니다.

---

## `nexus.apk` 무결성 검증

배포 또는 설치 전에 서명된 바이너리의 크기와 SHA-256 해시값을 확인하세요.

```파워셸
# Windows (PowerShell)
(Get-Item nexus.apk).Length
Get-FileHash nexus.apk -Algorithm SHA256
```

```bash
# Linux / macOS
ls -lh nexus.apk && sha256sum nexus.apk

# 서명 인증서
keytool -printcert -jarfile nexus.apk
```

---

## 향후 버전 및 프로젝트 범위

핵심 아이디어는 간단합니다. 매일 새로운 콘텐츠가 업데이트되는 200만 개 이상의 작품을 하나의 저장소에서 모두 즐길 수 있다면, 좋아하는 만화를 읽기 위해 수십 개의 개별 앱을 사용하는 대신 왜 그렇게 해야 할까요?

이 프로젝트는 처음에는 수천 편의 만화를 제공하는 소규모 서비스로 시작했지만, 최종적으로는 수백만 편의 만화를 온라인으로 읽거나 PDF 또는 CBR 형식으로 다운로드할 수 있도록 확장될 예정이며, 이를 위한 최적의 개발 계획을 수립하기 위해 서버 부하 및 스트레스 테스트가 진행 중입니다.

--
