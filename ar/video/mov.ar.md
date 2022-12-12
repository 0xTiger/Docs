{
  "date" : "2019-10-11",
  "keywords" :["mov file", "mov file format", "what is a mov file", "file", "mov example", "mov file extension", "extension", "format", "QuickTime", "MPEG- 4 "] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف MOV - تنسيق ملف أفلام Apple QuickTime" ,
  "description":"تعرف على تنسيق ملف MOV وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات MOV وفتحها." ,
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
} ,
  "lastmod" : "2021-07-29"
}

## ما هو ملف MOV؟

ملف MOV هو نوع ملف فيديو ، تم تطويره بواسطة شركة Apple Inc. ، ويحتوي على مسار واحد أو أكثر. يخزن كل مسار فيلمًا وصوتًا ومقاطع فيلم وترجمات. إنها حاوية وسائط متعددة يمكنها تخزين أنواع مختلفة من عناصر الوسائط. يتوافق تنسيق الفيديو MOV مع أنظمة Windows و Macintosh. يستخدم MPEG-4 المشفر للضغط ويتم الاحتفاظ بالمسارات في كائنات تسمى الذرات والتي يتم وضعها في بنية بيانات هرمية.

## تاريخ موجز لتنسيق ملف MOV

تم تطوير تنسيق ملف MPEG-4 من مواصفات تنسيق ملف QuickTime (** QTFF **) في عام 2001. وافقت المنظمة الدولية للتوحيد القياسي على التنسيق وتم نشر مواصفات أنظمة MPEG-4 الجزء 1 في عام 1999. في عام 2001 ، ملف مراجعة تم نشر التنسيق [MP4] (/ar/ video / mp4 /).

تمت مراجعة الإصدار الأول من MP4 في عام 2003 باعتباره MPEG-4 الجزء 14 (ISO / IEC 14496-14: 2003). في عام 2004 ، تم تعميم MP4 لتحديد هيكل عام لجميع ملفات الوسائط المستندة إلى الوقت. لذلك ، يتم استخدامه الآن كأساس للعديد من تنسيقات ملفات الوسائط المتعددة الأخرى.

## تنسيق ملف كويك تايم (QTFF) - مزيد من المعلومات

من أجل العمل مع الوسائط المتعددة الرقمية ، يمكن لـ QTFF الاحتفاظ بأنواع عديدة من البيانات. إنه تنسيق فكرة لتبادل الوسائط الرقمية حيث يحدد التنسيق المعايير لوصف أي نوع من هياكل الوسائط. يتكون تنسيق الملف من مجموعة مرنة من الكائنات الموجهة. لتخزين الأفلام على الأقراص ، يستخدم QuickTime بنيتين ، أي "ذرات" و "ذرات كيو تي".

### الذرات

Atom هي الوحدة الأساسية لملف QuickTime. يوجد حقلين رئيسيين في أي ذرة قبل أي حقل آخر: حقلا الحجم والنوع. يُظهر حقل الحجم حجم الذرة بينما يشير حقل النوع إلى نوع البيانات المخزنة في الذرة. بطبيعتها ، الذرات هرمية مما يعني أن ذرة واحدة يمكن أن تحتوي على ذرات أخرى يمكن أن تحتوي على ذرات أخرى. يظهر تخطيط ذرة العينة في الصورة التالية.

تتكون كل ذرة من جزأين ، "رأس" و "بيانات". يحتوي الرأس على حقلي الحجم والنوع ويحتوي جزء البيانات على البيانات الفعلية. علاوة على ذلك ، يتم شرح كل مجال أدناه:

### حجم الذرة

يُشار إلى رأس الذرة ومحتوياتها بعدد صحيح 32 بت يُعرف باسم حجم الذرة. يحتوي حقل الحجم على حجم الذرة بالبايت ، معبرًا عنه في عدد صحيح بدون إشارة يبلغ 32 بت.

### نوع الذرة

يتم عرض نوع الذرة أيضًا بواسطة عدد صحيح 32 بت ، والذي يتم التعامل معه في الغالب كحقل مكون من أربعة أحرف مع قيمة متقنة ، مثل "moov" (0x6D6F6F76) لذرة فيلم ، أو "trak" (0x7472616B) لـ ذرة مسار. بمجرد معرفة نوع الذرة ، فإنه يسمح بتفسير بياناته.

### حاويات QT Atoms و Atom

توفر ذرات QT تنسيق تخزين للأغراض العامة ولها رأس ممتد يتكون من حقول الحجم والنوع ومعرف Atom وعدد الذرات التابعة. يتم تغليف ذرات QT في حاوية ذرة ، وهي بنية بيانات فريدة لها رأس مع عدد قفل. توجد ذرة جذر واحدة في كل حاوية ذرة وهي ذرة كيو تي. يظهر تخطيط ذرة QT في الشكل أدناه.

يحتوي رأس حاوية QT atom على البيانات التالية:

محجوز: عنصر 10 بايت بقيمة 0.

عدد القفل: عدد صحيح 16 بت بقيمة 0.

تحتوي رؤوس QT atom على البيانات التالية:

** الحجم - ** يشار إلى رأس QT atom ومحتوياته بالبايت بواسطة عدد صحيح 32 بت. في حالة ذرة الورقة ، فإن هذا الحقل يحتوي على حجم ذرة واحدة.

** النوع - ** يُشار إلى نوع الذرة بعدد صحيح 32 بت. في حال كانت ذرة الجذر ، يتم تعيين القيمة على "sean".

** معرّف Atom - ** هو رقم صحيح 32 بت يُظهر معرّف الذرة ويجب أن يكون فريدًا لجميع الأشقاء. ذرة الجذر دائمًا هي قيمة معرّف atom على أنها 1.

** محجوز - ** عدد صحيح 16 بت يجب ضبطه على 0.

** عدد الأطفال - ** عدد صحيح 16 بت يشير إلى عدد ذرات الطفل في الذرة.

** محجوز - ** عدد صحيح 32 بت يجب ضبطه على 0.

## بنية ملف ملفات MOV

تتكون ملفات MOV من أجزاء متتالية. يحتوي كل مقطع على رأس 8 بايت: حجم مقطع 4 بايت (كبير النهاية ، مرتفع البايت أولاً) ونوع مقطع مكون من 4 بايت - أحد التوقيعات المحددة مسبقًا: "ftyp" ، "mdat" ، "moov" ، "pnot "،" udta "،" uuid "،" moof "،" free "،" skip "،" jP2 "،" wide "،" load "،" ctab "،" imap "،" matt "،" kmat "، "clip" ، "crgn" ، "sync" ، "chap" ، "tmcd" ، "scpt" ، "ssrc" ، "PICT". القطعة الأولى من النوع "ftype" ولها نوع فرعي عند الإزاحة 8. MOV معرّفة بالنوع الفرعي الذي يجب أن يكون "qt". لتكوين ملف MOV ، يلزم تكرار الأجزاء حتى يتم اكتشاف نوع غير معروف.

إليك "مثال نموذجي": فحص عينة من البيانات الثنائية لملف MOV ، من الواضح أنه يبدأ بالتوقيع ** ftyp ** (hex: 66 74 79 70) عند الإزاحة 4 ، والتي تحدد QuickTime Container File Type. نوع الملف الفرعي هو ** qt ~ _ ~ _ ** (hex: 71 74 20 20) مما يشير إلى نوع ملف MOV. حجم الكتلة الأول هو 32 (hex: 00 00 00 20 ، كبير النهاية ، البايت العالي أولاً) ، الحجم الموجود عند الإزاحة 0. عند الإزاحة 32 (hex: 20) يقع الجزء الثاني ، الذي يبلغ حجمه 8 و اكتب ** mdat ** (عرافة: 6D 64 61 74).

تقع القطعة التالية عند الإزاحة 32 + 8 # 40 (ست عشري: 28) ولها حجم 3،263،028 (ست عشري: 00 31 CA 34) ونوع ** mdat ** (ست عشري: 6D 64 61 74) عند الإزاحة 44 (ست عشري : 2 ج). تقع القطعة التالية عند الإزاحة 40 + 3،263،028 # 3،263،068 (عرافة: 00 31 CA 5C) ولها حجم 21189 (ست عشري: 00 00 52 C5) واكتب ** مووف ** (ست عشري: 6D 6F 6F 76) عند الإزاحة 1،836،019،574 (عرافة: 00 31 CA 60). هذا هو الجزء الأخير ، لذا فإن الحجم الإجمالي للملف هو 3،263،068 + 21،189 # 3،284،257 بايت.

## كيفية تحويل ملف MOV؟

هناك الكثير من مشغلات الوسائط وبرامج تحرير الفيديو المتاحة لتحويل ملفات MOV إلى تنسيقات ملفات الفيديو الشائعة الأخرى. تتضمن بعض مشغلات الوسائط التي يمكنها تحويل ملفات MOV إلى تنسيقات أخرى ما يلي:

* مشغل وسائط VideoLAN VLC
* عازف Eltima Elmedia

يمكن للعديد من مشغلات الوسائط وبرامج تحرير الفيديو ، بما في ذلك مشغل وسائط VideoLAN VLC و Eltima Elmedia Player ، تحويل ملفات MOV إلى تنسيقات أخرى. يمكن لهذه البرامج تحويل ملفات MOV إلى تنسيقات الفيديو التالية.

* فيديو MPEG-4 - [MP4] (/ar/ فيديو / mp4 /)
* فيديو WebM - [WEBM] (/ar/ video / webm /)
* دفق نقل الفيديو - [TS] (/ar/ video / ts /)
* تنسيق الأنظمة المتقدم - [ASF] (/ar/ video / ts /)
* Ogg Vorbis Audio - [OGG] (/ar/ audio / ogg /)
* صوت MP3 - [MP3] (/ar/ صوت / mp3 /)
* برنامج ترميز الصوت بدون فقدان البيانات - [FLAC] (/ar/ audio / flac /)
* WAVE Audio - [WAV] (/ar/ audio / wav /)

## Open Source API لملفات MOV

* [React Native API لتحويل MOV إلى MP4] (https://github.com/taltultc/react-native-mov-to-mp4)
* [Python API لإصلاح ملفات MOV] (https://github.com/nrosenstein-stuff/movrepair)
* [Ruby API لتحويل MOV إلى GIF] (https://github.com/skygroundmedia/convert-mov-to-gif)

## مراجع

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)
