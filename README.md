# Night Prayer – offline Android app

All prayer text and the logo are bundled inside the app, so it works with no internet.

## Get the APK (no Android Studio needed)

1. Create a free account at https://github.com and make a **new repository** (private is fine).
2. Upload everything in this folder to it (drag and drop on the repo page works).
   Make sure the `.github` folder is included.
3. Open the **Actions** tab → **Build APK** → wait about 5 minutes for the green check.
4. Open the finished run, download **night-prayer-apk** at the bottom, unzip it.
5. Send `app-debug.apk` to your phone and tap it. If asked, allow
   "Install unknown apps" for the app you opened it from.

## Editing

- Prayer text, colors, verses: `www/index.html`
- App name and ID: `capacitor.config.json`
- App icon: replace `assets/icon-only.png` (square, at least 1024×1024)

Push the change and download the new APK from Actions.

## Optional: build on your own computer

Needs Node 20+, Java 21 and Android Studio.

    npm install
    npx cap add android
    npx capacitor-assets generate --android --iconBackgroundColor '#082b62'
    npx cap sync android
    cd android && ./gradlew assembleDebug

APK location: `android/app/build/outputs/apk/debug/app-debug.apk`
