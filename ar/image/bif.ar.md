{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ملف BIF - تنسيق صورة الشريحة الكاملة لـ Ventana",
  "description":"ملف BIF - تنسيق صورة الشريحة الكاملة لـ Ventana",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## ما هو ملف BIF؟

ملف BIF هو ملف صورة نقطية يحتوي على صورة عينة الشريحة. وهو يتألف من صور TIFF متعددة يتم دمجها بواسطة تطبيقات عرض الشرائح في صورة مركبة واحدة. يتم إنشاء ملفات BIF بواسطة ماسح الشرائح الرقمي لأنظمة Ventana Medical وهي متوافقة تمامًا مع متغير BigTIFF لتعريف [TIFF](/image/tiff/) الإصدار 6.0.

## تنسيق ملف بيف

يتم حفظ ملف BIF كملف صورة ثنائي ويتكون من ما يصل إلى 200000 × 200000 بكسل. يمكن أن يؤدي هذا إلى أحجام ملفات كبيرة، مما يؤدي إلى كسر الحد الأقصى لحجم 4 جيجابايت الذي تفرضه مؤشرات الملفات 32 بت المحددة بواسطة معيار TIF. ومع ذلك، باستخدام مؤشرات الملفات ذات 64 بت، يتم التغلب على حاجز حجم الملف هذا بواسطة متغير BigTIFF لمعيار TIFF.

### من يستخدم ملف BIF؟

يتم استخدام ملفات BIF بواسطة الماسحات الضوئية للشرائح الرقمية لمسح عينات الشرائح وإنشاء نسخ رقمية منها. إذا كنت متخصصًا في علم الأمراض، فيمكنك فتح ملفات BIF هذه في تطبيقات عرض الشرائح. بفضل المستوى الرائع من التفاصيل والبيانات عالية الدقة، يمكنك تكبير صورة الشريحة وتصغيرها لعرض أقسام العينة بتفاصيل أكثر أو أقل. يحدد ملف البيانات التعريفية [XML](/web/xml/) الموجود في هذه الملفات كيفية دمج الصور، والصورة التي يجب استخدامها كصورة مصغرة للملف.

## كيفية فتح ملف BIF؟

يمكنك فتح ملفات BIF باستخدام:

 * OpenSlide (عبر الأنظمة الأساسية)
 * ImageJ (عبر الأنظمة الأساسية)
 * عارض NetScope (ويندوز)

## مراجع ##

 * [ورقة عمل روش لعلم الأمراض الرقمية BIF](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)
