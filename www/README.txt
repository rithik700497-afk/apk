SWIZ DELIVERY — SERVER SE CONNECT KARNE KE STEPS
================================================
Is folder mein:
  index.html           -> app
  config.js            -> yahan server ka URL daalna hai (sirf yehi file edit karni hai)
  test-connection.html -> server check karne ka page
  assets/              -> images (folder hatana mat)

1) Backend deploy karo (Render / Railway / VPS) -> aapko https://... URL milega.
2) Backend mein CORS ON karo (headers: Content-Type, Authorization;
   methods: GET, POST, PUT, PATCH, DELETE, OPTIONS; origin: jahan app host hoga).
3) Is folder ko Netlify Drop (app.netlify.com/drop) par daalo -> app ka link milega.
4) Link ke aage /test-connection.html lagao, server URL daalo, "Test karo" dabao. Sab green hona chahiye.
5) config.js kholo, URL daalo:   window.SWIZ_API_BASE_URL = 'https://aapka-server.com';
   Phir folder dobara upload karo.
6) App kholo aur login try karo. Galti aaye to browser mein F12 -> Network tab dekho.

URL khaali rakhoge to app DEMO mode mein chalega (fake data).

ICONS (APK / Play Store ke liye)
  assets/icon-512.png, icon-192.png, apple-touch-icon.png, favicon-32.png/64.png  -> SWIZ logo se bane hain.

BACK BUTTON
  Phone ka back button ab ek-ek screen peeche jaata hai. Home par back dabane par
  "Press back again to exit" aata hai, dobara dabane par app band hota hai.
