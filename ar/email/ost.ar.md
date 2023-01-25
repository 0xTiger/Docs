{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"OST - تنسيق ملف تخزين Outlook" ,
  "description":"تعرف على تنسيق ملف OST وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات OST وفتحها." ,
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف OST؟

تمثل ملفات OST أو Offline Storage بيانات صندوق بريد المستخدم في وضع عدم الاتصال على الجهاز المحلي عند التسجيل مع Exchange Server باستخدام Microsoft Outlook. يتم إنشاؤه تلقائيًا عند أول استخدام لبرنامج Microsoft Outlook عند الاتصال بالخادم. بمجرد إنشاء الملف ، تتم مزامنة البيانات مع خادم البريد الإلكتروني بحيث تكون متاحة في وضع عدم الاتصال وكذلك في حالة قطع الاتصال بخادم البريد الإلكتروني. يمكن لملفات OST استخدام عناصر صندوق البريد مثل رسائل البريد الإلكتروني وجهات الاتصال ومعلومات التقويم والملاحظات والمهام وغيرها من البيانات المماثلة. يمكن للمستخدمين إنشاء رسائل بريد إلكتروني وعناصر بيانات أخرى في ملف OST حتى في حالة عدم وجود اتصال بالخادم ، ولكن لن تتم مزامنتها مع الخادم. بمجرد إنشاء الاتصال ، تتم مزامنة الملف المحلي مع الخادم مرة أخرى بحيث يكون كل من الخادم والنسخة المحلية على نفس مستوى المعلومات.

## تنسيق ملف OST

يتكون تنسيق ملف OST (جدول التخزين غير المتصل) و [PST] (/ar/ email / pst /) (جدول التخزين الشخصي) من تنسيق ملف المجلد الشخصي (PFF) الذي يتوافق مع تخزين رسائل البريد الإلكتروني وجهات الاتصال والمواعيد الخاصة بالمستخدم. يتم تخزين البيانات في ملف PFF في لغة صغيرة مع تمثيل جميع التواريخ والأوقات على أنها FILETIME بالتوقيت العالمي المنسق. يحدد [MS-PST] نوعين من PFF:

* تنسيق ANSI 32 بت
* تنسيق Unicode 64 بت

تنسيق ملف PST [المواصفات] (https://msdn.microsoft.com/en-us/library/ff385210 (v # office.12) .aspx) ، كما هو متاح من Microsoft ، ينطبق أيضًا على تنسيق ملف OST باعتباره مجانيًا و ترخيص براءات الاختراع غير القابل للإلغاء من خلال وعد المواصفات المفتوحة. يتكون من العناصر التالية المميزة:

* رأس فل
* بيانات رأس الملف
* عقدة فرع الفهرس
* عقدة طرفية الفهرس
* (ملف) فهرس الإزاحة
* فهرس واصف (العنصر)
* الواصفات المحلية
* نوع جدول الصنف

### معلومات الرأس

توجد بنية HEADER لملف OST في بداية الملف عند 0 إزاحة. يحتوي على معلومات بيانات وصفية حول ملف OST ومعلومات ROOT للوصول إلى هياكل بيانات طبقة NDB الموضحة أعلاه. تختلف بنية HEADER بالنسبة لإصدارات Unicode و ANSI من تنسيق ملف OST.

يبدأ الرأس بكلمة سحرية من 4 بايت **! BDN ** ممثلة بالبايتات (0x21 ، 0x42 ، 0x44 ، 0x4E). يوجد رقم سحري آخر من 2 بايت ، ** SM ** (0x53 ، 0x4D) ، عند الإزاحة 8 من بداية الملف. معلومات الإصدار (ANSI أو Unicode) تقع في إزاحة 10 من بداية الملف. تحدد قيمة Hex (0x17) ملف Unicode OST بينما يمثل 0x0E أو 0x0F تنسيق ملف ANSI.

| الحقل | الوصف
---|---|
| dwMagic (4 بايت) | يجب أن يكون "{0x21، 0x42، 0x44، 0x4E} ("! BDN ")"
| dwCRCPartial (4 بايت) | قيمة CRC 32 بت لـ 471 بايت من البيانات بدءًا من wMagicClient (0ffset 0x0008)
| wMagicClient (2 بايت) | يجب أن يكون "{0x53، 0x4D}".
| wVer (2 بايت) | إصدار تنسيق الملف. يجب أن تكون هذه القيمة 14 أو 15 إذا كان الملف عبارة عن ملف ANSI PST ، ويجب أن تكون 23 إذا كان الملف هو ملف Unicode PST.
| wVerClient (2 بايت) | إصدار تنسيق ملف العميل. الإصدار الذي يتوافق مع التنسيق الموضح في هذا المستند هو 19. يجب على منشئو ملف PST جديد بناءً على هذا المستند تهيئة هذه القيمة إلى 19.
| bPlatformCreate (1 بايت) | يجب تعيين هذه القيمة على 0x01.
| bPlatformAccess (1 بايت) | يجب تعيين هذه القيمة إلى 0x01.
| dw محفوظة (8 بايت) |
| bidUnused (8 بايت Unicode فقط) | تمت إضافة حشوة غير مستخدمة عند إنشاء تنسيق ملف Unicode PST.
| bidNextP (Unicode: 8 بايت ؛ ANSI: 4 بايت) | الصفحة التالية BID. تحتوي الصفحات على عداد خاص لتخصيص قيم مؤشر العطاءات. يتم تخصيص قيمة bidIndex لصفحات BID من هذا العداد.
| bidNextB (4 بايت ANSI فقط): | BID التالي. هذه القيمة هي العداد الرتيب الذي يشير إلى تعيين BID للكتلة المخصصة التالية. تتقدم قيم BID بزيادات قدرها 4. لمزيد من التفاصيل ، انظر القسم 2.2.2.2.
| dwUnique (4 بايت) | هذه قيمة تتزايد بشكل رتيب ويتم تعديلها في كل مرة يتم فيها تعديل بنية HEADER لملف PST. وظيفة هذه القيمة هي توفير قيمة فريدة ، والتأكد من أن HEADER CRCs مختلفة بعد كل تعديل في الرأس.
| rgnid [] (128 بايت) | مصفوفة ثابتة من 32 NID ، كل منها يتوافق مع واحد من 32 NID_TYPEs الممكنة (NID_TYPE ، NID_TYPE_NORMAL_FOLDER ، NID_TYPE_SEARCH_FOLDER ، NID_TYPE_NORMAL_MESSAGE ، NID_TYPE_ASSOC_MESSAGE)
| qwUnused (8 بايت) | مساحة غير مستخدمة ؛ يجب ضبطه على الصفر. تنسيق ملف Unicode PST فقط.
| الجذر (Unicode: 72 بايت ؛ ANSI: 40 بايت) | بنية الجذر (القسم 2.2.2.5).
| dwAlign (4 بايت) | بايت محاذاة غير مستخدمة ؛ يجب ضبطه على الصفر. تنسيق ملف Unicode PST فقط.
| rgbFM (128 بايت) | إيقاف FMap. لم يعد هذا مستخدمًا ويجب ملؤه بـ 0xFF. يجب على القراء تجاهل قيمة هذه البايتات.
| rgbFP (128 بايت) | FPMap موقوف. لم يعد هذا مستخدمًا ويجب ملؤه بـ 0xFF. يجب على القراء تجاهل قيمة هذه البايتات.
| bSentinel (1 بايت) | يجب تعيينه على 0x80.
| bCryptMethod (1 بايت) | يشير إلى كيفية تشفير البيانات داخل ملف PST. يجب تعيينها على إحدى القيم المحددة مسبقًا (NDB_CRYPT_NONE ، NDB_CRYPT_PERMUTE ، NDB_CRYPT_CYCLIC).
| rgb محفوظة (2 بايت) | محجوز؛ يجب ضبطه على الصفر.
| bidNextB (8 بايت) | يشير إلى قيمة BID التالية المتوفرة. تنسيق ملف Unicode PST فقط.
| bidNextB (Unicode فقط: 8 بايت) | BID التالي. هذه القيمة هي العداد الرتيب الذي يشير إلى تعيين BID للكتلة المخصصة التالية. تتقدم قيم BID بزيادات قدرها 4. لمزيد من التفاصيل ، انظر القسم 2.2.2.2.
| dwCRCFull (4 بايت) | قيمة CRC 32 بت لـ 516 بايت من البيانات بدءًا من wMagicClient إلى bidNextB ، ضمناً. تنسيق ملف Unicode PST فقط.
| محجوز (8 بايت) | محجوز ؛ يجب ضبطه على الصفر. تنسيق ملف ANSI PST فقط.
| dw محجوز (4 بايت) | محجوز ؛ يجب ضبطه على الصفر. تنسيق ملف ANSI PST فقط.
| rgbReserved2 (3 بايت) |
| ب محفوظة (1 بايت) |
| rgbReserved3 (32 بايت) |

## مراجع

* [تنسيق ملف مجلدات Outlook الشخصية (.ost)] (https://msdn.microsoft.com/en-us/library/ff385210 (v # office.12) .aspx)
* [مواصفات تنسيق ملف المجلد الشخصي] (https://github.com/libyal/libpff/blob/master/documentation/Personal٪20Folder٪20File٪20 (PFF)٪ 20format.asciidoc)
