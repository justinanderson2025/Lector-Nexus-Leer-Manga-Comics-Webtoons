# Lector Nexus: Lee Webtoons, Mangas, Comics de forma practica

Desarrollado en Kotlin y Jetpack Compose compatible con con Android 7 a 16, con navegador integrado, modo oscuro web automático, favoritos e historial privados en Room local y alertas RSS en segundo plano cada 15 minutos. 

# Lector Nexus — Landing Oficial y Portal de Descarga (`nexus.apk`)

Landing page oficial de **Nexus (Lector Nexus)**, aplicación nativa Android desarrollada en **Kotlin** y **Jetpack Compose (Material Design 3)** para explorar manga, webtoons y cómics, con modo oscuro web automático, favoritos e historial privados en Room (SQLite local), alertas RSS en segundo plano cada 15 minutos y verificador de actualizaciones.

## Ficha técnica de la aplicación Android

| Dato | Valor |
| --- | --- |
| **Nombre / Título interno** | Nexus (`Lector Nexus`) |
| **ID de paquete (`applicationId`)** | `com.henfluxdevelopments.nexus` |
| **Repositorio GitHub** | [justinanderson2025/Lector-Webtoons-Nexus](https://github.com/justinanderson2025/Lector-Webtoons-Nexus) |
| **Versión actual** | `1.0a` (inicio en `1.0-beta`, `versionCode: 1`) |
| **Archivo instalador** | `nexus.apk` |
| **Compatibilidad Android** | Android 7.0 Nougat (`API 24`) hasta Android 16 (`API 36`) |
| **Stack Android** | Kotlin, Jetpack Compose (Material 3), Room (SQLite), DataStore, OkHttp, Coil |
| **Paleta Darkstyle** | `#0B0B10` (fondo), `#13141C` (superficies), `#FF2E63` (acento primario), `#00E5FF` (acento secundario) |
| **Tipografías** | Space Grotesk, Plus Jakarta Sans, JetBrains Mono, Sans-Serif sistema (`11sp`) |

### Permisos declarados en `AndroidManifest.xml`

- `INTERNET` y `ACCESS_NETWORK_STATE`: Navegación integrada, lectura del feed RSS y verificación de actualizaciones.
- `POST_NOTIFICATIONS`: Solicitado en tiempo de ejecución en Android 13+ únicamente si el usuario mantiene activas las alertas RSS.
- `RECEIVE_BOOT_COMPLETED`: Reactiva la comprobación periódica del feed RSS cada 15 minutos tras reiniciar el dispositivo.
- **Sin permisos invasivos**: No solicita cámara, micrófono, GPS ni acceso amplio al almacenamiento.

---

## Verificación de integridad de `nexus.apk`

Comprueba el tamaño y el hash SHA-256 del binario firmado antes de distribuirlo o instalarlo:

```powershell
# Windows (PowerShell)
(Get-Item nexus.apk).Length
Get-FileHash nexus.apk -Algorithm SHA256
```

```bash
# Linux / macOS
ls -lh nexus.apk && sha256sum nexus.apk

# Certificado de firma
keytool -printcert -jarfile nexus.apk
```

---
