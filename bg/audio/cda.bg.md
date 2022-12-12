{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "файл", "разширение", "формат", "какво е cda файл", "музика", "cda файлов формат", "cda спецификация на файлов формат"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за CDA файловия формат и API, които могат да създават, конвертират и отварят CDA файлове.",
  "title" :"CDA - Файл за бърз достъп до аудио запис на CD",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Какво е CDA файл?

Файл с разширение .cda е малък файл-мъничък, генериран от Microsoft Windows за всеки аудио запис на аудио компактдиск. Тези файлове съдържат типична информация като времена на песните и пряк път на Windows, който позволява на потребителите да имат достъп до конкретни аудио записи. CDA файловете не са музика, но те сочат към музикален файл, който съществува някъде в хранилището. Можем да го кажем като пряк път на аудио файл, който се намира на CD.

## CDA файлов формат

Файловият формат CDA се използва, за да каже на компютъра кой аудио файл да възпроизведе на CD. Така че CDA файловете стават безполезни, отделени от CD, който представляват. CDA файловете обикновено се считат за RIFF ресурси. Има само една част, която се нарича "CDDA" и съдържа само един блок данни, наречен "FMT " в текущата версия на .cda файла. Този блок е дълъг 24 байта. Идентификаторът, създаден от Windows, се използва от свързаното с Windows 95 и Windows 98 CD устройство и неговият плейър не може да се свърже с FreeDB или CDDB. За да може да показва заглавието на песента и името на изпълнителя, трябва ръчно да въведете тази информация във файла cdplayer.ini.

### Организация на CDA файл

Следващата таблица показва информацията за типичните компенсации:
| офсет | дължина | съдържание |
---|---|---|
| 0x00 | 4 | 4-те ASCII знака "RIFF" |
| 0x04 | 4 | размера на следното парче: винаги 36 (44 - 8), на 4 байта (Intel ред) |
| 0x08 | 4 | идентификатор на парче: 4-те ASCII знака "CDDA" |
| 0x0C | 4 | 3-те ASCII знака "fmt", последвани от интервал |
| 0x10 | 4 | дължина на парчето: винаги 24, на 4 байта (Intel ред) |
| 0x14 | 2 | версия на CD формат, на 2 байта (Intel поръчка). През май 2006 г. винаги е равно на 1. |
| 0x016 | 2 | номер на диапазона, на 2 байта (Intel ред). Първата песен е с номер 1. |
| 0x18 | 4 | идентификатор, изчислен от Windows за cdplayer.exe. |
| 0x1c | 4 | отместване на диапазона, в брой кадри (Intel ред) |
| 0x20 | 4 | продължителност на песента, общ брой кадри (Intel order) |
| 0x24 | 1 | позиция на диапазона: рамки |
| 0x25 | 1 | позиция на обхват: секунди |
| 0x26 | 1 | позиция на диапазона: минути |
| 0x27 | 1 | нулев байт (двоична стойност 0) |
| 0x28 | 1 | продължителност на песента: кадри |
| 0x29 | 1 | продължителност на песента: секунди |
| 0x2a | 1 | продължителност на песента: минути |
| 0x2b | 1 | нулев байт (двоична стойност 0) |

## Препратки

* [.cda файл - от Wikipedia](https://en.wikipedia.org/wiki/.cda_file)
