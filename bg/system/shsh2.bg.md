{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH2 файл – iOS SHSH Blob файлов формат",
  "description":"Научете какво е SHSH2 файл.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Какво е SHSH2 файл?

SHSH2 файл, известен също като SHSH blob или ECID SHSH, е цифров подпис, използван от Apple за удостоверяване и проверка на актуализации на фърмуера за iOS устройства като iPhone, iPad и iPod. Той съдържа уникален идентификатор за устройството, който е известен като ECID (Exclusive Chip ID). Той също така съдържа информация за версията на фърмуера, инсталиран на устройството.

## SHSH2 файлов формат - повече информация

SHSH2 файловете се записват на диск в двоичен файлов формат и подробностите за вътрешната файлова структура на този файлов формат не са публично достъпни.

Когато се инсталира нова версия на iOS на устройство на Apple като iPhone, iPad или Mac, се генерира SHSH2 файл. Този SHSH2 файл се изпраща до сървърите на Apple, които четат и проверяват този файл с цифров подпис. Въз основа на тази информация сървърът разрешава или предотвратява инсталирането.

Същото се случва, когато се поиска актуализация. Когато потребител поиска актуализация или възстановяване на своето устройство чрез iTunes или друг софтуер, сървърите на Apple ще проверят дали файлът SHSH2 съответства на ECID на устройството и версията на фърмуера, преди да позволят на актуализацията да продължи.

## Препратки

* [SHSH Blob – от Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)
