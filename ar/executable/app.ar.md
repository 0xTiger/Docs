{
"التاريخ": "02-02-2023",
  "keywords": [
"ملف التطبيق",
"ما هو ملف التطبيق",
"ملف",
"كيفية فتح ملف التطبيق",
"امتداد ملف التطبيق",
"امتداد"
],
  "author": {
"display_name": "شكيل فايز"
},
"draft": "false",
"toc": true,
  "description":"تعرف على تنسيق ملف APP وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات APP وفتحها.",
"title": "تنسيق ملف التطبيق - حزمة تطبيقات macOS",
"linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app",
"parent" : "executable"
}
},
"آخر مود": "02-02-2023"
}

## ما هو ملف APP؟

يعد ملف ‎.app على نظام التشغيل macOS نوعًا خاصًا من الدليل الذي يحتوي على جميع الملفات الضرورية لتشغيل تطبيق معين, بما في ذلك التعليمات البرمجية القابلة للتنفيذ والموارد وبيانات التعريف. يشير الامتداد .app إلى نظام التشغيل بأنه يجب التعامل مع هذا الدليل كوحدة واحدة, بدلاً من مجموعة من الملفات المنفصلة, وأنه يمكن تشغيله مباشرة من Finder أو Dock.

Finder هو تطبيق مدير الملفات الافتراضي على نظام التشغيل macOS. يسمح لك بتصفح وتنظيم الملفات والأدلة الموجودة على جهاز الكمبيوتر الخاص بك. تعد Dock إحدى ميزات نظام التشغيل macOS التي توفر وصولاً سريعًا إلى التطبيقات والمستندات المستخدمة بشكل متكرر. يسمح لك كل من Finder وDock بتشغيل التطبيقات من خلال النقر على ملفات .app الخاصة بها, والتي ستفتح حزمة التطبيقات المقابلة. عند تشغيل تطبيق ما, يتم تشغيل التعليمات البرمجية القابلة للتنفيذ ضمن حزمة .app, مما يجعل التطبيق متاحًا للاستخدام. يمثل ملف ‎.app التطبيق على نظام الملفات, ويوفر طريقة للمستخدم للوصول إلى التطبيق وتشغيله.

عند النقر بزر الماوس الأيمن على ملف ‎.app في Finder على نظام macOS وتحديد "إظهار محتويات الحزمة", ستتمكن من رؤية البنية الداخلية لحزمة التطبيق. يعد هذا مفيدًا إذا كنت تريد الوصول إلى الموارد أو الملفات التي يستخدمها التطبيق, أو إذا كنت تريد فحص محتويات التطبيق لأغراض استكشاف الأخطاء وإصلاحها. تتضمن محتويات حزمة ملف ‎.app عادةً أدلة للموارد مثل الصور والأصوات, بالإضافة إلى التعليمات البرمجية القابلة للتنفيذ الخاصة بالتطبيق. من خلال استكشاف محتويات ملف ‎.app, يمكنك الحصول على رؤى أعمق حول كيفية تجميع التطبيق معًا وما يفعله.

## كيفية فتح ملف التطبيق؟

لفتح ملف ‎.app على نظام التشغيل macOS, ما عليك سوى النقر نقرًا مزدوجًا فوق الملف في Finder. سيؤدي هذا إلى تشغيل التطبيق الموجود ضمن حزمة .app. إذا كان التطبيق مثبتًا على نظامك وكان مرتبطًا بنوع الملف ‎.app, فيجب أن يؤدي النقر المزدوج فوق الملف إلى بدء تشغيل التطبيق تلقائيًا. إذا لم يكن التطبيق مرتبطًا بنوع الملف ‎.app, فقد تحتاج إلى النقر بزر الماوس الأيمن فوق الملف وتحديد "فتح باستخدام" لاختيار التطبيق المناسب لفتحه به.

يمكنك فتح ملف ‎.app على الجهاز الطرفي في نظام التشغيل macOS باستخدام الأمر "فتح". للقيام بذلك, انتقل إلى الدليل الذي يوجد به ملف .app باستخدام الأمر "cd", ثم قم بتشغيل الأمر التالي:

```
open <AppName>.app 
```

أين<AppName> هو اسم التطبيق الذي تريد تشغيله. سيؤدي هذا إلى تشغيل التطبيق كما لو كنت قد نقرت عليه نقرًا مزدوجًا في Finder. يعد الأمر "فتح" أداة مساعدة للأغراض العامة يمكن استخدامها لفتح العديد من أنواع الملفات المختلفة, بما في ذلك التطبيقات والمستندات والدلائل. عند استخدام الأمر "open" في ملف ‎.app, فإنه يقوم بتشغيل التطبيق الموجود داخل الحزمة.

## مراجع
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
