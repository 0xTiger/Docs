{
  "date" : "2021-06-29",
  "keywords" :["CFG" , "التمديد" , "الملف" , "التنسيق" , "النظام" , "التكوين" , "الإعدادات" , "البرامج" , "الكمبيوتر" , "التطبيق"] ,
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - تنسيق الملف" ,
  "description":"تعرف على تنسيق ملف CFG وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CFG وفتحها." ,
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
} ,
  "lastmod" : "2021-06-29"
}

## CFG ما ه ##

الملف ذو الامتداد .cfg هو نوع من ملفات "الإعدادات". إنه نوع ملف شائع الاستخدام ويستخدم لتخزين المعلومات المتعلقة بالتكوين والإعدادات لبرامج الكمبيوتر. يتم تخزين معظم أنواع ملفات CFG بتنسيق نصي ولا يجب فتحها يدويًا ، وبدلاً من ذلك ، يجب فتحها باستخدام محرر نصوص. ومع ذلك ، هناك أنواع مختلفة من ملفات CFG ، والتي تختلف في التنسيق الذي يتم تخزين المعلومات به. تختلف الميزات التي تقدمها ملفات CFG من تطبيق إلى آخر. تمكّن بعض تطبيقات الكمبيوتر المستخدمين من تعديل أو تطوير بنية ملفات التكوين الخاصة بهم عن طريق استخدام التداخلات الرسومية ، بينما يسمح البعض الآخر بالتعديلات فقط باستخدام محرر نصوص. بعد تعديل هذه الملفات ، يمكن للمستخدمين توجيه التطبيق لقراءة هذه الملفات مرة أخرى وتطبيق التعديلات على النظام.


## تنسيق ملف CFG ##

يتم دعم ملفات CFG بواسطة أنظمة تشغيل مختلفة مثل أنظمة التشغيل التي تشبه Unix و Unix و MS-DOS و macOS و Microsoft Windows و IBM OS / 2. يختلف التنسيق الذي يتم تخزين هذه الملفات واستخدامها في كل من أنظمة التشغيل هذه. تستخدم معظم الأنظمة هذه الملفات وتخزنها بتنسيق نص عادي يمكن قراءته بواسطة الإنسان وقابل للتحرير ، بينما يقوم الآخرون بتخزينه بتنسيق أكثر تعقيدًا ، اعتمادًا على استخدام الملفات ومتطلبات نظام التشغيل.

في أنظمة التشغيل التي تشبه Unix و Unix ، تُستخدم معظم ملفات CFG عدة أنماط تنسيقات مختلفة لملفات CFG ، ومع ذلك ، فإن التنسيق الأكثر شيوعًا هو تنسيق نص عادي يمكن قراءته بسهولة ، وتسمح جميع التنسيقات تقريبًا بعمل التعليقات وتحريرها. امتدادات الملفات الأكثر شيوعًا لملفات CFG في أنظمة التشغيل هذه هي CNF و CONF و CF و INI.

في نظام التشغيل MS-DOS ، كان هناك في البداية تنسيق واحد فقط لملف التكوين ، وهو نص عادي ، ومع ذلك ، فقد جلب MS-DOS 6 معه إدخال تنسيق ملف تكوين INI.

يستخدم macOS ملف تكوين نمط تنسيق قائمة الخصائص القياسي.

في Microsoft Windows ، كانت ملفات تكوين نمط INI للنص العادي مصدرًا مهمًا لتخزين المعلومات وتحريرها ، ومع ذلك ، تم تقديم نظام قاعدة بيانات جديد في عام 1993 ، مما أدى إلى انخفاض في استخدام ملفات التكوين في Microsoft Windows بعد عام 1993.


## مثال CFG ##

يمكن الاطلاع على نموذج ملف CFG أدناه:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```