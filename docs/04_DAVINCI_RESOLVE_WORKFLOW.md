# سير عمل DaVinci Resolve

## إعداد المشروع

- أنشئ مشروعًا باسم `Bells_of_Thomas_S01`.
- استخدم مجلدات Media Pool: `00_ADMIN`, `01_VIDEO`, `02_AUDIO_DIALOGUE`, `03_MUSIC`, `04_SFX`, `05_STILLS`, `06_GFX`, `07_EXPORTS`.
- ثبّت معدل الإطارات قبل أول Timeline، ولا تغيّره بعد بدء المونتاج.
- احتفظ بملف مشروع احتياطي وإصدارات مرقمة.

## الاستيراد

1. تحقق من اسم الملف وسجل الأصول.
2. انسخ الوسائط إلى تخزين منظم، أو استخدم Proxy/Optimized Media.
3. طابق الصوت مع الفيديو، ثم أضف metadata للحلقة والمشهد واللقطة.
4. أنشئ Timeline لكل حلقة: `EP01_Master_v01`.

## المراحل

- **Assembly:** ترتيب اللقطات دون تلميع زائد.
- **Rough Cut:** إيقاع، أداء، حذف التكرار.
- **Fine Cut:** انتقالات، استمرارية، عناوين.
- **Picture Lock:** يمنع تغيير الصورة بعد تسليم الصوت إلا بإذن.
- **Color/Fairlight:** تصحيح لوني ومزج حوار/موسيقى/SFX.

## التصدير المقترح

- Master: ProRes/DNxHR حسب بيئة العمل، 16:9، مع الحفاظ على معدل الإطارات الأصلي.
- Review: H.264 أو H.265 بجودة عالية مع burn-in للنسخة ورقمها.
- Audio stems: Dialogue / Music / SFX منفصلة إن أمكن.
- Subtitle: WebVTT وSRT، UTF-8، مع فحص التوقيت يدويًا.

لا ترفع ملفات master الكبيرة إلى Git مباشرة. خزّنها خارجيًا أو عبر Git LFS، وسجل checksum ومسار الأرشيف في `production/asset-register-template.csv`.
