{
"التاريخ": "08-06-2023",
  "keywords": [
"ملف crx",
"ما هو ملف crx",
"كيفية تثبيت ملف crx في جوجل كروم",
"كيفية فتح ملف crx",
"ماذا يحتوي ملف crx",
"ما هو تنسيق ملف crx",
"ملف",
"امتداد الملف crx",
"امتداد"
],
  "author": {
"display_name": "شكيل فايز"
},
"draft": "false",
"toc": true,
"title": "تنسيق الملف CRX - ملحق Google Chrome",
  "description":"تعرف على تنسيق CRX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CRX وفتحها.",
"linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
"parent": "متفرقات"
}
},
"آخر مود": "08-06-2023"
}

## ما هو ملف CRX؟

يرتبط تنسيق الملف CRX بملحقات متصفح Google Chrome. يعد ملف CRX في الأساس حزمة مضغوطة تحتوي على الملفات والبيانات الوصفية الضرورية للملحق الذي سيتم تثبيته وتشغيله في Google Chrome. إنه يعزز وظيفة أو مظهر متصفح الويب من خلال توفير ميزة أو سمة إضافية.

عند تنزيل ملف CRX وتثبيته في Google Chrome, يتحقق المتصفح من سلامة الامتداد باستخدام المفتاح العام والتوقيع. إذا نجحت عملية التحقق, فسيقوم Chrome باستخراج محتويات ملف CRX وتثبيت الامتداد, مما يجعله متاحًا للاستخدام. يمكن للمستخدمين إدارة ملحقاتهم من خلال صفحة ملحقات Chrome, والتي تسمح بتمكين أو تعطيل أو إزالة الملحقات المثبتة.

## كيفية تثبيت ملف CRX في جوجل كروم؟

لتثبيت ملف CRX في Google Chrome, يمكنك اتباع الخطوات التالية:

1. افتح متصفح كروم.
2. اكتب "chrome://extensions" في شريط العناوين ثم اضغط على Enter.
3. قم بتمكين مفتاح التبديل "وضع المطور" الموجود في الزاوية العلوية اليمنى من صفحة الإضافات.
4. انقر على زر "تحميل مفتوح".
5. حدد موقع المجلد الذي يحتوي على محتويات ملف CRX وحدده (أو ببساطة حدد ملف CRX نفسه).
6. انقر فوق "فتح" لتثبيت الامتداد.

## ماذا يحتوي ملف CRX؟

يحتوي ملف CRX على الملفات والبيانات الوصفية الضرورية المطلوبة لامتداد Google Chrome. فيما يلي تفاصيل للمحتويات النموذجية الموجودة في ملف CRX:

- **ملف البيان (manifest.json):** هذا الملف عبارة عن ملف بتنسيق JSON يتضمن معلومات حول الامتداد مثل الاسم والإصدار والوصف والأذونات والبرامج النصية للخلفية. وهو يحدد هيكل وسلوك التمديد.
- **ملفات جافا سكريبت:** تحتوي هذه الملفات على الكود الذي يحدد وظيفة الامتداد. وقد تتضمن نصوصًا برمجية للتعامل مع الأحداث أو تعديل صفحات الويب أو التفاعل مع واجهات برمجة تطبيقات Chrome.
- **ملفات HTML وCSS والصور:** تشتمل الإضافات غالبًا على عناصر واجهة المستخدم, مثل النوافذ المنبثقة أو صفحات الخيارات. تحدد ملفات HTML بنية هذه الواجهات, بينما تتحكم ملفات CSS في مظهرها. تُستخدم ملفات الصور للأيقونات أو الأصول الرسومية الأخرى.
- **ملفات الموارد الاختيارية:** قد تتضمن الامتدادات موارد إضافية, مثل ملفات الترجمة لدعم لغات متعددة. تحتوي هذه الملفات على ترجمات للنص المستخدم في واجهة مستخدم الامتداد.
- **البرامج النصية للخلفية:** إذا كان الملحق يحتوي على عمليات خلفية أو نصوص برمجية تعمل بشكل مستقل عن صفحة الويب النشطة, فسيتم تضمين هذه البرامج النصية في ملف CRX.
- **البرامج النصية للمحتوى:** البرامج النصية للمحتوى هي نصوص برمجية يمكن إدخالها في صفحات الويب لتعديل سلوكها أو التفاعل مع محتواها. إذا كان الامتداد يستخدم نصوصًا برمجية للمحتوى, فستكون الملفات الضرورية لهذه النصوص البرمجية موجودة في ملف CRX.
- **أصول أخرى:** اعتمادًا على متطلبات الامتداد المحددة, قد يتم تضمين ملفات إضافية مثل ملفات الصوت أو الفيديو أو الخطوط أو ملفات البيانات.

يعد تنسيق ملف CRX في الأساس حزمة مضغوطة تحتوي على كل هذه الملفات والمجلدات بطريقة منظمة. عند تثبيت ملف CRX في Google Chrome, يستخرج المتصفح المحتويات ويضعها في المواقع المناسبة, مما يسمح بتحميل الامتداد وتشغيله داخل المتصفح.

## ما هو تنسيق ملف CRX؟

يعد تنسيق ملف CRX تنسيقًا محددًا لتعبئة ملحقات Google Chrome وتوزيعها. إنه في الأساس أرشيف ZIP مضغوط بامتداد ملف مختلف. البنية الأساسية لملف CRX هي كما يلي:

- **توقيع الملف:** تحتوي أول 4 بايت من الملف على الرقم السحري "Cr24" (النظام الست عشري: 43 72 32 34) الذي يعمل كتوقيع لتعريف الملف كملف CRX.
- **رقم الإصدار:** تمثل البايتات الأربع التالية رقم إصدار تنسيق CRX.
- **طول المفتاح العام:** تشير البايتات الأربع التالية إلى طول المفتاح العام المشفر المستخدم للتحقق من توقيع الامتداد.
- **طول التوقيع:** تحدد البايتات الأربع اللاحقة طول توقيع الامتداد.
- **المفتاح العام:** يحتوي هذا القسم على المفتاح العام المشفر المستخدم للتحقق من سلامة الامتداد.
- **التوقيع:** يحتوي هذا القسم على توقيع الامتداد, والذي يتم إنشاؤه عن طريق التوقيع على محتويات الامتداد باستخدام مفتاح خاص يتوافق مع المفتاح العام المذكور أعلاه.
- **أرشيف ZIP:** تشتمل وحدات البايت المتبقية من ملف CRX على أرشيف ZIP مضغوط. يحتوي هذا الأرشيف على جميع الملفات والمجلدات الضرورية للامتداد, بما في ذلك ملف البيان وملفات JavaScript وملفات HTML وملفات CSS والصور وأي موارد أخرى.

## مراجع
* [مواصفات تنسيق CRX](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)
