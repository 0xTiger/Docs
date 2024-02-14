{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "برنامج Shell النصي - كيفية تشغيله على Ubuntu وLinux",
  "description":"برنامج Shell النصي - كيفية تشغيله على Ubuntu وLinux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## ما هو برنامج شل النصي؟

تتضمن البرمجة النصية لـ Shell كتابة سلسلة من الأوامر في ملف نصي عادي، يُشار إليه غالبًا باسم **Shell Script**. يتم تنفيذ هذه البرامج النصية بواسطة Shell، وهو مترجم سطر الأوامر. تشمل القذائف الأكثر شيوعًا

1. باش (بورن مرة أخرى شل)
2. Zsh (Z شل)
3. سمكة.

يمكن أن تتراوح نصوص شل النصية من البرامج البسيطة إلى البرامج المعقدة، ويتم استخدامها لأداء مجموعة واسعة من المهام، مثل معالجة الملفات، وإدارة النظام، وأتمتة المهام المتكررة.

## فوائد البرمجة النصية لـ Shell:

1.  **الأتمتة:** تسمح البرامج النصية لـ Shell للمستخدمين بأتمتة المهام المتكررة، مما يوفر الوقت ويقلل من فرصة حدوث خطأ بشري.
    
2.  **التخصيص:** يمكن للمستخدمين إنشاء نصوص برمجية مصممة خصيصًا لتلبية احتياجاتهم الخاصة، مما يوفر درجة عالية من التخصيص.
    
3.  **معالجة الدفعات:** تعتبر البرامج النصية لـ Shell ممتازة للتعامل مع مهام المعالجة المجمعة، حيث يجب تنفيذ أوامر متعددة بالتسلسل.
    
4.  **إدارة النظام:** تُستخدم البرامج النصية لـ Shell بشكل شائع في مهام إدارة النظام، مثل النسخ الاحتياطية وتدوير السجل وتثبيت البرامج.

## كتابة نص شل بسيط:

لنقم بإنشاء برنامج نصي أساسي لـ Shell يطبع رسالة ترحيب. افتح محرر نصوص وأنشئ ملفًا باسم greeting.sh. أضف الأسطر التالية:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

احفظ الملف واجعله قابلاً للتنفيذ عن طريق تشغيل الأمر التالي في الجهاز:

```
chmod +x greeting.sh
```

الآن يمكنك تنفيذ البرنامج النصي:

```
./greeting.sh
```

يجب أن يكون الإخراج:

```
Hello, welcome to the world of shell scripting!
```

## تشغيل برامج Shell النصية على Ubuntu وLinux:

سنناقش الآن **كيفية تشغيل ملف .sh في Ubuntu وLinux**.

1.  **اجعل البرنامج النصي قابلاً للتنفيذ:** قبل تشغيل برنامج Shell النصي، تأكد من أنه قابل للتنفيذ. استخدم الأمر `chmod` كما هو موضح سابقًا.
    
2.  ** انتقل إلى دليل البرامج النصية: ** افتح محطة طرفية واستخدم الأمر `cd` للانتقال إلى الدليل الذي يحتوي على برنامج Shell النصي الخاص بك.
    
3.  **تشغيل البرنامج النصي:** قم بتنفيذ البرنامج النصي عن طريق كتابة `./scriptname.sh` في الوحدة الطرفية، مع استبدال scriptname بالاسم الفعلي للبرنامج النصي الخاص بك.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **استخدام أمر Bash:** إذا كان البرنامج النصي الخاص بك يبدأ بـ `#!/bin/bash` (المعروف باسم **shebang**)، فيمكنك أيضًا تشغيله باستخدام الأمر `bash`.

```
bash greeting.sh
```

## ماذا يعني $@ في Shell Script؟

في برنامج Shell النصي، يمثل `$@` كافة وسائط سطر الأوامر التي تم تمريرها إلى البرنامج النصي. غالبًا ما يتم استخدامه للإشارة إلى قائمة الوسائط ككيانات منفصلة. عند استخدامها ضمن علامات اقتباس مزدوجة، مثل `$@`، فإنها تحافظ على الوسائط الفردية، مع مراعاة المسافات والأحرف الخاصة.

وهنا شرح مختصر:

- `$@`: يمثل كافة المعلمات الموضعية (الوسائط) التي تم تمريرها إلى البرنامج النصي أو الوظيفة. يتم التعامل مع كل وسيطة على أنها كلمة منفصلة.
    
- `$@`: عند وجود علامات اقتباس مزدوجة، يحافظ على الفصل بين الوسائط، مما يسمح بالمسافات أو الأحرف الخاصة داخل الوسائط الفردية.
    

وهنا مثال بسيط للتوضيح:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

عند تشغيل هذا البرنامج النصي مع الوسائط، على سبيل المثال:

```
bash example.sh arg1 "argument 2" arg3
```

من شأنه أن يخرج:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

كما ترى، يمثل `$@` جميع الوسائط، ويحتفظ `$@` بالوسائط الفردية، حتى لو كانت تحتوي على مسافات.
