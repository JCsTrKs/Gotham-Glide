# Gotham Glide Android build

This project wraps the supplied `Gotham Glide` HTML game in an Android WebView and enables immersive full-screen mode.

## Build on your phone with GitHub Actions
1. Create a GitHub repository and upload **all files and folders** from this project. Make sure `.github/workflows/build-apk.yml` is included.
2. Open the repository's **Actions** tab.
3. Select **Build Gotham Glide APK** and tap **Run workflow** (or wait for the initial push build).
4. Open the completed workflow run and download the `Gotham-Glide-debug-apk` artifact.
5. Extract the ZIP and install `app-debug.apk` on your Android phone.

## Notes
- The original game mechanics, including the Gargoyle King boss fight at score 50, are preserved in `app/src/main/assets/index.html`.
- The HTML uses the live visual viewport and fills the available screen on different phone sizes, including when browser viewport dimensions change. To avoid black bars, the canvas fills the screen; this can cause slight stretching on unusual aspect ratios. The Android wrapper runs portrait and immersive full-screen.
- Android immersive mode hides the status and navigation bars, which can temporarily reappear with a system swipe.
- This is a debug APK for personal testing, not a Play Store release.
