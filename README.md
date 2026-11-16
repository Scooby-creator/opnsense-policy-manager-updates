# opnsense-policy-manager-updates

Windows update distribution for OPNsense Policy Manager. Release assets only; application source is maintained separately.

## تثبيت Windows 6.6.94

[تنزيل OPNsense-Setup-6.6.94.exe](https://github.com/Scooby-creator/opnsense-policy-manager-updates/releases/download/platform-6.6.94/OPNsense-Setup-6.6.94.exe) · [تفاصيل الإصدار](https://github.com/Scooby-creator/opnsense-policy-manager-updates/releases/tag/platform-6.6.94)

ملف تثبيت واحد ذاتي الاحتواء. اختر دور الجهاز: خادم رئيسي أو جهاز إدارة. يفحص النسخ الموجودة ويعرض خطة التثبيت، ويحافظ على الإعدادات، ثم يهيئ قناة التحديث داخل التطبيق. لا يتطلب Python أو .NET أو OpenSSH على جهاز المستخدم.

خطوة المثبّت تحدث تطبيق Windows وعامل التحديث؛ تحفظ Backend الموجود دون إيقافه أو استبدال إعداداته. استبدال Backend وترقية نظام OPNsense يخضعان لفحص وموافقة منفصلين؛ لا يفعّل المثبّت بوابة الدخول أو يغيّر الشبكة.

عند الحاجة لقراءة إعدادات محمية يظهر «استكمال الفحص». اضغطه ووافق على طلب Windows لإتمام القراءة فقط، ثم راجع خطة التثبيت ووافق عليها منفصلًا. إلغاء طلب الصلاحية لا يبدأ تثبيتًا.

يحمل اسم الملف ورأس المثبّت رقم الإصدار نفسه. يوحّد هذا الإصدار فحص الصلاحيات في المثبّت ومحرك المنصة وWindows وBackend، مع التمييز بين المجلد والملف والحفاظ على حماية ملفات التشغيل.

بصمة SHA256 للمثبّت:

```text
a36f07b9d34bbed9aa52585b67f6f2725f6fd54cbc75743db0ed4d4b609d2c86
```

بعد التهيئة افتح «تحديث المنصة». يمكن تنزيل الحزم الموقعة من الإنترنت أو فتح ملف ZIP واحد للتحديث دون الإنترنت. الفحص لا ينزّل أو يثبت تلقائيًا. توقيع حزم المنصة Ed25519 مستقل عن Windows Authenticode.

تستخدم القناة الجديدة إصدارات `platform-*`. يبقى GitHub Latest على `windows-6.6.90` لتوافق العملاء القديمة؛ استخدم رابط المثبّت المحدد أعلاه للانتقال إلى القناة الجديدة.
