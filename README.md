# محسّن — Android Java + HTML/CSS/JavaScript

هذه نسخة أساس محلية قابلة للفتح في Android Studio. الواجهة عربية RTL وتعمل دون خادم: اختيار صورة أو فيديو، معاينة، تعديلات إضاءة/تباين/تشبع، وإعادة ضبط. لا تسمي هذه التعديلات ذكاءً اصطناعيًا.

## التشغيل
1. افتح المجلد في Android Studio.
2. استخدم Android SDK 35 وJDK 17 أو 21.
3. نفّذ `./gradlew assembleDebug` بعد إضافة Gradle Wrapper أو استخدم Gradle من Android Studio.
4. ثبّت `app/build/outputs/apk/debug/app-debug.apk` على جهاز Android 8+.

## ما هو جاهز
- Android Native Java.
- WebView آمن نسبيًا مع JavaScript bridge.
- اختيار ملفات من الجهاز وصورة/فيديو.
- RTL ووضع ليلي وتصميم متجاوب.
- نقطة Native باسم `NativeBridge` لتشخيص الجهاز ورسائل التطبيق.

## ما لم أفعّله عمدًا
رفع الدقة Real-ESRGAN، رفع الفريمات RIFE، إزالة الضبابية، Whisper، وإخراج فيديو كامل ليست موجودة في هذه النسخة؛ لا يصح الادعاء بأنها تعمل قبل إضافة ملفات النماذج ومحركات ONNX/NCNN وMediaCodec واختبارها على أجهزة فعلية.

## المرحلة التالية
إضافة `ModelManager` لتنزيل/التحقق من نماذج ONNX محليًا، ثم وحدة Kotlin/Java لمعالجة الصور بالبلاطات والذاكرة، وبعدها MediaCodec للفيديو. نسخة iPhone تحتاج مشروع Swift/Core ML مستقلًا أو Flutter.
