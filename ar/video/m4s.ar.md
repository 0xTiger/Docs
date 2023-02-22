{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف M4S - ما هو ملف M4S؟",
  "description":"تعرف على تنسيق ملف M4S وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات M4S وفتحها." ,
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
} ,
  "lastmod" : "2022-07-18"
}

## ما هو ملف M4S؟

ملف M4S هو جزء صغير من مقطع فيديو يتم دفقه عبر الإنترنت باستخدام تقنية البث ** MPEG-DASH **. يحتوي على مقطع فيديو في شكل بيانات ثنائية. يقوم التطبيق المستلم (عادةً متصفح الويب أو مشغلات الوسائط) بتشغيل هذه الأجزاء بالترتيب الذي تم استلامها به. يتم تحديد مقطع M4S الأول من خلال بيانات التهيئة التي يحتوي عليها. في ** الملخص ** ، ملفات M4S عبارة عن مقاطع وسائط فردية صغيرة من ملف كامل.

## تنسيق ملف M4S

تستند ملفات M4S إلى [تنسيق ملف الوسائط الأساسي ISO (ISOBMFF)] (https://www.w3.org/TR/mse-byte-stream-format-isobmff/). يمكن تنزيل هذه الأجزاء الصغيرة من ملف كبير بشكل مستقل عبر HTTP. وبالتالي ، إذا كان لديك ملف فيلم كبير [MP4] (/ar/ video / mp4 /) ، فيمكن دفقه باستخدام تقنية MPEG-DASH (دفق ديناميكي متكيف عبر HTTP) عن طريق تقسيمه كملفات مقطع M4S. إذا تم تنزيل ملف الفيلم الكبير هذا على قرص كـ M4S ، فسيتم تنزيل ملفات M4S متعددة. إذا كانت كل مقاطع .m4s متسلسلة ، يتم إنتاج ملف كامل قابل للتشغيل. لا يمكن لمشغلات الوسائط تشغيل الملف ما لم يكن مقطع التهيئة الأول متاحًا أيضًا مع الملف.

## حول دفق MPEG-DASH

يستخدم MPEG-DASH تقنية دفق معدل البت التكيفي التي تجعل من الممكن دفق محتوى وسائط عالي الجودة عبر الإنترنت. يتم ذلك عن طريق تقسيم المحتوى إلى سلسلة من المقاطع الصغيرة التي يتم دفقها عبر HTTP. يمكن دفق ملفات الوسائط الكبيرة مثل الأفلام أو البودكاست أو البث المباشر لحدث رياضي بهذه الطريقة. يتم ترميز هذه المقاطع بمعدلات بت مختلفة. تقوم مشغلات الوسائط التي تم تمكين MPEG-DASH تلقائيًا بتحديد المقطع الذي يحتوي على أعلى معدل بت باستخدام خوارزمية تكيف معدل البت. هذا يتجنب المماطلة أو إعادة التخزين المؤقت للأحداث في التشغيل.

### واجهة برمجة تطبيقات مفتوحة المصدر لملفات M4S

تتوفر واجهات برمجة تطبيقات مفتوحة المصدر يمكن استخدامها لقراءة ملفات M4S وتحويلها.

* [libdash] (https://github.com/bitmovin/libdash) - واجهة برمجة تطبيقات .NET لملفات M4S
* [dash.js] (https://github.com/Dash-Industry-Forum/dash.js) - عميل جافا سكريبت لملف M4S
* [اذهب إلى المكتبة لإنشاء ملفات داش] (https://github.com/zencoder/go-dash)

### واجهة برمجة تطبيقات مفتوحة المصدر لتحويل M4S إلى MP4

* [MFourStoMp4] (https://github.com/muri11o/mfourstomp4)

## مراجع ###

* [تنسيق ملف وسائط ISO الأساسي (ISOBMFF)] (https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [البث الديناميكي التكيفي عبر HTTP - MPEG-DASH] (https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)
