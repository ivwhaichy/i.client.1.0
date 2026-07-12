# i.client

Android VPN client built with Kotlin, Jetpack Compose, Android VpnService, WorkManager, WebView, and Xray runtime integration.

## Features

- VLESS REALITY / XTLS Vision profile parsing and Xray config generation.
- Multiple saved connection profiles with profile metadata.
- Web panel opened from the selected profile URL.
- Split tunneling modes for installed and system apps.
- Quick Settings tile with the rabbit icon.
- Connection state verification before showing the VPN as connected.

## Build

Requirements:

- JDK 17
- Android SDK with API 35
- Gradle wrapper from this repository

Debug:

```powershell
.\gradlew.bat assembleDebug
```

Release:

```powershell
.\gradlew.bat assembleRelease
```

The named release APK is produced at:

```text
app/build/outputs/apk/release/i.client.apk
```

The standard Gradle release APK is also produced at:

```text
app/build/outputs/apk/release/app-release.apk
```

## Release Signing

For local development, the release build falls back to the debug signing config if no release keystore is configured.

For a real release, create `keystore.properties` from `keystore.properties.example` or provide these environment variables:

```text
RELEASE_STORE_FILE
RELEASE_STORE_PASSWORD
RELEASE_KEY_ALIAS
RELEASE_KEY_PASSWORD
```

Do not commit `keystore.properties` or keystore files.

## Repository Notes

- `local.properties`, local Android SDK folders, Gradle build outputs, and signing files are ignored.
- `app/libs/libv2ray.aar` is required for the current Xray integration. It is a large binary, so GitHub may recommend Git LFS for it.
- `app/libs/libbox.aar` is ignored because the current release uses Xray/libv2ray instead of sing-box/libbox.

## GitHub

See [GITHUB_UPLOAD.md](GITHUB_UPLOAD.md) for the exact upload checklist, ignored local files, release APK publishing steps, and GitHub Actions signing setup.
