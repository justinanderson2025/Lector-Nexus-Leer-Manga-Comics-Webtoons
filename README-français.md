# Nexus Reader : Lisez des Webtoons, des mangas et des comics en toute simplicité

Développée en Kotlin et Jetpack Compose, compatible avec Android 7 à 16, cette application intègre un navigateur, un mode sombre automatique pour le web, une gestion privée des favoris et de l'historique via Room (base de données locale), ainsi que des alertes RSS en arrière-plan toutes les 15 minutes.

# Nexus Reader — Page officielle et portail de téléchargement (`nexus.apk`)

Page officielle de **Nexus (Nexus Reader)**, une application Android native développée en **Kotlin** et **Jetpack Compose (Material Design 3)** pour consulter des mangas, des webtoons et des comics. Elle propose un mode sombre automatique pour le web, une gestion privée des favoris et de l'historique via Room (SQLite local), des alertes RSS en arrière-plan toutes les 15 minutes, ainsi qu'un vérificateur de mises à jour.

## Fiche technique de l'application Android

| Donnée | Valeur |
| --- | --- |
| **Nom / Titre interne** | Nexus (`Nexus Reader`) |
| **ID du paquet (`applicationId`)** | `com.henfluxdevelopments.nexus` |
| **Dépôt GitHub** | [justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons](https://github.com/justinanderson2025/Lector-Nexus-Leer-Manga-Comics-Webtoons) |
| **Version actuelle** | `1.0a` (début à `1.0-beta`, `versionCode: 1`) |
| **Fichier d'installation** | `nexus.apk` |
| **Compatibilité Android** | Android 7.0 Nougat (`API 24`) à Android 16 (`API 36`) |
| **Stack Android** | Kotlin, Jetpack Compose (Material 3), Room (SQLite), DataStore, OkHttp, Coil |
| **Palette « Darkstyle »** | `#0B0B10` (arrière-plan), `#13141C` (surfaces), `#FF2E63` (accentuation primaire), `#00E5FF` (accentuation secondaire) |
| **Polices d'écriture** | Space Grotesk, Plus Jakarta Sans, JetBrains Mono, police sans-serif système (`11sp`) |

### Autorisations déclarées dans `AndroidManifest.xml`

- `INTERNET` et `ACCESS_NETWORK_STATE` : Navigation intégrée, lecture du flux RSS et vérification des mises à jour.
- `POST_NOTIFICATIONS` : Demandée à l'exécution (runtime) sur Android 13+ uniquement si l'utilisateur maintient les alertes RSS activées.
- `RECEIVE_BOOT_COMPLETED` : Réactive la vérification périodique du flux RSS toutes les 15 minutes après le redémarrage de l'appareil.
- **Aucune autorisation intrusive** : L'application ne demande pas l'accès à l'appareil photo, au microphone, au GPS, ni un accès étendu au stockage.

---

## Vérification de l'intégrité de `nexus.apk`

Vérifiez la taille et le hash SHA-256 du fichier binaire signé avant toute distribution ou installation :

```powershell
# Windows (PowerShell)
(Get-Item nexus.apk).Length
Get-FileHash nexus.apk -Algorithm SHA256
```

```bash
# Linux / macOS
ls -lh nexus.apk && sha256sum nexus.apk

# Certificat de signature
keytool -printcert -jarfile nexus.apk
```

---

## Versions futures et envergure du projet

L'idée est simple : pourquoi utiliser des dizaines d'applications distinctes pour lire vos bandes dessinées préférées, alors qu'il est possible de tout regrouper dans un seul et unique répertoire ? Celui-ci contient plus de 2 millions d'œuvres et est mis à jour quotidiennement avec de nouveaux contenus. Des tests de charge et de contrainte sur les serveurs sont en cours afin d'élaborer la meilleure stratégie de développement pour un tel projet ; celui-ci a débuté comme un simple accès à quelques milliers de bandes dessinées, pour aboutir, à terme, à des millions de publications disponibles à la lecture en ligne ou au téléchargement aux formats PDF ou CBR.

---
