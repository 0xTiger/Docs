{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "пристрій Rocket eBook від Nuvo Media", "файл", "розширення", "формат", "електронна книга" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу RB для пристрою Nuvo Media Rocket eBook та API, які можуть створювати та відкривати файли RB.",
  "title" :"RB - файл електронної книги Rocket",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Що таке файл RB?

Файл із розширенням .rb містить вміст електронної книги Rocket. Електронна книга Rocket насправді є пристроєм, виготовленим компанією Nuvo Media; вони випустили цей пристрій у 1998 році. Хоча Rocket eBook здатний відображати зображення, але лише в чорно-білому режимі. Він має екран 106 dpi або 480 x 320 пікселів на 4,5 x 3-дюймовому сенсорному екрані. Rocket eBook підключається до комп’ютера через послідовний порт для завантаження електронних книг у форматі RB. Файли RB можуть використовувати DRM, але ця технологія не використовується в сучасних електронних книгах. Файл RB традиційно містить файл HTML із зображеннями та файл псевдо-OPF з усіма метаданими (.info).

## Технічні характеристики формату файлу RB ##

Магічне число (у шістнадцятковому) відображається в перших 4 байтах файлу: B0 0C B0 0C.

Схоже, що наступні два байти є номером версії, як-от «02 00», що означає основну версію 2 і додаткову версію 0.

Наступні чотири байти містять текст "NUVO", за яким слідують 4 байти 00h.

Наступні 4 байти — це дата створення книги, закодована як int16. Це ставить нас на зсув 0Eh. Стара версія ORocketLibrary кодувала повне значення року (тобто 1999 був "CF 07", 2000 був "D0 07"). В останній версії tm_year зберігається дослівно, тобто 100 для 2000 року ("64 00"). Після року йде int8, що представляє 1 відносне число місяця, і int8, що представляє день місяця.

Наступні 6 байтів - це 00h. Для встановлення часу їх можна зарезервувати.

Абсолютне зміщення «Змісту» міститься в int32 зі зміщенням 18h.

Після цього є int32, що містить довжину файлу .rb. Це використовується для визначення повності файлів чи ні.

Уся ця частина байтів (від 20 до 128 годин) потрібна лише для зашифрованого заголовка. У незашифрованих заголовках вони завжди дорівнюють нулю.

У більшості випадків слідує зміст (зі зміщенням 128). Він починається з підрахунку int32 кількості записів "сторінки" (розділів файлу .rb) у ToC. Кожен запис складається з імені (доповненого нулем до 32 байтів), за яким слідують 3 int32: довжина сегмента даних, позиція у файлі .rb і прапор для цього запису. На сьогодні відомі такі значення: 1 (зашифровано), 2 (інформаційна сторінка) і 8 (дефльовано). Усі назви підбираються за потреби, щоб гарантувати їх унікальність.

## Список літератури

* [E-Reader - від MobileRead](https://en.wikipedia.org/wiki/E-reader)
