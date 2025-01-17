{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Стиснутий", "Файл", "Розширення", "Формат файлу", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу LZO",
  "description":"Дізнайтеся про формат файлу LZO та API, які можуть створювати та відкривати файли LZO.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Що таке файл LZO? ##

Файл із розширенням .lzo поєднується з функціями архівування файлів, які можуть зменшити розмір усіх файлів у стисненому файлі. Усі стиснені файли можуть складатися з одного або кількох файлів або навіть груп підшивок із кількома файлами різних типів і розмірів. Розмір стисненого файлу менший порівняно з загальним розміром усіх файлів і папок, що зберігаються у стисненому файлі LZO. Усі стиснуті файли LZO зберігаються у форматі LZO та явно виконуються з функціями стиснення, які використовуються програмним забезпеченням для стиснення та розпакування файлів LZOP. Усі специфікації стиснення об’єднані в цю програму стиснення та декомпресії файлів, яка походить від бібліотеки стиснення файлів Lempel-Ziv-Oberhume. Швидша швидкість декомпресії та підвищені коефіцієнти стиснення також об’єднані в ці файли LZO.

## Специфікація LZO ##

У 1996 році Маркус Франц Ксавер Йоханнес Обергумер розробив оригінальний алгоритм "lzop", заснований на попередніх алгоритмах Абрахама Лемпеля та Якоба Зіва. Ця бібліотека реалізує різноманітні алгоритми з такими характеристиками:

* Швидше стиснення, ніж DEFLATE
* Швидка декомпресія
* Додаткові буфери, необхідні під час стиснення (розміром 8 КБ або 64 КБ, залежно від рівня стиснення)
* Буфери джерела та призначення — це вся пам’ять, необхідна для декомпресії
* Забезпечує контроль як за ступенем стиснення, так і за швидкістю стиснення

Як алгоритм блокового стиснення, LZO виконує стиснення, що перекривається, а також декомпресію на місці. Щоб досягти стиснення, що перекривається, розмір блоку стиснення та декомпресії має збігатися. Алгоритм стиснення LZO розділяє вхідні дані на збіги (ковзний словник) і літерали, які не збігаються, даючи хороші результати з надлишковими даними та прийнятні результати з даними, що не стискаються, лише збільшуючи нестисливі дані на 1/64 вихідних даних. розмір.

## Проблеми з відкриттям файлу LZO ##

Нижче наведено кілька проблем, які можуть спричинити погану роботу формату файлу LZO:
  


* Файл може бути пошкоджений. Щоб вирішити цю проблему, завантажте файл ще раз або попросіть відправника повторно надіслати файл
* Другою причиною є інфікований файл, у цьому випадку скануйте файл належним чином
* Неправильні посилання на файл LZO
* Видалення опису ЛЗО
* Недостатньо апаратних ресурсів
* Застарілі драйвери обладнання
  


## Посилання ##

* [LZO – Вікіпедія](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

