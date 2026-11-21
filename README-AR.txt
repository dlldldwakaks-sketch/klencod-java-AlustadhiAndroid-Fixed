إصلاح مشروع تطبيق الأستاذي

سبب الخطأ السابق:
كان GitHub Actions يشغّل Gradle داخل مجلد لا يحتوي على settings.gradle أو build.gradle.
هذه الحزمة تضيف مشروع Android حقيقياً وتضع ملف HTML الأصلي داخل assets دون تعديل محتواه.

طريقة الاستخدام:
1) ارفع محتويات هذا المجلد إلى جذر مستودع GitHub (بحيث يظهر settings.gradle في الجذر).
2) تأكد أن ملف .github/workflows/android.yml موجود في المسار نفسه.
3) افتح GitHub > Actions > Build Android APK > Run workflow.
4) بعد نجاح البناء افتح نتيجة التشغيل ثم Artifacts ونزّل alustadhi-debug-apk.
5) فك ZIP وثبّت app-debug.apk على هاتف Android.

معرّف التطبيق: com.alustadhi.app
ملاحظة: هذا إصدار Debug للتجربة والتثبيت المباشر، وليس إصداراً موقعاً للنشر على Google Play.
