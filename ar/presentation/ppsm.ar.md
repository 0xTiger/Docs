{
  "date" : "2019-10-11",
  "keywords" :["ملف ppsm" , "تنسيق ملف ppsm" , "ما هو ملف ppsm" , "ملف" , "مثال ppsm" , "امتداد ملف ppsm" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - ملف عرض PowerPoint تقديمي ممكّن بماكرو" ,
  "description":"تعرف على تنسيق ملف PPSM وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PPSM وفتحها." ,
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف PPSM؟

تمثل الملفات ذات امتداد PPSM تنسيق ملف عرض الشرائح ممكّن بماكرو تم إنشاؤه باستخدام Microsoft PowerPoint 2007 أو إصدار أحدث. تنسيق ملف آخر مشابه هو [PPTM] (/ar/ العرض التقديمي / pptm /) والذي يختلف في الفتح باستخدام Microsoft PowerPoint بتنسيق قابل للتحرير بدلاً من التشغيل كعرض شرائح. عند تشغيله كعرض شرائح ، يعرض ملف PPSM شرائح العرض التقديمي مع محتويات سليمة في عرض الشرائح ويكون في وضع القراءة فقط افتراضيًا. لا يزال من الممكن تحرير ملفات PPSM في Microsoft PowerPoint عن طريق فتحها في PowerPoint.

## تنسيق الملف ##

تم تقديم تنسيق ملف PPSM مع PowerPoint 2007 وهو يعتمد على تنسيق ملف OpenXML الذي يستخدم مزيجًا من XML و [ZIP] (/ar/ compression / zip /) لتخزين محتوياته. الملفات التي تم إنشاؤها باستخدام تنسيق ملف Office Open XML عبارة عن مجموعة من ملفات XML جنبًا إلى جنب مع الملفات الأخرى التي توفر روابط بين جميع الملفات المكونة. هذه المجموعة هي في الواقع أرشيف مضغوط يمكن استخراجه لعرض محتوياته. للقيام بذلك ، ما عليك سوى إعادة تسمية امتداد الملف PPSM باستخدام zip واستخراجه لمراقبة محتوياته.

المقاطع التالية تلقي بعض الضوء على كل واحد من هؤلاء.

### [أنواع_المحتوى] .xml ###

هذا هو الملف الوحيد الذي يتم العثور عليه في المستوى الأساسي عند استخراج ملف zip. يسرد أنواع المحتويات للأجزاء داخل الحزمة. تتم الإشارة إلى كافة الإشارات إلى ملفات XML المضمنة في الحزمة في ملف XML هذا. فيما يلي نوع محتوى لجزء شريحة:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
إذا كانت هناك حاجة إلى إضافة أجزاء جديدة إلى الحزمة ، فيمكن القيام بذلك عن طريق إضافة الجزء الجديد وتحديث أي علاقات داخل ملفات. يجب أن يؤخذ في الاعتبار أنه لمثل هذا التغيير ، يجب أيضًا تحديث Content_Types.xml.

### \ _ برميل (مجلد) ###

يتم الحفاظ على العلاقات بين الأجزاء والموارد الأخرى خارج الحزمة من خلال جزء العلاقات. يحتوي المجلد "العلاقات" على ملف XML واحد يخزن العلاقات على مستوى الحزمة. يحتوي هذا الملف على ارتباطات للأجزاء الرئيسية لملفات العرض التقديمي كمعرفات URI. تحدد URIs نوع العلاقة بين كل جزء رئيسي والحزمة. يتضمن ذلك العلاقة بمستند المكتب الأساسي الموجود على هيئة ppt / Present.xml وأجزاء أخرى داخل docProps كخصائص أساسية وممتدة.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
كل جزء من المستند يمثل مصدرًا لعلاقة واحدة أو أكثر سيكون له جزء العلاقات الخاص به حيث يتم العثور على كل جزء من هذه العلاقة داخل مجلد فرعي \ _براميل للجزء ويتم تسميته بإلحاق "براميل" باسم جزء. يحتوي جزء المحتوى الرئيسي (Present.xml) على جزء العلاقات الخاص به (Present.xml.rels). يحتوي على علاقات بأجزاء أخرى من المحتوى مثل slideMaster1.xml و notesMaster1.xml و handoutMaster1.xml و slide1.xml و presProps.xml و tableStyles.xml و theme1.xml بالإضافة إلى URIs للروابط الخارجية.

#### علاقة صريحة ####

بالنسبة للعلاقة الصريحة ، تتم الإشارة إلى المورد باستخدام سمة المعرف الخاصة بـ<Relationship> عنصر. أي أن المعرّف الموجود في المصدر يعيّن مباشرةً معرّف عنصر العلاقة ، مع إشارة صريحة إلى الهدف.

على سبيل المثال ، قد تحتوي الشريحة على ارتباط تشعبي مثل هذا:
```
<a:hlinkClick r:id#"rId2">
```
يشير r: id # "rId2" إلى العلاقة التالية ضمن جزء العلاقات للشريحة (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### العلاقة الضمنية ####

بالنسبة للعلاقة الضمنية ، لا توجد مثل هذه الإشارة المباشرة إلى ``<Relationship> المعرف بدلا من ذلك ، يتم فهم المرجع.

### مجلد ppt ###

هذا هو المجلد الرئيسي الذي يحتوي على كافة التفاصيل حول محتويات العرض التقديمي. بشكل افتراضي ، يحتوي على المجلدات التالية:

* \ _ براميل
* سمة
* الشرائح
* تخطيطات الشرائح
* سلايد ماسترز

وملفات xml التالية:

* عرض. xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## مراجع ##

* [تنسيق ملف عرض OpenXML] (https://msdn.microsoft.com/en-us/library/dd926741 (v # office.12) .aspx)
* [Open Office XML] (http://officeopenxml.com/anatomyofOOXML-pptx.php)
