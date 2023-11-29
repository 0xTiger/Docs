{
"التاريخ": "27-09-2023",
  "keywords": [
"سي إف جي",
"ملف سي إف جي",
"ملف التكوين cfg mame",
"ما هو ملف cfg",
"كيفية فتح ملف سي إف جي",
"ملف",
"امتداد الملف cfg",
"امتداد"
],
  "author": {
"display_name": "شكيل فايز"
},
"draft": "false",
"toc": true,
"title": "تنسيق ملف CFG - ملف تكوين MAME",
  "description":"تعرف على تنسيق ملف التكوين CFG MAME وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CFG وفتحها.",
"linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
"parent": "الإعدادات"
}
},
"آخر مود": "27-09-2023"
}

## ما هو ملف CFG؟

ملف CFG هو ملف تكوين لوحة مفاتيح XML تستخدمه برامج محاكاة ألعاب الفيديو MAME arcade. يعد هذا مكونًا حاسمًا لتخصيص عناصر التحكم في لوحة المفاتيح ومفاتيح التشغيل السريع لتناسب تفضيلات اللاعب. تقوم هذه الملفات بتخزين التعيينات والإعدادات التي تحدد كيفية تفاعل لوحة المفاتيح مع المحاكي أثناء تشغيل اللعبة. من خلال تحرير هذا الملف, يمكن للمستخدمين تخصيص تجربة الألعاب الخاصة بهم عن طريق تعيين مفاتيح لوحة مفاتيح محددة للإجراءات داخل اللعبة, مثل إدخال العملة المعدنية والبدء والحركة ووظائف أخرى متنوعة.

## ملف التكوين MAME

MAME, الذي يرمز إلى **Multiple Arcade Machine Emulator**, هو تطبيق برمجي يسمح لك بمحاكاة ألعاب الأركيد وتشغيلها على جهاز الكمبيوتر الخاص بك. يستخدم MAME ملفات التكوين لتخصيص سلوكه وإعداداته. توجد ملفات التكوين هذه عادةً في مجلد "cfg" داخل دليل MAME الخاص بك.

فيما يلي ملفات التكوين الرئيسية التي قد تواجهها عند إعداد MAME وتكوينه:

1. **mame.ini:** هذا هو ملف التكوين الرئيسي لـ MAME. يحتوي على إعدادات عامة تنطبق على جميع الألعاب. يمكنك العثور على هذا الملف في الدليل الجذر لتثبيت MAME الخاص بك.

1. **default.cfg:** يخزن هذا الملف الإعدادات الافتراضية لجميع الألعاب التي لا تحتوي على ملفات تكوين خاصة بها. يتم استخدامه كبديل للإعدادات الخاصة باللعبة.

1. **game-special.cfg:** تُستخدم هذه الملفات لتخزين إعدادات الألعاب الفردية. يتم تسميتها عادةً على اسم ملف ROM الخاص باللعبة التي تتوافق معها. على سبيل المثال, إذا كانت لديك لعبة تسمى "pacman.zip", فسيكون ملف التكوين الخاص بها هو "pacman.cfg."

فيما يلي بعض الإعدادات الشائعة التي قد تجدها في ملف تكوين MAME.

1. **rompath:** يحدد الدليل الذي توجد به ROM الخاصة بلعبة الآركيد.

1. **cfg_directory:** يحدد الدليل الذي يتم فيه تخزين ملفات التكوين الخاصة باللعبة.

1. **nvram_directory:** يحدد الدليل الذي يتم فيه تخزين ملفات ذاكرة الوصول العشوائي (NVRAM) غير المتطايرة. تقوم NVRAM بتخزين النتائج العالية والبيانات الأخرى الخاصة باللعبة.

1. **artwork_directory:** يحدد الدليل الذي يتم فيه تخزين ملفات العمل الفني (مثل الحواف, والسرادقات, والنشرات الإعلانية).

1. **samplepath:** يحدد الدليل الذي توجد به ملفات الصوت النموذجية.

1. ** مسار الغش: ** يحدد الدليل الذي توجد به ملفات الغش.

يمكنك أيضًا تكوين العديد من الإعدادات الأخرى مثل خيارات الفيديو والصوت وعناصر التحكم وأجهزة الإدخال. لتعديل هذه الإعدادات, يمكنك فتح ملف التكوين في محرر النصوص وإجراء التغييرات اللازمة.

## مامي

MAME, الذي يرمز إلى **"Multiple Arcade Machine Emulator",** هو تطبيق برمجي مصمم لمحاكاة وتكرار أجهزة آلات الآركيد القديمة ووحدات تحكم ألعاب الآركيد. فهو يسمح للمستخدمين بلعب مكتبة واسعة من ألعاب الآركيد الكلاسيكية على أجهزة الكمبيوتر الحديثة والأجهزة الأخرى المتوافقة. MAME هو مشروع مفتوح المصدر وقد أصبح محاكيًا مفضلاً للحفاظ على التاريخ الغني لألعاب الأركيد والاستمتاع به.

1. **المحاكاة:** الغرض الأساسي من MAME هو محاكاة أجهزة أجهزة الآركيد بدقة, بما في ذلك وحدات المعالجة المركزية (CPUs) وشرائح الصوت وشرائح الرسومات وأجهزة الإدخال. يضمن هذا المستوى من الدقة أن تكون الألعاب أقرب ما تكون إلى تجربة الآركيد الأصلية قدر الإمكان.

1. **التوافق:** يدعم MAME مجموعة واسعة من ROMs الخاصة بألعاب الآركيد, مما يجعله واحدًا من أكثر محاكيات الآركيد المتوفرة شمولاً. يمكنه تشغيل ألعاب من منصات آركيد مختلفة بما في ذلك الألعاب الكلاسيكية من السبعينيات والثمانينيات والتسعينيات وحتى بعض عناوين الأركيد الأحدث.

1. **الحفظ:** إحدى المهام الأساسية لـ MAME هي الحفاظ على تاريخ ألعاب الأركيد. من خلال محاكاة أجهزة الآركيد بدقة, يساعد MAME على منع فقدان الألعاب الكلاسيكية ويضمن أن تتمكن الأجيال القادمة من تجربتها كما كانت مقصودة في الأصل.

1. **الواجهات الأمامية:** يستخدم العديد من المستخدمين تطبيقات الواجهة الأمامية التي توفر واجهة رسومية لإدارة الألعاب وتشغيلها من خلال MAME. تسهل هذه الواجهات الأمامية التنقل في مكتبة ألعاب MAME الواسعة.

## كيفية فتح ملف CFG؟

البرامج التي تفتح ملفات CFG أو تشير إليها

- MAME (مجاني) (ويندوز)
- ExtraMAME (نسخة تجريبية)
- ماكمامي (ماك)

## ملفات CFG أخرى

فيما يلي أنواع الملفات الأخرى التي تستخدم امتداد الملف **.cfg**.

**إعدادات**
- [CFG - ملف تكوين Celestia](/ar/settings/cfg-celestia/)
- [CFG - ملف اتصال خادم Citrix](/ar/settings/cfg-citrix/)
- [CFG - ملف تكوين MAME](/ar/settings/cfg-mame/)
- [CFG - ملف تكوين LightWave](/ar/settings/cfg-lightwave/)

**لعبة**
- [CFG - ملف لغة ترميز Wesnoth](/ar/game/cfg-wesnoth/)
- [CFG - ملف تكوين MUGEN](/ar/game/cfg-mugen/)
- [CFG - ملف تكوين المحرك المصدر](/ar/game/cfg-sourceengine/)

**النظام والمتفرقات**
- [CFG - ملف CFG](/ar/system/cfg/)
- [CFG - ملف تكوين نموذج Cal3D](/ar/misc/cfg-cal3d/)

## مراجع
* [MAME](https://en.wikipedia.org/wiki/MAME)
