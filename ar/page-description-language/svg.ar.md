{
  "date" : "2020-03-02",
  "keywords" :["SVG" , "ملف" , "تنسيق الملف" , "لغة وصف الصفحة" , "Scalar"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف SVG وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات SVG وفتحها." ,
  "title" :"ما هو ملف SVG؟" ,
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
} ,
  "lastmod" : "2020-03-02"
}

## ما هو ملف SVG؟ ##

ملف SVG هو ملف Scalar Vector Graphics يستخدم تنسيق نصي مبني على XML لوصف مظهر الصورة. تشير كلمة Scalable إلى حقيقة أنه يمكن تحجيم SVG إلى أحجام مختلفة دون فقدان أي جودة. الوصف المستند إلى النص لمثل هذه الملفات يجعلها مستقلة عن الدقة. إنه أحد أكثر التنسيقات استخدامًا لإنشاء موقع ويب وطباعة الرسومات من أجل تحقيق قابلية التوسع. لا يمكن استخدام التنسيق إلا للرسومات ثنائية الأبعاد. يمكن عرض / فتح ملفات SVG في جميع المتصفحات الحديثة تقريبًا بما في ذلك Chrome و Internet Explorer و Firefox و Safari.

## نبذة تاريخية ##

تتوفر مواصفات SVG كمعيار مفتوح من قبل World Wide Web Consortium (W3C) منذ عام 1999. قبل ذلك ، تم تقديم مواصفات تنسيق ملف مماثلة بستة تنسيقات مختلفة إلى W3C حتى عام 1998. تم تطبيق تحديث على المواصفات في عام 2011 وتم إصداره 1.1 . في عام 2016 ، تم نشر SVG 2 كإصدار أحدث بما في ذلك الميزات بالإضافة إلى تلك الموجودة في SVG 1.1.

## مواصفات تنسيق الملف ##

يضع SVG Document Object Model (DOM) الأسس لجميع المواصفات والواجهات التي تتوافق مع أقسام معينة من المواصفات. يجب أن يقوم عارضو SVG بتنفيذ واجهات SVG DOM على النحو المحدد في مواصفات W3C. يعرض DOM الخاص به العديد من الواجهات لأنواع البيانات المختلفة والعناصر.

### أشكال SVG ###

يحتوي SVG على بعض عناصر الشكل المحددة مسبقًا التي يمكن للمطورين استخدامها:

* مستطيل<rect>
* الدائرة<circle>
* الشكل البيضاوي<ellipse>
* خط<line>
* بوليلاين<polyline>
* مضلع<polygon>
* طريق<path>

بناءً على هذه الأشكال والمواصفات ، فإن المجالات الوظيفية لـ SVG هي كما يلي.

** المسارات ** - تُستخدم المسارات لتمثيل مخططات الأشكال البسيطة والمركبة. تستخدم الترميزات لتحديد طبيعة العملية. على سبيل المثال ، يتم استخدام M لـ Move To ، و L لـ Line To ، و Z لإغلاق مسار وما إلى ذلك.

** الأشكال الأساسية ** - يمكن رسم المسارات والمسارات المستقيمة المكونة من سلسلة من مقاطع الخطوط المستقيمة المتصلة (خطوط متعددة) ، بالإضافة إلى المضلعات والدوائر والأشكال البيضاوية المغلقة. المستطيلات والمستطيلات ذات الزوايا الدائرية هي أيضًا عناصر قياسية.

** نص ** - يتم التعبير عن تمثيل النص على هيئة بيانات أحرف XML حيث يمكن تطبيق العديد من التأثيرات المرئية على النص. تسمح المواصفات بمعالجة النص ثنائي الاتجاه والنص الرأسي والأحرف على طول مسار منحن.

** الرسم ** - يمكن تعبئة الأشكال و / أو تحديدها بلون أو تدرج أو نقش ، مما يتيح إمكانية جعلها غير شفافة أو تتمتع بأي درجة من الشفافية. يتم تمثيل ميزات نهاية الخط مثل رؤوس الأسهم أو الرموز التي تظهر عند رؤوس المضلع بواسطة العلامات.

** اللون ** - تسمح مواصفات SVG بتطبيق الألوان على جميع عناصر SVG المرئية ، إما بشكل مباشر أو عن طريق التعبئة والحد وخصائص أخرى. يمكن استخدام ترميز لوني مختلف لتحديد مثل الأسود أو الأزرق ، التمثيل السداسي ، العشري أو كنسب مئوية من نموذج RGB.

** التدرجات والأنماط ** - يمكن تعبئة الأشكال في ملف SVG أو تحديدها بألوان خالصة أو تدرجات أو أنماط متكررة.

** تأثيرات المرشح ** - في الواقع عبارة عن سلسلة من عمليات الرسومات التي يتم تطبيقها على رسم متجه مصدر معين لإنتاج نتيجة معدلة.

** التفاعل ** - يمكن للمستخدمين التفاعل مع ملفات SVG عن طريق تغيير التركيز أو نقرات الماوس أو التمرير أو تكبير الصورة. يتيح التفاعل لصور SVG التفاعل مع المستخدمين بعدة طرق مختلفة كما هو مذكور أعلاه.

** الربط ** - من الممكن أن تحتوي صور SVG على ارتباطات تشعبية لمستندات أخرى. يتم تحقيق ذلك من خلال لغة ربط XML أو XLink. يسمح هذا بإنشاء حالات عرض محددة تُستخدم لتكبير / تصغير منطقة معينة أو لتقييد العرض بعنصر معين.

** البرمجة ** - على غرار HTML ، يمكن الوصول إلى جميع جوانب مستند SVG للمعالجة باستخدام البرامج النصية. توفر كائنات SVG DOM إرشادات لتحقيق ذلك باستخدام عنصر وسمة SVG. يتم تضمين البرامج النصية في عناصر علامة "البرنامج النصي" ويمكن تشغيلها استجابةً لأحداث المؤشر أو لوحة المفاتيح أو المستند كما هو مطلوب.

** الرسوم المتحركة ** - عناصر DOM<animate> و<animateMotion> و<animateColor> يتيح لك تضمين الرسوم المتحركة لمحتويات SVG. بالطبع ، لا يمكن تحقيق ذلك بدون استخدام البرامج النصية وأجهزة ضبط الوقت المدمجة. يمكن أن تكون هذه الرسوم المتحركة مستمرة ويمكن وضعها في حلقة بالإضافة إلى تكرارها أثناء الاستجابة في نفس الوقت لأحداث المستخدم.

** الخطوط ** - يمكن أن يشير النص في SVG إلى ملفات الخطوط الخارجية مثل خطوط النظام. في حالة عدم وجود مثل هذه الخطوط ، لن يتم عرض النص في SVG على الإخراج. يمكن التغلب على ذلك من خلال دمج الحروف الرسومية المطلوبة في ملف كخط يتم عرضه بعد ذلك باستخدام امتداد<text> عنصر.

## أمثلة ##
توضح الأسطر التالية كيفية تمثيل الدائرة باستخدام برنامج SVG النصي.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

توضح سطور التعليمات البرمجية التالية كيفية استخدام ملف<text> حظر لتقديم النص إلى SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## مراجع ##

* [مواصفات W3C SVG] (https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - ويكيبيديا] (https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)
