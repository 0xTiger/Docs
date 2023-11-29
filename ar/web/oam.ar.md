{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ملف OAM - تنسيق ملف Adobe Edge Animate Widget",
  "description" :"تعرف على ما هو ملف OAM وواجهات برمجة التطبيقات التي يمكنها إنشاء ملف OAM وفتحه.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## ما هو ملف OAM؟

ملف .oam هو ملف عنصر واجهة مستخدم متحرك تم تصديره من Adobe Edge Animate Widget. يمكن إدراج الرسوم المتحركة المصدرة بتنسيق ملف عنصر واجهة المستخدم OAM في تطبيقات Adobe الأخرى مثل InDesign Documents ([ملف INDD](/ar/page-description-language/indd/), وDreamweaver, وMuse. تشبه ملفات OAM حزم النشر التي يمكن نشرها بسهولة تم إدراجها في مشاريع Adobe الأخرى للاستفادة منها. تحتوي ملفات OAM على معلومات حول أصول الرسوم المتحركة وسلوكياتها ورمز actionscript. يمكنك إنشاء ملف OAM عن طريق نشر مشروع Adobe Animate [ملف .AN](/ar/web/an/) .
يمكن للمستخدمين إنشاء ملفات OAM عن طريق النشر من مشروع Edge Animate (ملف .AN).

## تنسيق ملف OAM

يتم حفظ ملف OAM على القرص كأرشيف مضغوط [ZIP](/ar/compression/zip/). وهذا يعني أنه يمكنك إعادة تسمية امتداد الملف إلى .zip واستخراجه باستخدام أي أداة ضغط مثل WinZIP أو WinRAR. يُسهل حجم الملف المنخفض نقل الرسوم المتحركة ومشاركتها مع مستخدمين آخرين عبر الإنترنت.

### بنية ملف OAM

تعتبر بنية الملف الداخلي لملف ‎.oam ملكية خاصة ولم يتم توثيقها بشكل علني بواسطة Adobe. ومع ذلك, فمن المعروف أن ملفات .oam تحتوي على مجموعة من الملفات والموارد (مثل الرسومات والصوت وكود ActionScript) مجمعة في ملف واحد. قد تتضمن محتويات ملف .oam ملفات [XML](/ar/web/xml/) وملفات SWF وملفات موارد أخرى. تعتمد البنية الدقيقة لملف .oam على الإصدار المحدد من Adobe Animate المستخدم في إنشائه, بالإضافة إلى نوع الرسوم المتحركة والأصول المضمنة في الملف.

يحتوي ملف OAM على المعلومات التالية.

`الأصول:` معلومات حول أصول الرسومات والصوت والفيديو المستخدمة في الرسوم المتحركة.

`السلوكيات:` وصف الإجراءات والتفاعلات التي تحدث في الرسوم المتحركة.

`كود ActionScript:` الكود المستخدم للتحكم في سلوك الرسوم المتحركة وتفاعلها.

`إعدادات النشر:` معلومات حول النظام الأساسي والتنسيق الذي سيتم نشر الرسوم المتحركة به, مثل HTML5 أو AIR.

`البيانات الوصفية:` معلومات إضافية مثل مؤلف الرسوم المتحركة وتاريخ الإنشاء ورقم الإصدار.

## كيفية فتح ملف OAM؟

يمكنك استخدام التطبيقات التالية لفتح ملفات OAM.

* Adobe Edge Animate CC (توقف)
* أدوبي أنيميت 2023
* أدوبي إن ديزاين 2023
* أدوبي دريمويفر 2021

## مراجع

* [نشر OAM](https://helpx.adobe.com/animate/using/OAM-publishing.html)
