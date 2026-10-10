# Daily Collection Book — Android APK build

This project packages the HTML app in `www/index.html` into an Android app using Capacitor and builds the APK on GitHub Actions.

## Build it on GitHub (no Android Studio required)

1. Create a GitHub repository, for example `DailyCollectionBookAPK`.
2. Extract this ZIP on your computer.
3. In the extracted folder, open PowerShell/Terminal and run:

   ```powershell
   git init
   git add .
   git commit -m "Add Daily Collection Book Android app"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   git push -u origin main
   ```

   Replace the URL with your own repository URL. If GitHub asks you to sign in, complete its authentication steps.

4. On GitHub, open the repository and click **Actions**. If prompted, enable workflows.
5. Open **Build Daily Collection Book APK** and click **Run workflow** if it is not already running automatically after your push.
6. Wait until the workflow has a green checkmark. Open that workflow run, scroll to **Artifacts**, and download `daily-collection-book-apk`.
7. Extract the downloaded artifact ZIP. It contains `app-debug.apk`. Transfer it to your Android phone and open it to install. If Android blocks installation, allow installation from that source in Android settings.

## Data storage warning

The app uses browser localStorage. Inside the APK it should persist between app launches, but uninstalling/clearing app data can erase local records. Use the in-app JSON backup regularly. WhatsApp opens with a prefilled message; you still tap Send yourself.

This is a debug APK for personal testing, not a Play Store release. Do not share personal collection data in the GitHub repository.
