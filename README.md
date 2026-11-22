# RapidJobs Android WebView wrapper

A lightweight Android app that loads https://rapidjobs.in/ in a native Android WebView.

## Included
- JavaScript and DOM storage for website login/session flows
- Persistent WebView cookies
- Back button browser navigation
- File chooser support for resume/document uploads
- External links handed to Android apps/browser
- Download handoff
- HTTPS-only website loading

## Build an APK without installing software (GitHub cloud build)

This project includes a GitHub Actions workflow at `.github/workflows/build-apk.yml`. GitHub's hosted runner installs the Android build environment and builds the APK online.

1. On your phone, open https://github.com/ and sign in (create a free account if needed).
2. Create a **New repository** named `rapidjobs-android`. Set it to **Private** if you prefer.
3. Extract this ZIP on your phone using your phone's file manager. Upload the **contents** of the `RapidJobs-WebView-Android` folder to the repository, keeping the `.github/workflows/build-apk.yml` folder structure. If your file manager hides dot-folders, enable hidden files before uploading; the workflow file is essential.
4. In the GitHub repository, open **Actions**. If prompted, enable workflows. Select **Build RapidJobs APK**, then tap **Run workflow**.
5. Wait for the run to finish with a green check mark. Open that run, scroll to **Artifacts**, and download `RapidJobs-debug-apk`.
6. Extract the downloaded artifact ZIP. It contains `app-debug.apk`. Tap it on your Android phone to install. Android may ask you to allow installs from that browser or file manager.

The workflow also runs automatically whenever you push a commit to the `main` branch.

## Technical details
- Package: `in.rapidjobs.app`
- Version: `1.0.0`
- Minimum Android: Android 6.0 (API 23)
- Target SDK: 35

This is a **debug APK** for testing, not a signed Play Store release. It has not been compiled or device-tested in this workspace. Test website login, uploads, downloads, navigation and any payment or external-link flows on your phone before wider distribution.
