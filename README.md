# Voice-TV-Remote-pro

Android Arabic speech recognition prototype for a TV remote.

**Important:** This is not yet a direct Xiaomi TV remote. It sends commands to a user-provided HTTP bridge on the local network, at `GET /command?key=VOLUME_UP` (or `VOLUME_DOWN`, `MUTE`, `HOME`, `BACK`, `PLAY_PAUSE`). A compatible and securely configured bridge is required; no bridge is included. The APK cannot control a TV on its own.

## Build

Upload project files to the repository root, preserving directories, then open GitHub Actions > Build Android APK > Run workflow. Download `Voice-TV-Remote-debug-apk` from the successful run's Artifacts section. The APK is a debug build, not a production release.

Requires Android SDK 35, Java 17 and Gradle with Android Gradle Plugin 8.7.3. On a local machine run `gradle :app:assembleDebug`.

For testing, use only a bridge on your own trusted LAN. The app uses cleartext HTTP for local development; do not expose it to the public internet.
