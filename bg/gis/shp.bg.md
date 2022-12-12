{
  "date" : "2019-10-11",
  "keywords" :[ "shp файл", "shp файлов формат", "какво е shp файл", "файл", "shp пример", "shp файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - ESRI Shapefile",
  "description":"Научете за SHP файловия формат и API, които могат да създават и отварят SHP файлове.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е SHP файл?

SHP е файловото разширение за един от основните типове файлове, използвани за представяне на ESRI Shapefile. Той представлява геопространствена информация под формата на векторни данни, които да се използват от приложенията на Географските информационни системи (ГИС). Форматът е разработен като отворени спецификации, за да се улесни оперативната съвместимост между ESRI и други софтуерни продукти.

## Представяне на данни

Както споменахме, форматът на шейпфайл описва геопространствената информация на набор от данни като векторни характеристики. Тези векторни характеристики включват:

* точки
* линии
* многоъгълници

Тези характеристики в комбинация могат да представляват почти всякакъв тип форми като водни кладенци, граници на страната, пространствени точки, реки, езера и т.н. Всеки векторен елемент може да има атрибути, които всъщност определят целта на този елемент. Например шейп файл, съдържащ градове на Лос Анджелис, може да има име на града и температура като атрибути, което дава смислено представяне на пространствените данни.

## Свързани файлове

Самостоятелен shp файл не може да се използва от софтуерни приложения, за да осмислят данните, които съдържа. За да осмисли информацията, съдържаща се в такъв файл, шейпфайлът използва следните допълнителни задължителни файлове.

* shx файл - индексен файл
* dbf файл - dBASE файл, който съхранява всички атрибути на фигурите в основния файл
* prj файл - съхранява информация за проекта на файла

Може да има и други незадължителни файлове, които споделят същото име като основния файл.

## Спецификации на SHP файлов формат

Отворените спецификации на shapefile са достъпни онлайн от ESRI под формата на [Technical Description](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) и разработват цялостната структура на файла в детайли. Информацията в главния .shp файл се състои от заглавки и записи. Заглавката на файла с фиксирана дължина е последвана от записи с променлива дължина, където всеки запис е съставен от заглавка на запис с фиксирана дължина, последвана от съдържание на запис с променлива дължина.

### Основен заглавен файл на SHP

Главният хедър на файла започва от началото на файла и е с дължина 100 байта. Организацията на този главен файлов хедър заедно с позицията на байта, стойността, типа и реда на байтовете е както е показано в следващата таблица.


|Байтове|Поле|Стойност|Тип|Ред на байтовете
---|---|---|---|---|
|0-3|Код на файла|9994|Цяло число|Голям редиан
|4-23|Неизползвано|0|Цяло число|Голям редиан
|24-27|Дължина на файла|Дължина на файла|Цяло число|Голям редиан
|28-31|Версия|1000|Цяло число|Little Endian
|32-35|Тип фигура|Тип форма|Цяло число|Little Endian
|36-67|Минимален ограничаващ правоъгълник|Xmin, Ymin, Xmax и Ymax|double|Little Endian
|68-83|Ограничаваща кутия|Zmin, Zmax|двойно|Little Endian
|84-99|Ограничаваща кутия|Mmin, Mmax|двойно|

Трябва да се отбележи, че стойността на дължината на файла е общата дължина на файла в 16-битови думи, която също включва петдесетте 16-битови думи, съставляващи заглавката.

#### Типове форми

Стойностите на полето тип форми в горната таблица са както следва:


|Стойност|Тип форма
---|---|
|0|Нулева форма
|1|Точка
|3|Полилиния
|5|Многоъгълник
|8|Многоточков
|11|Точка Z
|13|PolyLineZ
|15|Многоъгълник Z
|18|MultiPointZ
|21|Точка М
|23|PolyLineM
|25|Многоъгълник M
|28|MultiPointM
|31|MultiPatch

### Записи на данни ###

Заглавката на основния файл е последвана от записи с променлива дължина, като всеки запис се състои от заглавка на запис с фиксирана дължина, последвана от съдържание на запис с променлива дължина.

#### Заглавие на запис ####

Заглавката на записа съдържа информация за номера на записа и дължината на съдържанието на записа с фиксирана дължина от 8 байта. Организацията на заглавката на записа е както е показано по-долу:


|Байтове|Поле|Стойност|Тип|Ред на байтовете
---|---|---|---|---|
|0-3|Номер на запис|Номер на запис|Цяло число|Голям
|4-7|Дължина на запис|Дължина на запис|Цяло число|Голям

#### Съдържание на запис ####

Съдържанието на запис във шейпфайл се състои от тип форма, последван от геометричните данни за тази форма. Тип форма 0 представлява нулева форма, която няма геометрични данни за формата. Дължината на съдържанието на записа е отражение на частите и върховете на формата. Нека вземем пример за тип Point Shape, за да разберем как записът съдържа информация за такъв тип форма.

Точка представлява определено географско местоположение в реда X,Y, където всяка координата е представена със стойност с двойна точност. Следващата таблица показва подредбата на тип форма Point.


|Байтове|Тип на формата|Стойност|Тип|Число|Ред на байтовете
---|---|---|---|---|---|
|0-3|Тип фигура|1|Цяло число|1|Малко
|4-11|X|X|двойно|1|Малко
|12-19|Y|Y|двойно|1|Малко

Примери за други типове форми могат да бъдат намерени в документа с техническо описание на ESRI.

## Препратки ##

* [Техническо описание на ESRI Shapefile] (http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) от ESRI
