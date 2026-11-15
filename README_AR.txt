مشروع Termox Android - نسخة محسّنة للبناء عبر GitHub Actions

مهم: هذا أرشيف مشروع Android وليس ملف APK جاهزًا للتثبيت.

طريقة البناء:
1) فك ضغط هذا الملف على هاتفك أو الكمبيوتر.
2) ارفع محتويات المجلد (وليس ملف ZIP نفسه) إلى جذر مستودع GitHub.
   يجب أن يظهر build.gradle و settings.gradle ومجلد app ومجلد .github في الصفحة الرئيسية للمستودع.
3) افتح تبويب Actions.
4) اختر Build Android APK ثم Run workflow، أو ادفع commit جديدًا إلى main/master.
5) بعد نجاح العملية، افتح صفحة التشغيل وانزل إلى Artifacts.
6) نزّل Termox-debug-apk وفك ضغطه لتحصل على app-debug.apk.

التحسينات:
- تشغيل ملفات HTML من WebViewAssetLoader على نطاق HTTPS محلي موثوق، ما يسمح بعمل Service Worker بصورة أفضل.
- إضافة إذن الإنترنت للموارد الخارجية التي قد يستخدمها الموقع.
- تعطيل الوصول المباشر إلى ملفات الهاتف من WebView.
- تثبيت Android SDK 35 صراحةً في GitHub Actions.

ملاحظات:
- الناتج Debug APK للتجربة والتثبيت، وليس إصدار Release للنشر على المتجر.
- لم يتم تنفيذ بناء فعلي داخل هذه البيئة؛ نجاح البناء النهائي يتأكد بعد تشغيل GitHub Actions.
