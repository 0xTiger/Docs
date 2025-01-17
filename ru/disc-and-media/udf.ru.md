{
  "date" : "2021-08-17",
  "keywords" :[ "файл udf", "формат файла udf", "что такое файл udf", "файл", "пример udf", "расширение файла udf", "расширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Узнайте о формате файла UDF и API-интерфейсах, которые могут создавать и открывать файлы UDF.",
  "title" :"UDF — файл универсального формата диска",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## .UDF вариант №
Файл с расширением .udf представляет собой формат образа диска, который обычно используется для сохранения файлов на оптических носителях. можно использовать для записи DVD, CD и других оптических носителей; хранит набор файлов, используя структуру каталогов, указанную в стандарте UDF; позволяет удалять и изменять файлы на целевом диске даже после того, как они были записаны. Ассоциация оптических технологий хранения установила файловую систему UDF в качестве стандарта, чтобы сформировать общую файловую систему для всех оптических носителей, таких как перезаписываемые оптические носители и носители только для чтения.

## Формат UDF-файла
Формат файла UDF представляет собой открытую файловую систему, независимую от поставщика, для хранения компьютерных данных для широкого спектра носителей. Он обычно используется для DVD и более новых форматов оптических дисков. Обычно программное обеспечение обрабатывает файловую систему UDF в пакетном режиме и записывает ее на оптический носитель за один проход. Однако, когда он записывает пакеты на перезаписываемый носитель, UDF позволяет создавать, удалять и изменять файлы на диске, подобно файловой системе общего назначения на съемных носителях, таких как флэш-накопители или дискеты.
### Спецификации UDF
Стандарт UDF определяет следующие три варианта файловой системы:

- **Обычная сборка**: это исходный формат, поддерживаемый во всех версиях UDF. Он был представлен в первой версии стандарта. Этот формат можно использовать на дисках любого типа, допускающих произвольный доступ для чтения или записи, таких как DVD+RW, жесткие диски и носители DVD-RAM.
- **Сборка НДС**: используется специально для записи на однократно записываемый носитель. VAT — это дополнительная структура на диске, позволяющая записывать пакеты; то есть переназначение физических блоков при изменении или удалении файлов или других данных на диске. Для носителей с однократной записью весь диск виртуализируется, что делает природу однократной записи прозрачной для пользователя; с диском можно обращаться так же, как с перезаписываемым диском.
- **Запасная (RW) сборка**: используется специально для записи на перезаписываемый носитель. Он добавляет дополнительную таблицу резервирования для управления ошибками, которые в конечном итоге могут возникнуть на частях диска, которые были перезаписаны несколько раз. Эта таблица сохраняет трек изношенных секторов и переназначает их на рабочие. Управление дефектами UDF не применяется к системам, в которых уже реализована другая форма управления дефектами, например Mount Rainier (MRW) для оптических дисков или контроллер диска для жесткого диска.
 




## использованная литература


* [Формат Windows Imaging — по Википедии](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


