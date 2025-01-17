{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 — формат файла Microsoft OneNote",
  "description":"Узнайте о формате файлов ONETOC2 и API-интерфейсах, которые могут создавать и открывать файлы ONETOC2.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Что такое ОНЕТОК2? ##

Те, кто работал с приложением [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app), могли заметить наличие файлов .onetoc2 в папке блокнота. Microsoft OneNote создает двоичный файл .onetoc2 в качестве оглавления для хранения указателя порядка различных разделов заметок в записной книжке. Записная книжка — это набор файлов разделов, которые хранятся в одном каталоге. Файл .onetoc2 использует набор свойств для указания таких параметров, как порядок разделов в записной книжке и цвет записной книжки.

Когда вы создаете записную книжку в OneNote 2016, она автоматически сохраняется в новом формате файла 2010–2016. Этот формат понадобится вам, если вы хотите, чтобы все функции OneNote 2016, такие как математические уравнения и связанные заметки, работали правильно.

## Формат файла ONETOC2 ##

Формат файла .onetoc2 представлен как формат файла хранилища редакций OneNote и представляет собой набор структур, определяющих хранилище редакций, организованное в пространства объектов с перекрестными ссылками, содержащее объекты с наборами свойств и журнал транзакций для обеспечения целостности файлов в асинхронном режиме. пишет. Полные спецификации для формата файла .onetoc2 доступны [онлайн](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) и могут использоваться для разработки приложений .

### Структура файла ###

Файл хранилища изменений ДОЛЖЕН начинаться со структуры **Заголовок**. Оставшаяся часть файла разделена на блоки байтов, где размер и структура каждого блока определяется полем, которое на него ссылается. Блок достижим, если на него ссылается структура **Заголовок** или если на него ссылается поле в другом достижимом блоке. Данные вне структуры **Заголовок** и любые достижимые блоки ДОЛЖНЫ игнорироваться.

Все структуры выровнены по 1-байтовым границам. Все целые числа имеют знак, если не указано иное. Все поля имеют формат [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), если не указано иное.

#### Заголовок ####

Заголовок файла .ONE состоит из фрагментов, которые содержат различные уникальные идентификаторы и поля для представления информации о файле следующим образом:

`guidFileType (16 байтов):` GUID, указывающий тип файла хранилища изменений. ДОЛЖНО быть одним из значений из следующей таблицы.

|Формат файла|Значение
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 байтов):` GUID, указывающий идентификатор этого файла хранилища изменений. ДОЛЖЕН быть глобально уникальным.

`guidLegacyFileVersion (16 байтов):` ДОЛЖНО быть "{00000000-0000-0000-0000-000000000000}" и ДОЛЖНО игнорироваться.

`guidFileFormat (16 байтов):` GUID, указывающий, что файл является файлом хранилища изменений. ДОЛЖЕН быть "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 байта):` Целое число без знака. ДОЛЖЕН быть одним из значений в следующей таблице, в зависимости от типа файла.

|Формат файла|Значение
--- | --- |
|.один|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 байта):` Целое число без знака. ДОЛЖЕН быть одним из значений в следующей таблице, в зависимости от формата этого файла.


|Формат файла|Значение
--- | --- |
|.один|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 байта):` Целое число без знака. ДОЛЖЕН быть одним из значений в следующей таблице, в зависимости от формата этого файла.
:


|Формат файла|Значение
--- | --- |
|.один|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 байта):` Целое число без знака. ДОЛЖЕН быть одним из значений в следующей таблице, в зависимости от формата этого файла.


|Формат файла|Значение
--- | --- |
|.один|0x0000002A
|.onetoc2|0x0000001B

## Использованная литература ##

* [[MS-ONESTORE] — формат файла OneNote](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote — Википедия](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

