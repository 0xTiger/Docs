{
  "date" : "2020-11-11",
  "keywords" :["LDF" , "extension" , "file" , "تنسيق الملف" , "نوع ملف قاعدة البيانات" , "تنسيق ملف قاعدة البيانات" , "ملفات قاعدة البيانات"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف LDF وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات LDF وفتحها." ,
  "title" :"LDF - تنسيق ملف قاعدة بيانات SQL Server الرئيسية" ,
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
} ,
  "lastmod" : "2020-08-12"
}

## ما هو ملف LDF؟

الملف بامتداد .ldf هو ملف سجل يتم الاحتفاظ به بواسطة Microsoft SQL Server وهو نظام إدارة قواعد بيانات علائقية (RDBMS). يتم تسجيل جميع المعاملات التي تتم على ملفات قاعدة البيانات الأولية ([MDF](/ar/database/mdf/)) (مثل الإدراج والتحديث والحذف) في ملف LDF. تعد ملفات LDF مكونات أساسية لأي قاعدة بيانات. في حالة فشل النظام ، يتم استخدام ملف السجل لاستعادة قاعدة البيانات إلى حالة متسقة. يمكن زيادة حجم ملف سجل المعاملات إذا لم يتم الالتزام بالمعاملات بشكل كامل. يمكن فتح ملفات LDF باستخدام تطبيق برنامج Microsoft SQL Server.

## العمليات المسجلة في ملف LDF

يسجل ملف سجل SQL العمليات التالية:

* بداية ونهاية كل معاملة.

* كل تعديل بيانات بيانات (ادراج ، تحديث ، او حذف). يتضمن هذا أيضًا التغييرات حسب الإجراءات المخزنة في النظام أو عبارات لغة تعريف البيانات (DDL) إلى أي جدول ، بما في ذلك جداول النظام.

* كل مدى وتخصيص الصفحة أو إلغاء التخصيص.

* إنشاء أو إسقاط جدول أو فهرس.

## تنسيق ملف LDF

يتكون ملف LDF من سجلات معاملات SQL Server التي تم ترتيبها كسلسلة من سجلات السجل. يحتوي كل سجل سجل على رقم تسلسل سجل (LSN) أعلى من LSN للسجل السابق. السلاسل متسلسلة بعد بعضها البعض في الملف. نظرًا لأجهزة الكمبيوتر الحديثة عالية السرعة ، يمكن إدراج السجلات في مكان وجود LSN2 في ملف السجل قبل LSN1. نظرًا لتسجيل العمليات في مسلسل ، تم إجراء التغيير الموصوف بواسطة LSN2 بعد سجل السجل LSN1. يتم ربط السجلات الخاصة بمعاملة معينة للخلف باستخدام المؤشرات المستخدمة وتسريع التراجع عن المعاملة.
 

## مراجع

* [ملفات قاعدة البيانات ومجموعات الملفات](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [دليل هندسة وإدارة سجل المعاملات](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server-ver15)

