# Student Finance – APK build

## Get your APK (about 5 minutes, free)
1. Create a free account at github.com and make a **new repository** (any name, Public or Private).
2. Upload everything in this folder to it, including the hidden `.github` folder.
   (If the web uploader skips `.github`, click Add file > Create new file, type
   `.github/workflows/build-apk.yml` as the name, and paste in that file's contents.)
3. Open the **Actions** tab. The "Build APK" run starts by itself. Wait about 4-6 minutes for the green tick.
4. Click the finished run, scroll to **Artifacts**, download **student-finance-apk**, unzip it.
5. Send `app-debug.apk` to your phone (WhatsApp, Drive, USB) and open it.
   Android will ask you to allow "install unknown apps" for that app. Allow it once.

## Updating the app
Replace `www/index.html` with the new version and commit. A new APK builds automatically.
Install it over the old one. Your data is kept because every build uses the same signing key (`debug.keystore`).

## Notes
- Keep `debug.keystore` in the repo. A different key would force people to uninstall first and lose their data.
- This is a personal sideloaded app, so the standard debug key is fine. It is not for the Play Store.
- Automatic SMS reading is the next step: it adds a native SMS plugin and permission.
