{
  "date" : "2021-07-28",
  "keywords" :[ "файл ntf", "формат файла ntf", "что такое файл ntf", "файл", "пример ntf", "расширение файла ntf", "расширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF — файлы в формате передачи в национальном формате",
  "description":"Узнайте о формате файлов NTF и API, которые могут создавать и открывать файлы NTF.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## .NTF вариант №
Файлы с расширением .ntf называются файлами **National Transfer Format (NTF)**; в основном используется Управлением боеприпасов Великобритании (OS); специально для передачи геопространственных данных. Он управляется Британским институтом стандартов. Он стал стандартным форматом передачи цифровых данных Ordnance Survey. Проекция National Grid Великобритании, которая является разновидностью поперечной проекции Меркатора, содержит всю информацию с географической привязкой для файлов NTF.

## Формат файла NTF
Формат файла NTF принадлежит Ordnance Survey в Соединенном Королевстве; поддерживается библиотекой GDB для импорта. Текущая версия формата файла NTF — 2.0. Этот формат файла был введен для устранения ограничения векторного сегмента **PCIDSK**, который имеет только одно поле атрибута на структуру, но существует множество атрибутов, которые можно извлечь из векторных данных. Чтобы обойти формат файла NTF, он состоит из двух сегментов. Каждый сегмент состоит из одних и тех же векторов, но с разными атрибутами. Первый сегмент векторного файла NTF содержит векторы с кодовым номером объекта в качестве атрибута. Второй сегмент содержит векторы со значением в качестве атрибута.

### Система координат
Библиотека GDB представляет растровые и векторные данные с соответствующими характеристиками проекции ТМ:

- Базовая долгота: 49,0
- Базовая широта: 2,0
- Ложный восток: 400000
- Ложный север: -100000
- Масштаб: 0,9996012717
- Эллипсоид: Эйри 1830 (E009)
Недоступна поддержка обновления или записи файлов NTF, а также нельзя связать файлы DTM.

### Пример огринфо
В следующем примере используется **ogrinfo** в файле NTF для получения номеров слоев:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## использованная литература

* [Национальный формат передачи Великобритании (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Веб-картографирование — иллюстрации Тайлера Митчелла](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

