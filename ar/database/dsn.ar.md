{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "تنسيق ملف DSN - ملف اسم مصدر قاعدة البيانات",
  "title" : "تنسيق ملف DSN - ملف اسم مصدر قاعدة البيانات",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## ما هو ملف DSN؟

يرمز DSN إلى اسم مصدر البيانات وهو تنسيق ملف يستخدم لتخزين معلومات اتصال قاعدة البيانات. تُستخدم ملفات DSN عادةً مع ODBC (اتصال قاعدة البيانات المفتوحة) وتسمح بالوصول السهل إلى قاعدة بيانات معينة من خلال توفير المعلومات اللازمة للاتصال بها، مثل اسم الخادم واسم المستخدم وكلمة المرور. يكون الملف عادةً بنص عادي ويمكن إنشاؤه وتحريره باستخدام محرر النصوص. ويمكن استخدامه على أنظمة التشغيل المختلفة مثل Windows، Linux، وMac.

## كيفية إنشاء ملف DSN؟

قد تختلف طريقة إنشاء ملف DSN بناءً على نظام التشغيل والأدوات المتوفرة. توفر الخطوات التالية نظرة عامة على عملية إنشاء ملف DSN على نظام Windows.

1. افتح مسؤول مصدر بيانات ODBC من خلال البحث عن مصادر بيانات ODBC في قائمة البداية.
2. حدد علامة التبويب System DSN وانقر فوق الزر Add.
3. حدد برنامج التشغيل المناسب لقاعدة البيانات التي ترغب في الاتصال بها وانقر فوق إنهاء.
4. قم بملء المعلومات اللازمة للاتصال بقاعدة البيانات، مثل اسم الخادم واسم المستخدم وكلمة المرور.
5. انقر فوق موافق لحفظ ملف DSN.

وبدلاً من ذلك، يمكنك إنشاء ملف DSN يدويًا عن طريق إنشاء ملف نصي عادي بامتداد .dsn وإدخال معلومات الاتصال الضرورية بالتنسيق:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

يمكنك بعد ذلك استخدام مسار هذا الملف باعتباره DSN في التعليمات البرمجية/البرنامج النصي الخاص بك للاتصال بقاعدة البيانات.

## البرامج التي تفتح ملف DSN

ملف DSN هو ملف نصي عادي يقوم بتخزين المعلومات المستخدمة للاتصال بقاعدة بيانات، مثل اسم الخادم واسم المستخدم وكلمة المرور. يتم استخدامه عادةً مع ODBC (اتصال قاعدة البيانات المفتوحة) لتوفير وصول سهل إلى قاعدة بيانات محددة.

لفتح وعرض محتويات ملف DSN، يمكنك استخدام أي محرر نصوص مثل Notepad أو Sublime Text أو Atom وما إلى ذلك. ستسمح لك هذه البرامج بفتح ملف DSN وعرض معلومات الاتصال المخزنة داخله.

ومع ذلك، لاستخدام ملف DSN للاتصال بقاعدة بيانات وتنفيذ عمليات مثل SELECT وINSERT وUPDATE وDELETE وما إلى ذلك، يجب استخدام برنامج يدعم ODBC، مثل لغة برمجة مثل Python أو Java أو C# أو أداة إدارة قاعدة بيانات مثل Microsoft Access مطلوب SQL Server Management Studio. يمكن لهذه البرامج استخدام المعلومات الموجودة في ملف DSN للاتصال بقاعدة البيانات وتنفيذ العملية المطلوبة.

## مراجع

* [ما هو DSN (اسم مصدر البيانات)؟](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30-606e-2436fe26e89f)