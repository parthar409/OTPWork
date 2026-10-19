# OTPWORK Android WebView App

- **App name:** OTPWORK
- **Application ID:** `online.otpwork.app`
- **Start URL:** `https://otpwork.online/panel.php`
- **Theme:** Blue
- **Minimum Android:** 6.0 (API 23)
- **Target SDK:** 35

## Build APK with Android Studio

1. Install **Android Studio** and JDK 17 (Android Studio includes an embedded JDK).
2. Unzip this project. In Android Studio choose **Open** and select the `OTPWORK-Android-Studio` folder.
3. Allow Gradle sync and Android SDK 35 installation. Internet access is needed to download build tools/dependencies.
4. Choose **Build > Build Bundle(s) / APK(s) > Build APK(s)** (wording may differ by version).
5. Find debug APK at `app/build/outputs/apk/debug/app-debug.apk`.
6. Transfer the APK to your Android phone and open it to install. Android may ask you to allow installs from that source.
7. For production, use **Build > Generate Signed Bundle / APK > APK**, create and securely back up your keystore, and sign the release APK. Never share your keystore password.

## Notes

- This is **source code**, not a precompiled APK. No APK has been built or device-tested here.
- Requires a working HTTPS site and network connection. The site controls authentication and dashboard behavior.
- File uploads use Android's system picker. Downloads go to app-specific external Downloads storage (not necessarily the public Downloads folder).
- External `http://` links are opened in a browser; HTTPS pages are kept inside the WebView.
- Camera capture, geolocation, notifications, payment popups, `target=_blank`, and OAuth may require additional implementation and testing depending on website features.
- Check site ownership/permission, and test login, session persistence, file uploads/downloads, redirects, and back navigation on real devices before distribution.
- The app icon is a generated generic blue document icon, not an official OTPWORK brand asset.
- Android 15 edge-to-edge and navigation behavior should be verified on actual target devices.
- This archive does not include Gradle wrapper binaries. Android Studio can sync with its bundled Gradle integration; if necessary generate a wrapper with `gradle wrapper --gradle-version 8.7` using installed Gradle, then sync.
