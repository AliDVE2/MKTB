تطبيق مكتب المهندس - اخر نسخة (فيها رفع الصورة من الجهاز + الايقونة + شاشة الافتتاح)

الملف public/index.html هو التطبيق كامل بملف وحيد، مربوط اونلاين بفايبرس.

=== لماذا محتاج تبني الـ APK بنفسك؟ ===
انشاء ملف APK يحتاج بيئة اندرويد (Android SDK) وتوقيع رقمي، وهذا غير متوفر بالبيئة اللي اشتغل بيها.
لكن جهزتلك كل شي جاهز، والخطوة الوحيدة الباقية عليك تاخذ اقل من 5 دقائق.

=== الطريقة الأسهل (بدون برمجة) ===
1. ارفع public/index.html على رابط اونلاين (GitHub Pages او Firebase Hosting).
2. افتح https://www.pwabuilder.com
3. حط رابط موقعك، اضغط Start.
4. اختار Android من Package for stores، ثم Generate.
5. ينزلك ملف يحتوي APK جاهز للتنصيب المباشر على أي جهاز اندرويد. الايقونة والاسم واللون تنجر تلقائي من نفس الملف.

=== الطريقة الثانية (تحتاج Node.js و Android Studio) ===
1. npm install
2. npx cap add android
3. npx cap sync android
4. npx cap open android
5. من Android Studio: Build > Build Bundle(s) / APK(s) > Build APK(s)
6. الملف: android/app/build/outputs/apk/debug/app-debug.apk
