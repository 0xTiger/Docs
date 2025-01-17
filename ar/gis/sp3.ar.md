{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - ملف NGS SP3" ,
  "description":"تعرف على تنسيق ملف SP3 وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات SP3 وفتحها." ,
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
} ,
  "lastmod" : "2021-09-29"
}

## ما هو ملف SP3؟

الملف ذو الامتداد .sp3 هو تنسيق مداري للمسح الجيوديسي الوطني (NGS) لتخزين المعلومات المدارية. هذا امتداد لتنسيقات NGS SP1 و SP2 ، ويتضمن معلومات تصحيح ساعة القمر الصناعي التي يتم حسابها في وقت واحد مع المدارات. يعتمد بشكل أساسي على الموقع والساعة ، ولا يشمل السرعات. تم اقتراح التنسيق في Remondi ، 1989 وتم اعتماده في عام 1991. بالإضافة إلى معلومات تصحيح ساعة القمر الصناعي ، فإنه يتضمن معلومات مثل أسس دقة المدار ، وخطوط التعليق ، وأسبوع GPS ، وثواني الأسبوع المرتبطة بالعصر الأول. يمكن فتح ملفات SP3 باستخدام Wolfram Research Mathematica.

## تنسيق ملف SP3 - مزيد من المعلومات

يتم حفظ ملفات SP3 على القرص بتنسيق ملف ASCII ويمكن فتح محتوياتها في أي محرر نصوص لعرضها. يمكن رؤية هيكل ملف SP3 من الصورة التالية.

{{< figure src="../sp3-file-format.png" title="" >}}

## مراجع

* [تنسيق Orbit Standard Product 3 (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar,a%20more%20flexible%20header%20structure)
* [تمديد تنسيقات المدار GPS للمسح الجيوديسي الوطني](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

