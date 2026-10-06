SWIZ DELIVERY - BUILD STEPS
1) www/config.js: set window.SWIZ_API_BASE_URL = 'https://your-deployed-backend' (HTTPS, no trailing slash).
   The CI build FAILS if this is empty (empty = demo mode with fake data).
2) Backend .env: CORS_ORIGINS must include  https://localhost  (the origin the Android app runs as).
3) Push to GitHub -> Actions -> "Build Android" -> Run workflow.
4) Debug APK artifact = quick phone test. For Play Store add repo secrets:
   ANDROID_KEYSTORE_BASE64, ANDROID_KEYSTORE_PASSWORD, ANDROID_KEY_ALIAS, ANDROID_KEY_PASSWORD
   -> the run also uploads a signed app-release.aab. KEEP the keystore safe; Play needs the same key for every update.
5) versionCode/versionName are set automatically from the run number.
