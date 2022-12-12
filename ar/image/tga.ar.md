{
  "date" : "2019-10-11",
  "keywords" :["ملف tga" , "تنسيق ملف tga" , "ما هو ملف tga" , "ملف" , "tga مثال" , "امتداد ملف tga" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف TGA - ملف صورة رسومية من TARGA" ,
  "description":"تعرف على تنسيق ملف TGA وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات TGA وفتحها." ,
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف TGA؟

الملف ذو الامتداد .tga هو تنسيق رسومي نقطي تم إنشاؤه بواسطة Truevision Inc. وقد تم تصميمه للوحات TARGA (محول Truevision Advanced Raster) وقدم دعم عرض Highcolor / truecolor لأجهزة الكمبيوتر المتوافقة مع IBM. وهو يدعم 8 و 16 و 24 و 32 بت لكل بكسل وقناة ألفا 8 بت. كما أنه يدعم ضغط RLE بدون فقدان والذي يمكن تطبيقه لتقليل حجم الصورة. تستخدم الصور والأنسجة الرقمية تنسيق صورة TGA.

## نبذة تاريخية

ظهر تشكيل تنسيق ملف TGA في عام 1984 بواسطة AT&T EPICenter (تم استخراجه وتشكيله لاحقًا ككيان مستقل يُعرف باسم Truevision) والذي كان يعمل على تسويق التقنيات الجديدة التي طورتها AT&T للمخازن المؤقتة للإطارات الملونة. كان EPICenter يعمل بالفعل على أول بطاقتين ، VDA (محول عرض الفيديو) و ICB (لوحة التقاط الصور) التي تعمل على نوعين من الملفات ، vda و. icb ، قيد التشغيل بالفعل. تم تقنين تنسيقات الملفات هذه وتم تقديم تنسيق TGA أقل نطاقًا محددًا. كان TGA امتدادًا لما كان مستخدمًا بالفعل ، وقدم معلومات مثل العرض والارتفاع وعمق البكسل وخريطة الألوان المرتبطة وأصل الصورة.

يتضمن الإصدار 2.0 من TGA ، المنشور في عام 1989 ، العديد من الميزات المحسنة مثل:

* الصور المصغرة
* قناة ألفا
* قيمة جاما
* البيانات الوصفية النصية

من بين المساهمين الرئيسيين في إصدار TGA 2.0 من Truevision's Shawn Steiner و Kevin Fiedly و David Spoelstra.

## مواصفات تنسيق ملف TGA TARGA

يتكون ملف TGA من جزأين رئيسيين:

* رأس
* معلومات Color Pixel

جميع القيم الموجودة في ملف TGA مكتوبة بأحرف صغيرة وفقًا لمواصفات التنسيق.

### رأس TGA

يتكون رأس ملف TGA من الحقول الخمسة التالية.

| رقم الحقل | الطول | اسم الحقل | الوصف |
---|---|---|---|
| 1 | 1 بايت | طول المعرف | طول حقل معرف الصورة (0-255) |
| 2 | 1 بايت | نوع خريطة اللون | ما إذا كانت خريطة الألوان مضمنة (0 - تشير إلى عدم وجود بيانات لخريطة الألوان مضمنة في هذه الصورة. 1 - تشير إلى أن خريطة الألوان مضمنة في هذه الصورة.) |
| 3 | 1 بايت | نوع الصورة | أنواع الضغط والألوان (0- لا توجد بيانات للصورة. 1- صورة غير مضغوطة ، ملونة مخططة ، 2- غير مضغوطة ، صورة ملونة حقيقية ، 9- طول التشغيل مشفر ، صورة معينة بالألوان ، 11- طول التشغيل مشفر ، صورة بالأبيض والأسود ) |
| 4 | 5 بايت | مواصفات خريطة اللون | يصف خريطة الألوان |
| 5 | 10 بايت | مواصفات الصورة | أبعاد الصورة وشكلها |

### بيانات خريطة الصور واللون

| حقل لا. | الطول | الحقل | الوصف |
---|---|---|---|
| 6 | من حقل طول معرف الصورة | معرف الصورة | حقل اختياري يحتوي على معلومات تعريف |
| 7 | من حقل مواصفات مخطط الألوان | بيانات خريطة اللون | جدول بحث يحتوي على بيانات خريطة اللون |
| 8 | من حقل مواصفات الصورة | بيانات الصورة | مخزنة وفقًا لواصف الصورة |

### منطقة المطور (اختياري)

يوفر الإصدار 2.0 من TGA دعمًا لمزيد من التحسينات / الإضافات التي أراد العديد من المطورين تخزين المزيد من المعلومات. المعلومات اختيارية بحيث إذا لم يكن مفكك الشفرة TGA قادرًا على تفسيرها ، فسيتم تجاهلها.

### منطقة الامتداد (اختياري)

| رقم الحقل | الطول | الحقل | الوصف |
---|---|---|---|
| 10 | 2 بايت | حجم الامتداد | الحجم بالبايت من منطقة الامتداد ، دائمًا 495 |
| 11 | 41 بايت | اسم المؤلف | اسم المؤلف. إذا لم يتم استخدامها ، يجب تعيين البايت على NULL (\ 0) أو مسافات |
| 12 | 324 بايت | تعليق المؤلف | تعليق منظم في أربعة أسطر ، كل منها يتكون من 80 حرفًا بالإضافة إلى NULL |
| 13 | 12 بايت | طابع التاريخ / الوقت | تاريخ ووقت إنشاء الصورة |
| 14 | 41 بايت | معرف الوظيفة ||
| 15 | 6 بايت | وقت العمل | الساعات والدقائق والثواني التي تم قضاؤها في إنشاء الملف (للفواتير ، وما إلى ذلك) |
| 16 | 41 بايت | معرّف البرنامج | التطبيق الذي أنشأ الملف. |
| 17 | 3 بايت | إصدار البرنامج ||
| 18 | 4 بايت | لون المفتاح ||
| 19 | 4 بايت | نسبة أبعاد البكسل ||
| 20 | 4 بايت | قيمة جاما ||
| 21 | 4 بايت | إزاحة تصحيح اللون | عدد البايت من بداية الملف إلى جدول تصحيح الألوان إن وجد |
| 22 | 4 بايت | طابع بريدي | عدد البايتات من بداية الملف إلى صورة الطابع البريدي إن وجدت |
| 23 | 4 بايت | مسح خط الإزاحة | عدد البايتات من بداية الملف إلى جدول خطوط المسح إن وجدت |
| 24 | 1 بايت | نوع السمات | يحدد قناة ألفا |

### تذييل الملف (اختياري)

يمثل آخر 26 بايت من الملف التذييل ، والذي إذا كان موجودًا يعني أنه من المحتمل أن يكون ملف الإصدار 2 من TGA.

| رقم الحقل | الطول | الحقل | الوصف |
---|---|---|---|
| 28 | 4 بايت | الإزاحة | الإزاحة بالبايت من بداية الملف |
| 29 | 4 بايت | إزاحة منطقة المطور | الإزاحة بالبايت من بداية الملف |
| 30 | 16 بايت | التوقيع | يحتوي على "TRUEVISION-XFILE" |
| 31 | 1 بايت | | يحتوي على "." |
| 32 | 1 بايت | | يحتوي على NULL |


## مراجع

* [مواصفات تنسيق ملف TGA 2.0] (https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf؟default=view&preview = true.pdf)
* [TGA by Wikipedia] (https://en.wikipedia.org/wiki/Truevision_TGA)
