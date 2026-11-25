# Nexus Reader：ウェブトゥーン、マンガ、コミックを快適に読む

KotlinとJetpack Composeで開発され、Android 7～16に対応。統合ブラウザ、自動ダークモード、ローカルルームへのプライベートお気に入りと履歴保存、15分ごとのバックグラウンドRSSアラート機能を搭載。

# Nexus Reader — 公式ランディングページとダウンロードポータル（`nexus.apk`）

**Nexus（Nexus Reader）**の公式ランディングページ。**Kotlin**と**Jetpack Compose（Material Design 3）**で開発されたネイティブAndroidアプリケーション。マンガ、ウェブトゥーン、コミックを閲覧でき、自動ダークモード、ローカルSQLiteルームへのプライベートお気に入りと履歴保存、15分ごとのバックグラウンドRSSアラート、アップデートチェッカー機能を搭載。

## Androidアプリケーション技術仕様

| データ | 値 |

| --- | --- |

**名前／内部タイトル** | Nexus（`Nexus Reader`）|

| **パッケージID（`applicationId`）** | `com.henfluxdevelopments.nexus` |

**GitHubリポジトリ** | [justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons](https://github.com/justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons) |

**現在のバージョン** | `1.0a`（`1.0-beta`、`versionCode: 1`から開始） |

**インストーラーファイル** | `nexus.apk` |

**Android互換性** | Android 7.0 Nougat（`API 24`）からAndroid 16（`API 36`）まで |

**Androidスタック** | Kotlin、Jetpack Compose (Material 3)、Room (SQLite)、DataStore、OkHttp、Coil |

**ダークスタイルパレット** | `#0B0B10` (背景)、`#13141C` (サーフェス)、`#FF2E63` (プライマリアクセント)、`#00E5FF` (セカンダリアクセント) |

**フォント** | Space Grotesk、Plus Jakarta Sans、JetBrains Mono、System Sans-Serif (`11sp`) |

### `AndroidManifest.xml` で宣言されているパーミッション

- `INTERNET` および `ACCESS_NETWORK_STATE`: 組み込みのブラウジング、RSSフィードの読み取り、および更新の確認に使用されます。

- `POST_NOTIFICATIONS`: Android 13以降で、ユーザーがRSSアラートを有効にしている場合のみ、実行時に要求されます。


- `RECEIVE_BOOT_COMPLETED`: デバイス再起動後、15分ごとに定期的なRSSフィードチェックを再開します。

**プライバシー侵害のないアクセス許可**: カメラ、マイク、GPS、および広範なストレージへのアクセスを要求しません。


---

## `nexus.apk` の整合性の検証

配布またはインストールする前に、署名済みバイナリのサイズとSHA-256ハッシュを確認してください。

```powershell
# Windows (PowerShell)
(Get-Item nexus.apk).Length
Get-FileHash nexus.apk -Algorithm SHA256
```

```bash
# Linux / macOS
ls -lh nexus.apk && sha256sum nexus.apk

# 証明書の署名
keytool -printcert -jarfile nexus.apk
```

---

## 今後のバージョンとプロジェクトの範囲

アイデアはシンプルです。お気に入りのコミックを読むために何十もの別々のアプリを使う必要はありません。200万点以上の作品を収録し、毎日新しい作品が追加される単一のリポジトリにすべてを統合すればいいのです。



このプロジェクトは当初、数千のコミックへのアクセスを提供するというシンプルなものでしたが、最終的には数百万もの投稿をオンラインで閲覧したり、PDFやCBR形式でダウンロードしたりできる規模にまで拡大する予定です。そのため、最適な開発計画を策定するために、サーバー負荷テストとストレステストを実施しています。

--
