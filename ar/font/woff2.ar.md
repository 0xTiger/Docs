{
  "date" : "2023-01-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ملف WOFF2 - ملف تنسيق الخط المفتوح على الويب 2.0",
  "description":"ملف WOFF2 - ملف تنسيق الخط المفتوح على الويب 2.0",
  "linktitle" : "WOFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-10"
}

## ما هو ملف WOFF2؟

WOFF2 هو تنسيق ملف خط وهو إصدار مضغوط أكثر من تنسيق Web Open Font Format (WOFF). وقد تم تطويره كوسيلة لتقليل حجم ملف خطوط الويب، مما يسمح لها بالتحميل بشكل أسرع واستخدام نطاق ترددي أقل. يستخدم WOFF2 خوارزمية ضغط تسمى Brotli لضغط بيانات الخط، مما قد يؤدي إلى أحجام ملفات أصغر بكثير من خطوط [WOFF](/font/woff/) المكافئة. يتم دعم هذا التنسيق بواسطة معظم متصفحات الويب الحديثة بما في ذلك Chrome وFirefox وSafari وOpera وEdge (الإصدار 14 وما بعده).

## تنسيق ملف WOFF2 - مزيد من المعلومات

تتكون بنية الملف الداخلي لملف خط WOFF2 من عدة أجزاء مختلفة، بما في ذلك الرأس وبيانات التعريف ودليل الجدول وبيانات الخط نفسها.

 1. يحتوي الرأس على معلومات حول التنسيق العام للملف، بما في ذلك رقم الإصدار وعدد الجداول الموجودة في الملف.

 1. يحتوي قسم البيانات التعريفية على معلومات مثل اسم الخط وحقوق النشر والمعلومات الأخرى المتعلقة بالخط.

 1. يحتوي دليل الجدول على معلومات حول الجداول المختلفة التي يتكون منها الخط، بما في ذلك موقعها في الملف وطولها.

 1. يتم تقسيم بيانات الخط نفسها إلى عدة جداول مختلفة، يحتوي كل منها على معلومات محددة حول الخط، مثل أحرفه والصور الرمزية المقابلة لها. قد تشمل هذه الجداول ما يلي:

 * يحتوي جدول glyf على الخطوط العريضة الفعلية للخط، بما في ذلك شكل وحجم كل حرف.
 * يحتوي جدول الرأس على معلومات عامة حول الخط، مثل رقم الإصدار وحجم التصميم وما إلى ذلك.
 * يحتوي جدول hmtx على معلومات حول قياسات الخط، بما في ذلك عرض الأحرف ومواضعها.
 * يتم ضغط كل جدول وتخزينه بتنسيق ملف WOFF2 بعد اكتمال عملية الترميز.

تم تصميم البنية بشكل عام للسماح بالتحليل وفك التشفير بسرعة، بحيث يمكن لمتصفحات الويب تحميل الخط وعرضه على موقع الويب بسرعة وكفاءة.

### رأس WOFF2
يتكون رأس WOFF من توقيع تعريفي يشير إلى نوع البيانات المضمنة في الملف. رأس WOFF مع حقوله هو كما يلي.

|النوع|اسم الحقل|الوصف|
---|---|---|
|UInt32|التوقيع |0x774F4632 'wOF2' |
|UInt32| نكهة |إصدار sfnt لخط الإدخال.|
|UInt32| length |الحجم الإجمالي لملف WOFF.|
|UInt16| numTables |عدد الإدخالات في دليل جداول الخطوط.|
|UInt16| محفوظة |محجوزة؛ مضبوطة على الصفر.|
|UInt32| TotalSfntSize |الحجم الإجمالي المطلوب لبيانات الخط غير المضغوطة، بما في ذلك رأس sfnt والدليل وجداول الخطوط (بما في ذلك الحشو).|
|UInt32| TotalCompressedSize إجمالي طول كتلة البيانات المضغوطة.|
|UInt16| MajorVersion |الإصدار الرئيسي لملف WOFF.|
|UInt16| minorVersion |إصدار ثانوي من ملف WOFF.|
|UInt32| metaOffset |الإزاحة إلى كتلة بيانات التعريف، من بداية ملف WOFF.|
|UInt32| metaLength |طول كتلة بيانات التعريف المضغوطة.|
|UInt32| metaOrigLength |الحجم غير المضغوط لكتلة بيانات التعريف.|
|UInt32| privOffset |إزاحة كتلة البيانات الخاصة، من بداية ملف WOFF.|
|UInt32| privLength |طول كتلة البيانات الخاصة.|


## مراجع
 * [تنسيق ملف w3 WOFF2](https://www.w3.org/TR/WOFF2/)

