{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Файл ZST - формат стисненого файлу Zstandard",
  "description":"Дізнайтеся про формат файлу ZST та API, які можуть створювати та відкривати файли ZST.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-uk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Що таке файл ZST?

Файл ZST — це стислий файл, створений за допомогою алгоритму стиснення Zstandard (zstd). Це стислий файл, створений за допомогою алгоритму зі стисненням без втрат. Файли ZST можна використовувати для стиснення різних типів файлів, таких як бази даних, файлові системи, мережі та ігри. Стандарт Z регулюється [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878), який описує загальний механізм стиснення, тип носія та кодування вмісту.

## Формат файлу ZST

Файли ZST зберігаються на диску у форматі стисненого файлу. Механізм стиснення описано в RFC 8878, який є застарілим RFC 8478.

## Рамки ZST

Файл ZST складається з одного або кількох кадрів. Кожен кадр може бути або стандартним кадром Z, або кадром, який можна пропустити. Фрейм Zstandard містить стислі дані, тоді як фрейм, який можна пропустити, містить власні метадані користувача.

### Zstandard Frame

Фрейм Zstandard має таку структуру.

|Поле|Розмір у байтах|
---|---|
|Магічне_число |4 байти|
|Заголовок_кадру |2-14 байтів|
|Блок_даних |n байт|
|[Більше блоків_даних] ||
|[Content_Checksum] |4 байти|

### Кадр, який можна пропустити

Кадр, який можна пропустити, дозволяє вставляти метадані, визначені користувачем, у потік об’єднаних кадрів. Структура кадру, який можна пропустити, така.

|Magic_Number |Frame_Size |User_Data|
---|---|---|
|4 байти |4 байти |n байт|

## Посилання ##

* [RFC 8878 Zстандартне стиснення](https://www.rfc-editor.org/rfc/rfc8878)


