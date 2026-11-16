# opnsense-policy-manager-updates

Windows update distribution for OPNsense Policy Manager. Release assets only; application source is maintained separately.

## تثبيت Windows 6.6.92

[تنزيل OPNsense-Setup.exe](https://github.com/Scooby-creator/opnsense-policy-manager-updates/releases/download/platform-6.6.92/OPNsense-Setup.exe) · [تفاصيل الإصدار](https://github.com/Scooby-creator/opnsense-policy-manager-updates/releases/tag/platform-6.6.92)

ملف تثبيت واحد ذاتي الاحتواء. اختر دور الجهاز: خادم رئيسي أو جهاز إدارة. يفحص النسخ الموجودة ويعرض خطة التثبيت، ويحافظ على الإعدادات، ثم يهيئ قناة التحديث داخل التطبيق. لا يتطلب Python أو .NET أو OpenSSH على جهاز المستخدم.

خطوة المثبّت تحدث تطبيق Windows وعامل التحديث؛ تحفظ Backend الموجود دون إيقافه أو استبدال إعداداته. استبدال Backend وترقية نظام OPNsense يخضعان لفحص وموافقة منفصلين؛ لا يفعّل المثبّت بوابة الدخول أو يغيّر الشبكة.

عند الحاجة لقراءة إعدادات محمية يظهر «استكمال الفحص». اضغطه ووافق على طلب Windows لإتمام القراءة فقط، ثم راجع خطة التثبيت ووافق عليها منفصلًا. إلغاء طلب الصلاحية لا يبدأ تثبيتًا.

بصمة SHA256 للمثبّت:

```text
ee578a742c1acf7d2c4e71ac1243bb4bbdf029605ac25fb06aeb9b77e6a35624
```

بعد التهيئة افتح «تحديث المنصة». يمكن تنزيل الحزم الموقعة من الإنترنت أو فتح ملف ZIP واحد للتحديث دون الإنترنت. الفحص لا ينزّل أو يثبت تلقائيًا. توقيع حزم المنصة Ed25519 مستقل عن Windows Authenticode.

تستخدم القناة الجديدة إصدارات `platform-*`. يبقى GitHub Latest على `windows-6.6.90` لتوافق العملاء القديمة؛ استخدم رابط المثبّت المحدد أعلاه للانتقال إلى القناة الجديدة.
