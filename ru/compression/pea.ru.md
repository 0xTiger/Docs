{
  "date" : "2021-04-21",
  "keywords" :[ "файл гороха", "формат файла гороха", "что такое файл гороха", "файл", "пример гороха", "расширение файла гороха", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA — формат файла архива PeaZip",
  "description":"Узнайте о формате файла PEA и API-интерфейсах, которые могут создавать и открывать файлы PEA.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## .PEA вариант №

Файл с расширением .pea (сокращение от Pack, Encrypt и Authenticate) представляет собой архив [zip](/ru/compression/zip/), созданный с помощью программного приложения для архивирования [PeaZip](https://peazip.github.io/). Он поддерживает сжатие и вывод нескольких томов, а также предлагает гибкую модель безопасности с помощью аутентифицированного шифрования и криптографии. Это обеспечивает как конфиденциальность, так и аутентификацию данных. Утилита PeaZip доступна как движок с открытым исходным кодом, который может быть скомпилирован для разных ОС в соответствии с требованиями.

## Формат файла PEA

[Спецификации формата файла PEA](https://peazip.github.io/pea_help.pdf) общедоступны для справки разработчика. Архивы PEA представляют собой двоичные файлы с гибкой моделью безопасности и избыточными проверками целостности, начиная от контрольных сумм и заканчивая криптографически стойкими хэшами. Это определяет три различных уровня связи для управления:

* Потоки - фактический поток выходных данных, который формируется несколькими входными файлами и может быть записан на несколько выходных томов.
* Объекты - входные файлы и папки, отправленные в архив .pea
* Объемы - выходной архивный файл, который может быть увеличен до заданного пользователем размера.

Каждый из них является необязательным и может быть включен в соответствии с требованиями пользователя. Формат файла PEA может хранить один поток, содержащий неограниченное количество объектов. Каждый поток имеет размер до 2^64 байт.

Файлы PEA предлагают дополнительную проверку целостности и аутентифицированное шифрование с использованием AES в режиме EAX или HMAC, либо Twofish и Serpent в режиме EAX.

### Заголовок архива PEA

Заголовок архива имеет размер 10 байт и имеет следующую структуру.

|Байты|Описание|
---|---|
|1 | Поле магического байта для устранения неоднозначности формата файла: $EA|
|1 | Номер версии|
|1 | Номер редакции|
|1 | Схема регулировки громкости|
|1 | Объявление ОС, в которой был построен поток|
|1 | Объявление даты и времени ОС |
|1 | Объявление кодировки символов имен объектов|
|1 | Объявление типа ЦП (закодировано в 7 бит) и порядка следования байтов (в старшем бите) |
|1 | Зарезервировано для использования в будущем|

## использованная литература

* [Спецификации формата файла PEA](https://peazip.github.io/pea_help.pdf)
* [Формат файла PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)

