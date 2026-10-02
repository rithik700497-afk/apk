SWIZ DELIVERY — APK BANANE KE STEPS (bina Android Studio ke)
=============================================================
1) www/config.js kholo aur apne backend ka URL daalo:
      window.SWIZ_API_BASE_URL = 'https://aapka-backend-url';
   (khaali rakhoge to APK demo mode mein chalega — nakli data)

2) Backend ke .env mein ye ADD karo (comma se alag), phir backend restart karo:
      CORS_ORIGINS=https://localhost,https://aapka-netlify-link.netlify.app
   "https://localhost" zaroori hai — APK ke andar app isi naam se chalta hai.
   Iske bina app mein "Could not reach the server" aayega.

3) github.com par free account banao -> New repository (naam: swiz-app) -> "uploading an existing file".
   Is folder ki SAARI files upload karo (hidden folder .github bhi — usko drag-drop se hi daalna).

4) Repo mein Actions tab -> "Build Android APK" -> Run workflow. 5-10 minute lagte hain.

5) Run poora hone par neeche Artifacts mein "swiz-delivery-apk" download karo (zip hai) -> andar app-debug.apk.

6) Phone mein APK bhejo -> install karo ("Unknown sources" allow karna padega).

NOTE: Ye debug APK hai — dosto/testing ke liye theek hai. Play Store ke liye signed release build alag se banti hai.
