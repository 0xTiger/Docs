{
"дата":"2023-11-09",
   "keywords":[
"зоопарк",
"зоофайл",
"стиснутий файл зоопарку",
"як відкрити зоофайл",
"файл",
"розширення файлу zoo",
"розширення",
"файл"
],
   "author":{
"display_name":"Шейкіл Фаїз"
},
"чернетка":"хибний",
"toc":true,
"title":"Файл ZOO - Що таке файл .zoo і як його відкрити?",
   "description":"Дізнайтеся про формат стисненого файлу ZOO та API, які можуть створювати та відкривати файли ZOO.",
   "linktitle":"ZOO",
   "menu":{
      "docs":{
         "identifier":"compression-zoo",
         "parent":"compression"
}
},
"lastmod":"2023-11-09"
}

## Що таке файл ZOO?

Файл `.zoo` — це формат архіву, який використовується для стиснення та зберігання файлів і каталогів; подібний до інших форматів архівів, таких як `.zip`, `.tar` і `.rar`. Формат `.zoo` був популярний на початку розвитку комп’ютерів, але останнім часом став менш поширеним. Його спочатку розробив **Rahul Dhesi** і використовувався в основному в системах Unix і DOS.

Файл `.zoo` зазвичай містить один або кілька файлів і каталогів, які були стиснуті та заархівовані в один файл. Ви можете створювати та видобувати файли `.zoo` за допомогою різних програмних засобів, які підтримують цей формат.

Архіви ZOO мають унікальну функцію, яка дозволяє зберігати кілька версій одного файлу за умови, що кожна версія була змінена в різну дату. Це означає, що користувачі ZOO можуть зберігати та отримувати доступ до попередніх ітерацій файлу безпосередньо з архіву ZOO. Ця функція дозволяє користувачам повернутися до попередньої версії файлу або порівняти стару версію з новішою, пропонуючи зручний спосіб керувати версіями файлів і змінами з часом.

## Загальні операції з файлами ZOO

Ось деякі звичайні операції, пов’язані з файлами `.zoo`:

1. **Створення файлу `.zoo`:** Ви можете використовувати утиліту командного рядка, наприклад "zoo", щоб створити файл `.zoo`. Наприклад, наступна команда створить архів `.zoo` з каталогу:
    








`zoo a -c каталог archive.zoo/`
    








У цій команді "a" означає "add", "-c" визначає стиснення, а "archive.zoo" є назвою вихідного архіву.
    








2. **Витягування файлів із файлу `.zoo`:** Щоб розпакувати вміст архіву `.zoo`, ви можете використати таку команду:
    








`zoo e archive.zoo`
    








Ця команда витягне файли з файлу `archive.zoo`.
    








3. **Перелік вмісту файлу `.zoo`:** Ви можете перерахувати вміст `.zoo` архіву, не розпаковуючи його за допомогою параметра "l":
    








    








`zoo l archive.zoo`

## Як відкрити файл ZOO?

Програми, які відкривають файли ZOO, включають

- **zoo** (безкоштовно) для (Windows, Linux)

## Список літератури
* [Zoo (file format)](https://en.wikipedia.org/wiki/Zoo_(file_format))