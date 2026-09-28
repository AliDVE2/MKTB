مكتب المهندس - موقع + تطبيق اندرويد (APK) من نفس الكود

المجلد:
  public/           ملفات الموقع والتطبيق (index.html هو كل شي)
  firestore.rules   قواعد الحماية (تنسخ لفايبرس)
  firebase.json     اعدادات النشر
  capacitor.config.json / package.json   لبناء APK

=== 1) نشر الموقع على Firebase Hosting ===
  npm install -g firebase-tools
  firebase login
  firebase use almhnds-67fdb
  firebase deploy --only hosting,firestore:rules
رابط الموقع: https://almhnds-67fdb.web.app
ثم من Firebase: Authentication > Settings > Authorized domains تأكد ان الدومين مضاف.

=== 2) بناء APK (الطريقة الاسهل بدون Android Studio) ===
  افتح https://www.pwabuilder.com
  حط رابط الموقع  https://almhnds-67fdb.web.app
  Package for stores > Android > Generate
  ينزل ملف zip بداخله ملف APK (للتجربة والتوزيع المباشر).

=== 3) بناء APK بطريقة Capacitor (تحتاج Node + Android Studio) ===
  npm install
  npx cap add android
  npx cap sync android
  npx cap open android
  ثم من Android Studio:  Build > Build APK(s)
  الملف: android/app/build/outputs/apk/debug/app-debug.apk

اي تعديل بـ public/index.html:  اعد النشر (firebase deploy) وللتطبيق نفذ npx cap sync.
