{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Файлов формат", "Отвори", "Четене", "Създаване", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете повече за HPGL файловия формат и API, които могат да създават и отварят HPGL файлове.",
  "title" :"Файлов формат HPGL – научете се от експерти по файлови формати!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## Какво е HPGL файл?

HPGFL (Hewlett-Packard Graphics Language) файл съдържа набор от инструкции за управление на плотер, разработен от HP. Плотерите на HP използват този файл, за да рисуват и отпечатват векторно и растерно съдържание върху хартията.

### HPGL команда

HPGL команда се състои от следното.
* Команден раздел от азбуката от два знака
* Раздел с параметри
* Раздел Терминатор

Всеки параметър във файла трябва да бъде разделен с разделител в случай на множество параметри.

### Пример за HPGL команда

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Координатна система

Системите за координати се състоят от двуизмерни индикатори за измерване за локализиране на всяко конкретно местоположение. HPGL използва както координатна система на плотера, така и потребителска координатна система за тази цел.

#### Координатна система на плотера

Тази координатна система се използва за изчертаване на чертежи въз основа на движението на плотера. Типичната XY единица за минимално движение на плотера е 0,025 mm. Възможният обхват на чертежа се променя с видовете плотери.

#### Потребителска координатна система

Посочената от потребителя координатна система може да бъде настроена с помощта на мащаба и началото. Те се преобразуват в координати на плотер с помощта на командата IP и командата SC. Системните координати на плотера се използват по подразбиране, ако това преобразуване не е извършено.

## HPGL файлов формат
HPGL файловете са във формат ASCII (текстов файл) и започват с няколко команди за настройка. Това настройва определени параметри на плотера за чертане. Типичен HPGL файл изглежда както следва.

|Команда|Значение
---|---|
|IN;|инициализиране, стартиране на задание за чертане|
|IP;|задайте точките на мащабиране (P1 и P2) на техните позиции по подразбиране|
|SP1;|изберете писалка 1|
|PU0,0;|повдигнете писалката нагоре и се придвижете до началната точка за следващото действие|
|PD100,0,100,100,0,100,0,0;|оставете писалката надолу и се преместете на следните места (начертайте кутия около страницата)|
|PU50,50;|Пуснете нагоре и преминете към X,Y координати 50,50|
|CI25;|начертайте окръжност с радиус 25|
|SS;|изберете стандартния набор от знаци|
|DT*,1;|задайте текстовия разделител на звездичката и не ги отпечатвайте (1, което означава "вярно")|
|PU20,80;|вдигнете писалката и преминете към 20,80|
|LBHello World*;|начертайте етикет|

## Препратки
* [HPGL от Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
* [HPGL Справочно ръководство](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

