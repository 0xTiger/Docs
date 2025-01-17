{
  "date" : "2021-02-01",
  "keywords" :["usdz" , "ملف usdz" , "تنسيق ملف usdz" , "تنسيق الملف" , "3d" , "تنزيل ملف usdz"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - تنسيق ZIP لوصف المشهد العالمي" ,
  "description":"تعرف على تنسيق ملف USDZ وواجهات برمجة التطبيقات التي يمكنها فتح وإنشاء ملفات USDZ." ,
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
} ,
  "lastmod" : "2021-02-01"
}

## ما هو ملف USDZ؟

الملف الذي يحتوي على .usdz هو أرشيف ZIP غير مضغوط وغير قابل للتجريب لتنسيق الملف [USD](/3d/usd/)(وصف المشهد العام) الذي يحتوي على ووكلاء للملفات ذات التنسيقات الأخرى (مثل الأنسجة والرسوم المتحركة) المضمنة في الأرشيف وتشغيلها مباشرة مع وقت التشغيل بالدولار الأمريكي دون الحاجة إلى تفريغ. ملفات USDZ هي حزم يعتمد تصميمها على التجريد الجديد للحزمة على مستوى Ar. تم تسجيل Usdz لدى IANA ولديه اسم نوع وسائط للنموذج واسم نوع فرعي لـ vnd.usd + zip ويمكن العثور على تفاصيله كما هو الحال في صفحة تسجيل [IANA](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## تنسيق ملف USDZ

تستند ملفات USDZ إلى تنسيق ملف ZIP الذي يقوم بأرشفة الملفات الفردية في حاويتها. يتيح ذلك لجهاز الاستقبال فك ضغط المحتويات واستخدام ملفات وصف مشهد الدولار العادي للعمل معها وفحصها. توفر جميع أنظمة التشغيل تقريبًا دعمًا مدمجًا لتنسيقات ملفات ZIP ، كما أن اختيار تنسيق الأرشفة هذا على أي طريقة مخصصة يجعل من السهل على ملفات USDZ أن تكون مفيدة كبروتوكول نقل بسيط.

### قيود ZIP

يستخدم تنسيق ملف USDZ تنسيق ملف ZIP بدون أي "ضغط" و "تشفير". كان الهدف من هذا التصميم هو تلبية متطلبين:

* بالنسبة للحزمة التي تم تحميلها بالفعل في الذاكرة أو كملف واحد على القرص ، فإن واجهة برمجة التطبيقات متاحة بالدولار الأمريكي للوصول إلى البيانات الموجودة في الصورة
* يجب ألا تكون هناك حاجة لاستخراج الملفات إلى القرص أو تخصيص المزيد من مساحة تخزين الكومة

مع USDZ ، يتم تلبية هذين المطلبين لأن معظم تنسيقات الصور نفسها تسمح بأنظمة ضغط داخلية ، مما ينتج عنه حجم ملف مضغوط.

### متطلبات التخطيط

تتطلب حزم USDZ تخطيط الملفات داخل الحزمة وهو أن البيانات لكل ملف يجب أن تبدأ بمضاعفات 64 بايت من بداية الحزمة. ومع ذلك ، يجب أن تبدأ الحزمة بملف أصلي [USD](/ar/3d/usd/) في حالة استهداف الحزمة بمرجع بسيط. في مثل هذه الحالة ، تتم الإشارة إلى ملف USD الأول باسم الطبقة الافتراضية. قد يرغب العملاء الذين يرغبون في تقديم "محتوى قابل للبث" في التفكير في قيود التخطيط الأخرى أيضًا.

## تنزيل ملف USDZ
نظرًا لأن ملفات usdz معبأة بصور أخرى عالية الجودة وملفات usd ، فإنها يمكن أن تشغل مساحة تخزين أكبر على القرص. هنا يمكنك العثور على مثال بسيط وأصغر لملف USDZ للتنزيل:

- [Sample.usdz](../sample.usdz)

## مراجع

* [مواصفات تنسيق ملف USDZ](https://openusd.org/release/spec_usdz.html)
