{
  "date" : "2023-06-14",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за файловия формат 4DL и API, които могат да създават и отварят 4DL файлове.",
  "title" :"4DL – Регистрационен файл на база данни с 4-то измерение",
  "linktitle" : "4DL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-06-14"
}

## Какво е 4DL файл?

4DL регистрационен файл се използва за записване на модификации, направени във файл с 4D база данни (.4DD). Този файл се съхранява заедно с файла на базата данни и споделя подобно име на файл. Целта му е точно да проследява и поддържа изчерпателен запис на актуализациите, въведени в базата данни. [4DD файл](/bg/database/4dd/), в сравнение с 4DL файла, се свързва главно с 4-тото измерение от 4D Inc.

## 4DL файлов формат - повече информация

Обикновено множество 4DL файлове се съхраняват заедно с 4DD файл. Така първата версия на регистрационния файл може да бъде наречена като 0001.4dl, но страничните версии на регистрационните файлове ще бъдат записани като 0002.4dl, 0003.4dl и т.н. Сега, ако самият лог файл претърпи 3 последователни записвания, той ще бъде етикетиран като "db1[0005-0003].4dl."

## Препратки

* [4DD - Wikipedia](https://en.m.wikipedia.org/wiki/4th_Dimension_(software))
