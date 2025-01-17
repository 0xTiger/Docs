{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ملف SHSH - تنسيق ملف SHSH Blob لجهاز iPhone/iPod Touch",
  "description":"تعرف على ما هو ملف SHSH.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## ما هو ملف SHSH؟

ملف SHSH, المعروف أيضًا باسم Signature HaSH, هو توقيع رقمي تستخدمه Apple للمصادقة والتحقق من تحديثات البرامج الثابتة لأجهزة iOS مثل iPhone وiPad وiPod.

## الفرق بين تنسيقات الملفات SHSH وSHSH2

مثل ملف SHSH2, يحتوي ملف SHSH على معرف فريد للجهاز يسمى "ECID" (معرف الشريحة الحصري), بالإضافة إلى معلومات حول إصدار البرنامج الثابت المثبت على الجهاز. ومع ذلك, تم استخدام ملفات SHSH في الإصدارات الأقدم من iOS (قبل iOS 10) وتم استبدالها منذ ذلك الحين بملفات SHSH2.

## تنسيق ملف SHSH - مزيد من المعلومات

يتم حفظ ملفات SHSH على القرص بتنسيق ملف ثنائي. تفاصيل بنية الملف الداخلية لتنسيق الملف هذا غير متاحة للعامة.

تعد ملفات SHSH مهمة للمستخدمين الذين يرغبون في الرجوع إلى إصدار سابق من البرامج الثابتة لأجهزتهم إلى إصدار سابق لم تعد شركة Apple موقعة عليه. من خلال حفظ ملفات SHSH لإصدار برنامج ثابت محدد عندما لا يزال قيد التوقيع بواسطة Apple, يمكن للمستخدمين استخدامها لاحقًا لتجاوز التحقق من توقيع Apple وتثبيت إصدار البرنامج الثابت هذا على أجهزتهم. تُعرف هذه العملية أيضًا باسم "كسر الحماية".

## مراجع

* [SHSH Blob - بواسطة ويكيبيديا](https://en.wikipedia.org/wiki/SHSH_blob)
* [توفير خدمات الدعم الفني](https://tsssaver.1conan.com/v2/)

