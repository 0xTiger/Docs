{
  "date" : "2019-10-11",
  "keywords" :[ "файл mng", "формат файлу mng", "що таке файл mng", "файл", "приклад mng", "розширення файлу mng", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу MNG - формат файлу мережевої графіки з кількома зображеннями",
  "description":"Дізнайтеся про формат файлу MNG та API, які можуть створювати та відкривати файли MNG.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл MNG?

Файл із розширенням .mng — це формат файлу мережевої графіки з кількома зображеннями, схожий на формат зображення [PNG](/uk/image/png/), але підтримує анімовані зображення. Його було розроблено, щоб уникнути перевантаження формату PNG додатковими функціями анімації. MNG також схожий на файли [GIF](/uk/image/gif/), але використовує більше стиснення та підтримує повну альфа-версію. Неофіційним типом носія MIME для файлів MNG є video/x-mng. Файли MNG можна відкривати в таких програмах, як ImageMagik і IrfanView.

## Формат файлу MNG

Формат файлу MNG схожий на формат PNG і використовує таку саму структуру фрагментів, як визначено в специфікаціях PNG. Декодер MNG повинен мати можливість декодувати потоки даних PNG без вказівки будь-яких спеціальних прапорів для інструкцій декодування. MNG об’єднує кілька зображень у «рамку», де деякі зображення використовуються як спрайти для переміщення з одного місця в інше. Механізм дозволяє повторно використовувати дані зображення без їх повторної передачі. [Специфікації MNG] (http://www.libpng.org/pub/mng/spec/) можна переглянути для довідки розробника.

### Підпис MNG

Потік даних MNG починається з 8-байтового підпису, який містить:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Це схоже на підпис PNG, але містить MNG замість PNG.

### Кадр MNG

Кадр MNG складається з двовимірного зображення менших зображень. До кожного маленького зображення можна отримати доступ за допомогою комбінації індексів рядків і стовпців. Формат здатний зберігати тривимірні «воксельні» дані, які розташовані в серії двовимірних площин. Кожна площина представлена потоком даних PNG або Delta-PNG. Кожен потік даних Delta-PNG визначає зображення як відмінності від батьківського зображення PNG. Це забезпечує набагато більш компактний спосіб представлення наступних зображень, ніж використання повного потоку даних PNG для кожного.

## Посилання ##

* [MNG](http://www.libpng.org/pub/mng/)
* [Формат MNG v 1.0](http://www.libpng.org/pub/mng/spec/)
