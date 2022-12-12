{
  "date" : "2019-10-11",
  "keywords" :[ "файл bz2", "формат файлу bz2", "що таке файл bz2", "файл", "приклад bz2", "розширення файлу bz2", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - формат стисненого файлу",
  "description":"Дізнайтеся, що таке файл BZ2 та API, які можуть створювати та відкривати файли BZ2.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## Що таке файл BZ2?

BZ2 — це стиснуті файли, створені за допомогою відкритого методу стиснення [BZIP2](http://www.bzip.org/), переважно в системах UNIX або Linux. Він використовується для стиснення одного файлу і не призначений для архівування кількох файлів. Це відрізняється від формату файлу TAR на тих же платформах, який архівує кілька файлів в один файл, але без стиснення. Файли, стиснуті як BZ2, можна розпакувати за допомогою таких програм, як [WinZip](https://www.winzip.com/win/en/). BZIP2 використовує алгоритм стиснення Run-Length Encoding (RLE) або [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) для досягнення високого рівня стиснення.

## Формат файлу BZ2

Для цього формату файлів немає формальних специфікацій. Однак неофіційні [специфікації зворотного проектування] (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) показують, що потік .bz2 складається з 4-байтового заголовка, за яким слідують нульовим або більшою кількістю стиснутих блоків. Одразу слідує маркер кінця потоку, що містить 32-бітний CRC для всього обробленого потоку звичайного тексту. Між стиснутими блоками немає заповнення, і всі блоки вирівняні за бітами.

## Розархівуйте/витягніть файл BZ2

Ви можете розархівувати файл BZ2 у Windows і Mac OS за допомогою програмного забезпечення, наприклад WinZip. У Linux наступна команда в терміналі.

```
bzip2 -d filename.bz2
```

## Список літератури

* [Специфікації формату BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)
