# THE Bazile oasis (Android APK)

This is an Android app that wraps the single-file web app `app/src/main/assets/index.html` in a WebView.

## Build on GitHub (no local tools needed)

1. Create a new GitHub repository and push this folder to it.
2. Open the **Actions** tab. The "Build APK" workflow runs on every push (or start it manually with "Run workflow").
3. When it finishes, open the run and download the `bazile-oasis-debug` artifact. It contains `app-debug.apk`.

## Install on your Android phone

1. Copy `app-debug.apk` to the phone and open it.
2. Allow installs from that source when Android asks.
3. Open "THE Bazile oasis".

## Updating the app

Replace `app/src/main/assets/index.html` with a new version and push. The workflow builds a new APK.

## Known limitations

- Downloads created from `blob:` URLs (the in-app downloader's save button) are not supported yet in this WebView wrapper. Direct http(s) downloads work.
- Pages that block cross-site requests can't be scanned from inside the app, same as in a browser.
- Fullscreen video is not wired up.
- The APK is a debug build, signed with the default debug key. It is fine for personal sideloading but not for Play Store release.
