{
"التاريخ": "2023-04-20",
  "keywords": [
"ملف إل دي بي",
"ما هو ملف ldb",
"ما هي المعلومات التي يحتوي عليها ldb",
"ما هو الغرض من ملف ldb",
"امتداد ldb",
"ملف",
"امتداد"
],
  "author": {
"display_name": "شكيل فايز"
},
"draft": "false",
"toc": true,
"title": "تنسيق ملف LDB - ملف قفل الوصول إلى Microsoft",
  "description":"تعرف على تنسيق LDB والمعلومات التي يحتوي عليها.",
"linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
"parent" : "misc"
}
},
"آخر مود": "2023-04-20"
}

## ما هو ملف LDB؟

ملف LDB هو ملف قفل يستخدمه Microsoft Access لمنع عدة مستخدمين من تحرير نفس قاعدة البيانات في وقت واحد. عندما يفتح المستخدم قاعدة بيانات Access, يقوم Access بإنشاء ملف LDB مطابق في نفس الدليل مثل قاعدة البيانات. يحتوي هذا الملف على معلومات حول الأشخاص الذين يستخدمون قاعدة البيانات حاليًا والسجلات التي يقومون بتحريرها.

يتم إنشاء ملف LDB تلقائيًا بواسطة Microsoft Access عند فتح قاعدة البيانات, ويتم حذفه عند إغلاق قاعدة البيانات. من المهم ملاحظة أنه لا ينبغي أبدًا حذف ملف LDB يدويًا لأن ذلك قد يسبب مشاكل في قاعدة البيانات.

إذا واجهت مشاكل مع قاعدة بيانات Microsoft Access, فإن أحد الحلول المحتملة هو محاولة حذف ملف LDB المرتبط بقاعدة البيانات تلك. سيؤدي هذا إلى تحرير أي أقفال قد تمنعك من الوصول إلى قاعدة البيانات. ومع ذلك, تأكد من عمل نسخة احتياطية لقاعدة البيانات قبل محاولة ذلك, لأن حذف ملف LDB يمكن أن يسبب فقدان البيانات أو تلفها إذا تم ذلك بشكل غير صحيح.

## تنسيق ملف LDB - مزيد من المعلومات

يحتوي ملف LDB في Microsoft Access على معلومات حول المستخدمين الذين يصلون حاليًا إلى قاعدة البيانات مثل اسم المستخدم واسم الكمبيوتر ووقت تسجيل الدخول. يحتوي ملف LDB أيضًا على معلومات حول أي أقفال تم وضعها على قاعدة البيانات, مثل السجلات التي يتم تحريرها بواسطة أي مستخدم.

فيما يلي قائمة أكثر تفصيلاً بأنواع المعلومات التي يمكن العثور عليها في ملف LDB:

- **اسم المستخدم** - اسم المستخدم الذي يصل حاليا إلى قاعدة البيانات
- **اسم الكمبيوتر** - اسم الكمبيوتر الذي يصل المستخدم منه إلى قاعدة البيانات
- **وقت تسجيل الدخول** - الوقت الذي فتح فيه المستخدم قاعدة البيانات لأول مرة
- **أقفال السجلات** - معلومات حول السجلات التي يتم تحريرها حاليًا بواسطة أي مستخدم
- **أقفال الكائنات** - معلومات حول كائنات قاعدة البيانات (مثل الجداول أو النماذج أو التقارير) التي يتم تحريرها حاليًا بواسطة أي مستخدم
- **معلومات الاتصال** - معلومات حول كيفية اتصال المستخدم بقاعدة البيانات (على سبيل المثال, ما إذا كان يستخدم اتصالاً محليًا أو اتصالاً بالشبكة)

يتم استخدام المعلومات الموجودة في ملف LDB بواسطة Microsoft Access لمنع عدة مستخدمين من إجراء تغييرات متعارضة على نفس قاعدة البيانات في نفس الوقت. عندما يحاول المستخدم تحرير سجل أو كائن مقفل بالفعل من قبل مستخدم آخر, سيعرض Microsoft Access رسالة تشير إلى أن الكائن قيد الاستخدام بالفعل. يتم تحديث ملف LDB عندما يقوم المستخدمون بفتح قاعدة البيانات وإغلاقها وإجراء تغييرات على الكائنات المقفلة.

## مراجع
* [ما هو ملف LDB؟](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

