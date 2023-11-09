{
   "date":"2023-07-18",
   "keywords":[
      "PAR",
      "PAR File",
      "how to open a par file",
      "file",
      "PAR file extension",
      "extension",
      "file"
   ],
   "author":{
      "display_name":"Shakeel Faiz"
   },
   "draft":"false",
   "toc":true,
   "title":"PAR File Format - Parchive Index File",
   "description":"تعرف على تنسيق PAR وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PAR وفتحها.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
         "parent":"compression"
      }
   },
   "lastmod":"2023-07-18"
}

## ما هو ملف PAR؟

ضمن أرشيفات Parchive (PAR)، يشير ملف .par إلى ملف فهرس يحتوي على مجموعة من وحدات تخزين التماثل أو كتل التماثل. يتم استخدام ملف الفهرس هذا لأغراض اكتشاف الأخطاء والاسترداد عند فقدان أو تلف ملف واحد أو أكثر في الأرشيف.

يتكون أرشيف Parchive عادةً من ملفات البيانات الأصلية ووحدات تخزين التكافؤ المقابلة. يتم إنشاء مجلدات التكافؤ باستخدام خوارزميات تصحيح الأخطاء Reed-Solomon. تحتوي وحدات تخزين التماثل هذه على معلومات متكررة يمكن استخدامها لاستعادة ملفات البيانات الأصلية.

يحتوي الملف .par، المعروف أيضًا باسم مجموعة وحدات تخزين التماثل، على معلومات حول بنية وموقع وحدات تخزين التماثل داخل الأرشيف. إنه بمثابة فهرس أو خريطة لعملية الاسترداد. باستخدام ملف .par، يمكن لبرنامج PAR المتخصص تحديد وحدات تخزين التكافؤ المطلوبة وكيفية استخدامها لإعادة بناء الملفات المفقودة أو التالفة.

عندما يتعذر الوصول إلى ملف واحد أو أكثر داخل أرشيف Parchive أو يصبح تالفًا، يمكن استخدام الملف .par جنبًا إلى جنب مع وحدات تخزين التكافؤ المتاحة لاستعادة البيانات المفقودة. يقرأ برنامج PAR ملف .par، ويحدد الملفات المفقودة أو التالفة، ويستخدم وحدات تخزين التكافؤ لإعادة بنائها.

## كيفية فتح ملف PAR؟

لفتح ملفات .par واستخدامها، ستحتاج إلى برنامج PAR متخصص. فيما يلي بعض خيارات البرامج الشائعة التي يمكنها التعامل مع ملفات .par:

- **QuickPar:** QuickPar هو برنامج PAR مستخدم على نطاق واسع لنظام التشغيل Windows. يسمح لك بإنشاء ملفات PAR والتحقق منها وإصلاحها. يمكنك فتح ملف .par في QuickPar للتحقق من سلامته أو استخدامه لإصلاح الملفات التالفة أو المفقودة في أرشيف Parchive.

- **MultiPar:** MultiPar هو برنامج PAR شائع آخر متاح لنظام التشغيل Windows. وهو يدعم تنسيقات الملفات PAR وPAR2 ويوفر ميزات متقدمة لإنشاء الأرشيفات والتحقق منها وإصلاحها. يمكن لـ MultiPar فتح ملفات .par وتنفيذ عمليات الكشف عن الأخطاء والاسترداد بناءً على وحدات تخزين التكافؤ المتوفرة.

- **MacPAR deLuxe:** MacPAR deLuxe هو برنامج PAR مصمم خصيصًا لنظام التشغيل macOS. وهو يدعم تنسيقات الملفات PAR وPAR2 ويوفر وظائف مشابهة مثل QuickPar وMultiPar. يمكن لـ MacPAR deLuxe فتح ملفات .par والمساعدة في التحقق من الأرشيفات واستعادة الملفات التالفة أو المفقودة.

## تنسيق ملف PAR - مزيد من المعلومات

تنسيق الملف PAR، والذي يشار إليه عادة باسم Parchive، هو تنسيق ملف محدد يستخدم لإنشاء بيانات التكافؤ واكتشاف الأخطاء والاسترداد في أرشيفات الملفات. يتكون تنسيق ملف PAR عادة من ثلاثة أنواع: PAR، وPAR2، وPAR3.

- **PAR:** تم تطوير تنسيق ملف PAR الأصلي، والمعروف أيضًا باسم PAR1، بواسطة مشروع Parchive. ويتضمن بيانات التكافؤ التي تم إنشاؤها من ملفات البيانات الأصلية. توفر ملفات PAR مستوى أساسيًا من اكتشاف الأخطاء واستعادتها، ولكنها تحتوي على قيود فيما يتعلق بقدرات تصحيح الأخطاء.

- **PAR2:** PAR2 هو نسخة محسنة من تنسيق ملف PAR. فهو يوفر إمكانات أكثر تقدمًا لتصحيح الأخطاء وميزات استرداد محسنة. تُستخدم ملفات PAR2 عادةً لإنشاء بيانات التكافؤ التي يمكنها استرداد الملفات المفقودة أو التالفة داخل الأرشيف. توفر ملفات PAR2 حماية أفضل ضد تلف البيانات وتستخدم على نطاق واسع لأغراض أرشفة الملفات.

- **PAR3:** PAR3 هو أحدث إصدار من تنسيق ملف PAR ويوفر المزيد من التحسينات في تصحيح الأخطاء واستعادتها. فهو يوفر مستويات أعلى من التكرار وقدرات تصحيح الأخطاء مقارنة بـ PAR2. تم تصميم ملفات PAR3 لتوفير خيارات حماية واسترداد أكثر قوة للبيانات المخزنة في الأرشيف.

يتم دعم تنسيقات الملفات PAR2 وPAR3 على نطاق واسع بواسطة برنامج PAR وتوفر القدرة على التحقق من سلامة الملفات داخل الأرشيف واستعادة البيانات المفقودة أو التالفة. لا تزال ملفات PAR وPAR2 شائعة الاستخدام، بينما تكتسب ملفات PAR3 اعتماداً تدريجيًا نظرًا لقدراتها المحسنة على تصحيح الأخطاء.

## مراجع
* [Parchive](https://en.wikipedia.org/wiki/Parchive)