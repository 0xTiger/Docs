{
  "date" : "2021-04-08",
  "keywords" :["ملف lz4" , "تنسيق ملف lz4" , "ما هو ملف lz4" , "ملف" , "lz4 مثال" , "امتداد ملف lz4" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف مضغوط LZ4 - LZ4" ,
  "description":"تعرف على تنسيق ملف LBR وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات LZ4 وفتحها." ,
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
} ,
  "lastmod" : "2021-04-19"
}

## ما هو ملف LZ4؟

الملف بامتداد .lz4 هو ملف أرشيف مضغوط تم إنشاؤه باستخدام تطبيقات / أدوات مساعدة تدعم ضغط [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)). تركز خوارزمية LZ4 على المفاضلة بين السرعة ونسبة الضغط. يمكن إنشاء أرشيفات LZ4 المضغوطة باستخدام الأداة المساعدة لسطر الأوامر LZ4 ويمكن فك ضغطها باستخدام نفس الأداة.

## تنسيق ملف LZ4

تنسيق ملف LZ4 ، المستند إلى خوارزمية ضغط LZ4 ، مستقل عن نوع وحدة المعالجة المركزية ونظام التشغيل ونظام الملفات ومجموعة الأحرف. إنه مناسب لضغط الملفات وضغط التدفق باستخدام خوارزمية LZ4. تم تنفيذ التنفيذ الأولي لتنسيق LZ4 بلغة [C](/ar/programming/c/) بواسطة Yann Collet في عام 2011 وهو متاح كمرجع للمطور على [Github](https://github.com/lz4/lz4) .

### تنسيق الإطار LZ4

الهيكل العام لتنسيق ملف LZ4 كما هو موضح أدناه.

| MagicNb | F. الواصف | منع | (...) | علامة النهاية | ج. اختباري |
---|---|---|---|---|---|
| 4 بايت | 3-15 بايت ||| 4 بايت | 0-4 بايت |

#### الرقم السحري

4 بايت ، تنسيق Endian صغير. القيمة: 0x184D2204

#### واصف الإطار

يتكون واصف الإطار من 3 t0 15 بايت وهو الجزء الأكثر أهمية في المواصفات. يُشار إلى الحقلين Magic_Number و Frame_Descriptor معًا باسم LZ4 Frame Header ويتراوح حجمه بين 7 و 19 بايت. كما هو موضح أدناه.

| FLG | BD | (حجم المحتوى) | (معرف القاموس) | HC |
---|---|---|---|---|
| 1 بايت | 1 بايت | 0 - 8 بايت | 0 - 4 بايت | 1 بايت |

#### كتل البيانات

كل كتلة بيانات تتبع الترتيب التالي.

| حجم الكتلة | البيانات | (المجموع الاختباري للكتلة) |
---|---|---|
| 4 بايت | | 0-4 بايت |

#### علامة النهاية

ينتهي تدفق الكتل عندما تتبع آخر كتلة بيانات بقيمة 32 بت 0x00000000.

#### المجموع الاختباري للمحتوى

يتحقق Content_Checksum من صحة المحتوى الذي يتم فك تشفيره بشكل صحيح ويتم تنفيذه باستخدام نتيجة خوارزمية xxHash-32. إنه يتحقق من صحة نتائج الإرسال الناجح لجميع الكتل بالترتيب الصحيح وبدون أي خطأ.

## مراجع

* [تنسيق إطار LZ4](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [LZ4 Compression Algorithm - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

