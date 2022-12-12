{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "розширення", "sav файл", "sav файл формату", "Тип файлу бази даних", "Формат файлу бази даних", "що таке файл Sav" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу SAV та API, які можуть створювати та відкривати файли SAV.",
  "title" :"SAV - файл даних SPSS",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Що таке файл SAV?
Файл SAV – це файл даних, створений у програмі Statistical Package for the Social Sciences (SPSS), яка широко використовується дослідниками ринку, дослідниками охорони здоров’я, дослідницькими компаніями, урядом, дослідниками в галузі освіти, маркетинговими організаціями, дослідниками даних для статистичного аналізу. SAV зберігається у власному двійковому форматі та складається з набору даних, а також словника, які представляють набір даних, зберігає дані в рядках і стовпцях.

## Формат файлу SAV
Формат файлу SAV став відносно стабільним, але ми не можемо сказати, що він статичний. Зворотна та пряма сумісність доступна за потреби, але не підтримується належним чином. Дані у файлі SAV класифікуються за такими розділами:

### Заголовок файлу
Він складається з 176 байт. Перші 4 байти вказують на рядок **$FL2** або **$FL3** у кодуванні символів, що використовується для файлу. Останні три байти означають, що дані у файлі стиснуті за допомогою **ZLIB**. Наступний 60-байтовий рядок починається з **@(#) SPSS DATA FILE** і також визначає операційну систему та версію SPSS, які створили файл. Потім заголовок продовжується шестизначними полями, що містять кількість змінних на спостереження та цифровий код для стиснення, і закінчується символьними даними, що вказують на дату й час створення та мітку файлу.
### Записи дескрипторів змінних
Запис містить фіксовану послідовність полів, що класифікують тип і назву змінної разом з інформацією про форматування, яку використовує SPSS. Кожен запис змінної може додатково містити мітку змінної довжиною до 120 символів і до трьох специфікацій пропущених значень.
### Мітки значень
Мітки значень є необов’язковими та зберігаються в парах записів із цілими тегами 3 і 4. Перший запис, який є тегом 3, містить послідовність пар полів, кожна пара містить значення та відповідну мітку значення. Другий запис, який є тегом 4, представляє, до яких змінних застосовується набір значень/міток.
### Документи
Один або кілька записів з цілим тегом 6. Додаткова документація. містить рядки по 80 символів.
### Записи розширення
Один або декілька записів із цілочисельним тегом 7. Записи розширення надають інформацію, яку можна безпечно ігнорувати, але зберегти у багатьох ситуаціях, що дає змогу зберігати зворотну сумісність файлів, написаних новішим програмним забезпеченням. Записи розширення мають цілочисельні теги підтипу.
### Термінатор словника
Лише запис із цілим тегом 999. Він відокремлює словник від спостережень даних.
### Спостереження даних
Вважається, що дані знаходяться в порядку спостереження, наприклад, усі значення змінних для першого спостереження, а потім усі значення для другого спостереження тощо. Формат запису даних змінюється залежно від коду стиснення в записі заголовка файлу. Частина даних у файлі .sav може бути розпакована:
- **код 0**: стиснутий байт-кодом
- **код 1**: стиснутий за допомогою стиснення ZLIB
 







## Посилання ##

* [Сімейство форматів файлів системних даних SPSS (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)
