{
  "date" : "2021-07-29",
  "keywords" :[ "файл shx", "формат файла shx", "что такое файл shx", "файл", "пример shx", "расширение файла shx", "расширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX — формат индекса формы шейп-файла",
  "description":"Узнайте о формате файла SHX и API-интерфейсах, которые могут создавать и открывать файлы SHX.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## .SHX вариант №
Файл SHX относится к формату индекса формы, который представляет собой позиционный индекс геометрии объекта, позволяющий быстро выполнять поиск вперед и назад. SHX — это файл смещения прямого доступа. В этом файле нет никаких данных, только дубликат первой сотни байт, номер записи и смещение до начального байта этой записи в файле shp. Обратите внимание, что файл с расширением .shx не связывает [SHP](/ru/gis/shp/) и [DBF](/ru/database/dbf/).

## Формат файла SHX
Формат SHX содержит позиционный индекс геометрии объекта и 100-байтовый заголовок, аналогичный файлу SHP, за которым следует любое количество 8-байтовых записей фиксированной длины, содержащих следующие два поля:
| Байты | Тип | Порядок байтов | Использование |
-------|-------|------------|---------------------------------|
| 0–3 | интервал32 | большой | Смещение записи (в 16-битных словах) |
| 4–7 | интервал32 | большой | Длина записи (в 16-битных словах) |

Этот индекс позволяет выполнять поиск в обратном направлении в шейп-файле, сначала выполняя поиск в обратном направлении в индексе формы, а затем читая смещение записи. Это смещение можно использовать для поиска правильной позиции в файле SHP. Вы также можете искать вперед; произвольное количество записей с использованием одного и того же метода. Хотя можно создать полный индекс вместе с файлом SHP, но это может увеличить вероятность быстрого повреждения файла SHP.


## использованная литература

* [Shapefile - из Википедии)](https://en.wikipedia.org/wiki/Shapefile)


