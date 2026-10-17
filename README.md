# Reminder (Kotlin + Jetpack Compose)

## Build the APK (pick one)
A. Android Studio (easiest): File > Open this folder, let Gradle sync, then Build > Build APK(s).
B. Command line: install JDK 17 + Android SDK (platform 35), run `gradle wrapper --gradle-version 8.9` once, then `./gradlew assembleRelease`.
   Output: app/build/outputs/apk/release/app-release.apk
C. No local tools: push this folder to a GitHub repo; the included workflow (Actions > Build APK) builds it and attaches the APK as a downloadable artifact.

## Install
Copy the APK to the phone, open it, and allow "Install unknown apps" for your file manager/browser when asked.

## Permissions
- Notifications (Android 13+): required; requested on first launch.
- Full-screen alerts (Android 14+): optional; lets the alarm screen open over the lock screen.
- Exact alarms: not needed; the app uses AlarmManager.setAlarmClock (exact, Doze-exempt).
- Samsung/Xiaomi etc.: if reminders arrive late, set the app's battery usage to "Unrestricted".
