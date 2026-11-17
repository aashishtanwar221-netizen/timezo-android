# TIMEZO — Android WebView Project (SB Infotech)

- **Package Name (`applicationId`):** `site.tiiny.tomato_jolee_83.twa`
- **Version Code:** `2`
- **Version Name:** `1.0.1`
- **Target / Compile SDK:** `34` (Android 14)
- **Min SDK:** `24` (Android 7.0)

## GitHub Actions se AAB / APK kaise banayein

1. GitHub par ek naya repository banayein (e.g., `timezo-android`).
2. Is ZIP ke andar ki saari files (including `.github/workflows/android-build.yml`) ko repository ke root me upload/push karein.
3. GitHub repo ke **Actions** tab me jayein — workflow automatic start ho jayega (ya **Run workflow** par click karein).
4. Build complete hone par **Artifacts** section se `TIMEZO-release-aab` aur `TIMEZO-release-apk` download karein.

## Play Store Signing (Optional / Recommended for Updates)

Agar aapko Play Store par signed AAB upload karna hai (especially jab `versionCode: 1` pehle se uploaded ho), to GitHub Repo -> **Settings -> Secrets and variables -> Actions** me ye 4 secrets add karein:

- `KEYSTORE_BASE64` (apne `.jks` keystore file ka base64 string)
- `KEYSTORE_PASSWORD`
- `KEY_ALIAS`
- `KEY_PASSWORD`

Agar secrets add nahi kiye hain, tab bhi workflow unsigned release AAB aur APK build karega.
