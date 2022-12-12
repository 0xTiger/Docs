{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c", "що таке файл ac", "як відкрити файл c", "розширення", "файл", "файл c", "формат файлу c", "розширення файлу c"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл програмування мовою C - C",
  "description":"Дізнайтеся про формат файлу C та API, які можуть створювати та відкривати файли C.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Що таке файл C?

Файл, збережений із розширенням c, є файлом вихідного коду, написаним мовою програмування C. **Файл C** містить усю реалізацію функцій програми у формі вихідного коду. Оголошення вихідного коду записується у файлах заголовків, які зберігаються з розширенням [.h](/uk/programming/h/). C++ — це сучасна форма мови C, яка сьогодні використовується для розробки більшості програмного забезпечення.

## Коротка історія

Мова Сі виникла в результаті створення різних утиліт для операційної системи UNIX. Деніс Річі, людина, що стоїть за створенням цієї мови програмування, спочатку розпочала роботу в 1960-х і на початку 1970-х років.

## Формат файлу C

Файли C записуються у форматі звичайного текстового файлу відповідно до синтаксису мови програмування. Типовий файл C матиме:

* оператор import у верхній частині файлу для імпорту будь-яких файлів заголовків
* один або кілька методів реалізації бажаної функціональності

### Імпорт заголовків

Файли заголовків із розширенням .h містять необхідні оператори включення для включення інших функціональних файлів у проект. Крім того, вони містять оголошення методів, визначених у файлі реалізації. Файли заголовків включаються за допомогою оператора include, як показано нижче.

```
#include <filename.h>
```

### Реалізація вихідного коду

Фактична реалізація функціональних вимог закодована як методи у файлі C. Кожен метод у файлі C має тип повернення, назву методу та може мати деякі вхідні параметри. Якщо тип повернення не пустий, можливо, метод повертає певне значення.

### Приклад коду C
Ось приклад програми ac:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Посилання** ##

* [Реалізація класу - Вікіпедія](https://en.wikipedia.org/wiki/Class_implementation_file)
