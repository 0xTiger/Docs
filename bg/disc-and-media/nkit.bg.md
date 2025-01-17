{
  "date" : "2022-04-01",
  "keywords" :[ "nkit файл", "nkit файлов формат", "какво е nkit файл", "файл", "nkit пример", "nkit файлово разширение", "разширение", "формат", "nkit долен колонтитул", "файл формат на nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Научете за NKIT файловия формат и API, които могат да създават и отварят NKIT файлове.",
  "title" :"NKIT - Файлов формат на дисково изображение",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Какво е NKIT файл?

NKIT файл е дисково изображение на данни, извлечени от игри NintendoWii и GameCube. NKIT е за формат на Nintendo Toolkit. Полученият компресиран [ISO](/bg/compression/iso/) файл използва основните данни от тези игри, за да се стартира с емулаторни програми като Dolphin, Swiss и Nintendont. NKit се предлага в необработени (iso) и компресирани (gcz) файлови формати, които и двата са проектирани, за да имат предвид възпроизвеждането и размера.

## Файлов формат NKIT

Файловият формат NKit е формат без загуба и се използва за свиване и възстановяване на изображения на Nintendo Wii и GameCube. Форматите са налични във файлови формати ISO и GCZ за всяка от игрите GameCube и Wii.

|Система |Формат |Поддържан хардуер |Поддържан Dolphin |Възстановяем 1:1 |Бележки|
---|---|---|---|---|---|
|GameCube| nkit.iso| Да |Да| Да |Същото като компактния GameCube iso|
|GameCube| nkit.gcz| Не| Да| Да |GCZ е собствен формат на Dolphin за компресиране с възможност за търсене|
|Wii| nkit.iso| Не Да| Да| RVT-H формат, възпроизвеждан само в Dolphin|
|Wii| nkit.gcz| Не Да| Да| RVT-H в GCZ може да се играе само в Dolphin|

### NKIT заглавка

Заглавката на файловия формат NKIT е както следва.

|Отместване |Дължина |Име|
---|---|---|
|0x200 |0x4 |NKit Заглавие 'NKIT'|
|0x204 |0x4 |NKit версия 'v01'|
|0x208 |0x4 |Изходно изображение оригинал CRC32|
|0x20C |0x4 |NKit CRC - прави NKit файла CRC32 равен на CRC източника при 0x208 (при 0x4 в GCZ)|
|0x210 |0x4 |Дължина на изходното изображение|
|0x214 |0x4 |Принудителен нежелан идентификатор (Когато ID на диска е различен - рядко - само за GameCube)|
|0x218 |0x4 |Wii Update дял CRC32, ако е премахнат при конвертиране|

## Препратки ##

* [Файлов формат NKIT - от gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

