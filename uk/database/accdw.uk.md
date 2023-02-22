{
  "date" : "2021-08-30",
  "keywords" :[ "ACCDW", "розширення", "файл", "формат файлу", "Тип файлу бази даних", "Формат файлу бази даних", "Файли бази даних" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу ACCDW та API, які можуть створювати та відкривати файли ACCDW.",
  "title" :"ACCDW - файл посилання на базу даних Microsoft Access",
  "linktitle" : "ACCDW",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-30"
}

## Що таке файл ACCDW?

Файл із розширенням .accdw — це файл посилання, створений за допомогою Microsoft Access і містить інформацію про посилання для завантаження файлу бази даних Access, наприклад [ACCDB](/uk/database/accdb/) із сервера SharePoint. Це дозволяє користувачам ділитися файлами бази даних, які розміщені віддалено. Відкриття файлу ACCDW завантажує пов’язаний файл ACCDB як локальну копію на комп’ютері користувача. Завантажений файл зберігається в місці завантаження за замовчуванням, і до нього можна отримати доступ, перейшовши до нього. Зазвичай ці файли завантажуються та зберігаються під іменем «SiteServer.accdb», яке відноситься до клієнтських баз даних.

## Формат файлу ACCDW – Додаткова інформація

Файл ACCDW — це XML-файл, який містить посилання на сайт SharePoint, де розміщено служби доступу. Це лише ярлик, і для їх запуску потрібне підключення до Інтернету. У разі роботи в Інтернеті SharePoint кешується локально, щоб надати можливість перевести його в автономний режим пізніше.

## Список літератури

* [Завантажений файл .accdw](http://channel9.msdn.com/shows/Access/)
* [Технічні характеристики Access 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Завантаження файлу .accdw](https://social.technet.microsoft.com/Forums/en-US/7bf02e9e-6246-44da-9513-4cf8f2cc2fb2/downloaded-accdw-file?forum=sharepointgeneralprevious)
* [Який формат файлу Access слід використовувати?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41?ui=en-us&rs=en-us&ad=us)
