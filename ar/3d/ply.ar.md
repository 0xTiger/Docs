{
  "date" : "2019-12-12",
  "keywords" :["PLY" , "ملف" , "امتداد" , "تنسيق" , "تنسيق ملف ثلاثي الأبعاد"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف PLY وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PLY وفتحها." ,
  "title" :"PLY - تنسيق ملف مضلع ثلاثي الأبعاد" ,
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف PLY؟

PLY ، Polygon File Format ، يمثل تنسيق ملف ثلاثي الأبعاد يخزن كائنات رسومية موصوفة كمجموعة من المضلعات. كان الغرض من تنسيق الملف هذا هو إنشاء نوع ملف بسيط وسهل يكون عامًا بما يكفي ليكون مفيدًا لمجموعة كبيرة من النماذج. يأتي تنسيق ملف PLY بتنسيق ASCII بالإضافة إلى تنسيق ثنائي للتخزين المضغوط وللتوفير والتحميل السريع. يتم استخدام تنسيق الملف بواسطة تطبيقات مختلفة توفر دعمًا لقراءة الملفات ثلاثية الأبعاد.

يتم وصف الكائنات بتنسيق PLY من خلال مجموعة من الرؤوس والوجوه والعناصر الأخرى ، جنبًا إلى جنب مع خصائص مثل اللون والاتجاه العادي التي يمكن إرفاقها بهذه العناصر. تشمل الخصائص الأخرى التي يمكن تخزينها أيضًا مع الكائن:

* الأعراف السطحية
* إحداثيات النسيج
* الشفافية
* مدى ثقة البيانات
* خصائص الجزء الأمامي والخلفي من المضلع

يمكن أن يكون الكائن الذي يمثله تنسيق PLY نتيجة لمصادر مختلفة مثل الكائنات الرقمية اليدوية ، وكائنات المضلع من تطبيقات النمذجة ، وبيانات النطاق ، والمثلثات من مكعبات السير ، وبيانات التضاريس ، ونماذج الإشعاع.

## نبذة تاريخية

تم تطوير تنسيق PLY في عام 1990 بواسطة Greg Turk وآخرين في مختبر رسومات ستانفورد ولهذا السبب يُعرف أيضًا باسم Stanford Triangle Format. يحتوي تنسيق الملف على الإصدار 1.0 منذ ذلك الحين ولم يتم إجراء أي تعديلات أخرى.

## تنسيق ملف PLY

يتكون كائن PLY البسيط من مجموعة من العناصر لتمثيل الكائن. يتكون من قائمة (x ، y ، z) ثلاثية من الرؤوس وقائمة الوجوه التي هي في الواقع مؤشرات في قائمة الرؤوس. الرؤوس والوجوه هما مثالان للعناصر وتتكون غالبية ملف PLY من هذين العنصرين. يمكن أيضًا إنشاء خصائص جديدة وإرفاقها بعناصر كائن ، ولكن يجب إضافتها بطريقة لا تتعطل البرامج القديمة عند مواجهة هذه الخصائص الجديدة. يمكن تجاهل هذه الخصائص من خلال قراءة التطبيقات أيضًا. علاوة على ذلك ، يمكن إنشاء عناصر جديدة وتحديد الخصائص باستخدام هذا العنصر أيضًا.

### بنية الملف

تكون بنية ملف تنسيق ملف PLY كما يلي:

| الحقل
---|
| رأس الملف
| قائمة Vertex
| قائمة الوجوه
| قائمة العناصر الأخرى

#### مثال على الهيكل

سنستخدم المثال التالي أدناه في مناقشتنا اللاحقة لأجزاء مختلفة من تنسيق ملف PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### رأس الملف

يتكون رأس تنسيق ملف PLY من نص ASCII لكل من ASCII وكذلك التنسيق الثنائي. يتم تحديد بداية ونهاية قسم الرأس بالكلمات الأساسية الرقيقة والرأس النهائية. تحتوي بداية الرأس على الكلمة السحرية ply التي تُستخدم للتعرف على تنسيق ملف PLY بواسطة القراء. يعرض السطر التالي رقم إصدار هذا الملف. تبدأ التعليقات بتنسيق ملف PLY بكلمة أساسية للتعليق في بداية كل سطر تعليق.

#### الكلمة الرئيسية للعنصر

ثم تخبر الكلمة الأساسية للعنصر ما بداخل الملف. يتبعها خصائص لنوع العنصر المحدد حيث يكون لكل خاصية نوع الخاصية والترتيب المحدد كما هو موضح أدناه:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

في هذا المثال بالذات ، يحتوي عنصر الرأس المحدد على 3 خصائص من النوع float بترتيبها المحدد.

#### أنواع أنواع البيانات

هناك نوعان من أنواع البيانات التي قد تحتوي عليها الخاصية.

"Scalar": أنواع البيانات العددية موضحة أدناه:

| #Name | # النوع | # عدد البايت
| حرف | شخصية | 1
| uchar | حرف غير موقع | 1
| قصير | عدد صحيح قصير | 2
| اختصار | عدد صحيح قصير بدون إشارة | 2
| int | عدد صحيح | 4
| uint | عدد صحيح غير موقع | 4
| طفو | عوامة أحادية الدقة | 4
| مزدوج | تعويم مزدوج الدقة | 8

"القائمة": يوجد نموذج خاص لتعريفات الخاصية يستخدم نوع بيانات القائمة. مثال على ذلك من ملف المكعب أعلاه:

`قائمة الخصائص uchar int vertex_index`

هذا يعني أن الخاصية "vertex_index" تحتوي أولاً على أحرف غير موقعة تخبرنا عن عدد الفهارس التي تحتوي عليها الخاصية ، متبوعة بقائمة تحتوي على هذا العدد من الأعداد الصحيحة. كل عدد صحيح في هذه القائمة ذات الطول المتغير هو فهرس للرأس.

## مراجع ##

* [تنسيق ملف PLY](http://paulbourke.net/dataformats/ply/)
* [PLY - بواسطة Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))

