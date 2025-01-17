{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "Компресиран", "Файл", "Разширение", "Файлов формат", "Lempel-Ziv", "Haruyasu", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файлов формат LZH",
  "description":"Научете за файловия формат LZH и API, които могат да създават и отварят LZH файлове.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Какво е LZH файл? ##

Файл с разширение .lzh и .lha обикновено се отнася до файлов формат за компресиране на архив. Този файлов формат е същият като другите файлови формати за компресиране като [ZIP](/bg/compression/zip/), [RAR](/bg/compression/rar/) и др. Основната цел на тези файлови формати е да намалят размера на формат за лесно изпращане, както и да ги съхранявате заедно в компресиран вид. В сравнение с други западни компании LZH файловете са много популярни в Япония и обикновено се използват за компресиране на данни от видеоигри. Добавката LZH за Windows 7 е вградена в японската версия на Windows 7. Microsoft за първи път пусна Microsoft Compressed (LZH) Folder Add-on за японската версия на Windows XP. Този файлов формат е реализиран с разпоредби за компресиране и функции, използвани от алгоритъма Lempel-Ziv и Haruyasu

## LZH Спецификация ##

Методът на компресиране на LZH архив се показва като петбайтов текстов низ, като -lz1-. Това са трети до седми байтове в компресирания файл.

|Спецификация|Описание|
---|---|
|Разширение | .lzh, .lha|
|Тип медия| приложение/x-lzh-compressed|
|Код на типа| "LHA_" (LHA-ПРОСТРАНСТВО)|
|UTI| public.archive.lha|
|Разработено от| Харуясу Йошизаки (Йоши)|
|Тип| Компресия|
|Разширено от| LArc|

## Проблеми при отваряне на LZH файл ##

Следват няколко проблема, които могат да причинят лоша работа на файловия формат LZH:
  

* Файлът може да е повреден. За да разрешите този проблем, изтеглете файла отново или помолете подателя да изпрати отново файла
* Втората причина е заразен файл, в този случай сканирайте правилно файла
* Неправилни връзки към файла LZH
* Премахване на описанието на LZH
* Няма достатъчно хардуерни ресурси
* Остарели драйвери на оборудването

## Препратки ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
