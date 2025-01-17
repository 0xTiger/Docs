{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف NMONEY وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات NMONEY وفتحها.",
  "title" :"ملف NMONEY - تنسيق ملف حساب Denaro",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## ما هو ملف NMONEY؟

ملف NMONEY هو ملف قاعدة بيانات لتخزين البيانات المالية يحتوي على سجل حافل للمعاملات المالية. تم تطويره بواسطة Nickvision وتم استخدامه في برنامج Nickvision Denaro وهو تطبيق برمجي مالي شخصي. تتضمن البيانات المخزنة داخل ملف NOMONEY معلومات معاملات الائتمان والخصم إلى الحساب.

يمكن فتح ملفات NOMONEY باستخدام تطبيق [Github](https://github.com/NickvisionApps/Denaro).

## نبذة عن برنامج دينارو

تم تطوير Denaro في البداية بواسطة [Nickvision](https://nickvision.org/) كمنتج تم تحويله لاحقًا إلى تطبيق برمجي مفتوح المصدر مستضاف على [Github](https://github.com/NickvisionApps/Denaro) . منذ ذلك الحين تم تعديل التطبيق وتحديثه على Github فقط. تم تطوير التطبيق بلغة C# في Windows UI باستخدام Windows App SDK (WinUI 3 في الوقت الحالي).

### الميزات التي تقدمها دينارو

* إدارة حسابات متعددة في وقت واحد من خلال واجهة علامة التبويب الأكثر شهرة ومألوفة
* تصفية المعاملات حسب النوع أو المجموعة أو التاريخ
* تكرار المعاملات مثل الفواتير التي تحدث كل شهر
* تحويل الأموال من حساب إلى آخر
* تصدير البيانات من الحساب كملف CSV واستيراد ملف CSV أو OFX أو QIF لإضافة المعاملات إلى الحساب

## تنسيق ملف دينارو - مزيد من المعلومات

يتم حفظ ملفات Denaro على القرص بتنسيق ملف ثنائي. يتم تخزين البيانات المالية كملف قاعدة بيانات بتنسيق ملف **.SQLITE3**. SQLITE هو ملف قاعدة بيانات SQL خفيف الوزن تم إنشاؤه باستخدام برنامج SQLite. إنه يوفر محرك قاعدة بيانات قائم بذاته قادر على توفير قاعدة بيانات كاملة المزايا وموثوقة للغاية. يمكن استخدام ملفات قاعدة بيانات SQLite لمشاركة المحتويات الغنية بين الأنظمة ببساطة عن طريق تبادل هذه الملفات عبر الشبكة. توجد روابط SQLite للغات البرمجة مثل C, [C#](/ar/programming/cs/), [C++](/ar/programming/cpp/), [Java](/ar/programming/java/), [PHP](/ar/programming/php/), وغيرها الكثير.

## مراجع

* [نيكفيجن](https://nickvision.org/)
* [NIckVision - جيثب](https://github.com/NickvisionApps/Denaro)

