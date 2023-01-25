{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF - ESRI ArcInfo формат на двоична мрежа",
  "description":"Научете за файловия формат на ADF и API, които могат да създават и отварят ADF файлове.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Какво е ADF файл?

Файл с разширение .adf е файлов формат с растерни данни, използван от софтуерни приложения на ESRI като ArcGIS, ArcView и ArcInfo. Пространствените данни се съхраняват като двоична мрежа, която е естествена за ESRI. Мрежата се състои от редове и колони от клетки, които могат да бъдат цели числа, както и с плаваща запетая. Целочислените мрежи в ADF файл представляват дискретни данни, а решетките с плаваща запетая представляват непрекъснати данни. Друг популярен файлов формат на ESRI е [SHP](/bg/gis/shp/) файл, който представлява геопространствена информация под формата на векторни данни, които да се използват от приложения на Географски информационни системи (GIS).

## ADF файлов формат - повече информация

ADF файловете се записват като двоични файлове на диск в двоична мрежа. Целочислените мрежи имат атрибути, които се съхраняват в таблица с атрибути на стойност (ДДС). Всяка уникална стойност в мрежата има един запис в ДДС, където записът съхранява уникалната стойност и броят на клетките в мрежата е представен от тази стойност.

Мрежите с плаваща запетая нямат ДДС.

### Мрежова структура

Вътре в ADF файла решетките се изпълняват с помощта на подредена растерна структура от данни. Основната единица в тази растерна структура от данни е правоъгълен блок от клетки. Всеки блок се съхранява на диск и се компресира във файлова структура с променлива дължина, наречена плочка. Всеки блок се съхранява като един запис с променлива дължина.

GRID растерите се съхраняват в работни пространства, където работното пространство съдържа една информационна поддиректория и поддиректория за всеки GRID. Има няколко файла с географско местоположение и атрибутни данни за съответната мрежа. Поддиректорията Info съдържа няколко файла, които поддържат определена информация за GRID и други набори от данни, като например покрития, в работното пространство.

## Препратки ##

* [ESRI Grid Format](https://help.arcgis.com/en/arcgisdesktop/10.0/help/index.html#//009t0000000w000000)
* [Често задавани въпроси: Каква е файловата структура на Arc/INFO Grid?](https://support.esri.com/en/technical-article/000008526)
