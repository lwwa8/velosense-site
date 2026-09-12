# velosense-site

الموقع العام لمشروع **VeloSense** — لوحة قيادة ذكية للدراجات الهوائية.

يُنشر تلقائياً على GitHub Pages عند كل دفع لفرع `main`.

```
index.html      الصفحة التعريفية
map/index.html  خريطة الرياض للدراجات (ملف واحد مكتفٍ بذاته)
.nojekyll       يمنع Jekyll من معالجة ملف الخريطة الكبير
```

## الخريطة

`map/index.html` نسخة **نظيفة** من الكونسول: تستعمل Web Bluetooth و Web Serial
الحقيقيين. لا تضع هنا النسخة المبنية لتطبيق Flutter — تلك محقون فيها شيم يحوّل
`navigator.bluetooth` إلى جسر التطبيق، فيتعطّل البلوتوث بالمتصفح.

المصدر الذي يُحرَّر منه: `Desktop\VeloSense_Console.html`.

## البلوتوث

يحتاج سياقاً آمناً (HTTPS أو localhost) — و GitHub Pages يوفّره.

| المنصة | Web Bluetooth |
|---|---|
| Chrome / Edge على الكمبيوتر | ✅ |
| Chrome على أندرويد | ✅ |
| أي متصفح على iOS | ❌ غير منفَّذ من آبل — استخدم التطبيق الأصلي |

## ربط نطاق مخصص

1. سجّل النطاق عند أي مسجّل.
2. أضفه في Settings ← Pages ← Custom domain (ينشئ ملف `CNAME`).
3. اضبط سجلات الـ DNS، ثم فعّل *Enforce HTTPS* بعد صدور الشهادة.

بيانات الخريطة من [OpenStreetMap](https://www.openstreetmap.org/copyright).
