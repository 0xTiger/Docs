{
  "date" : "2020-03-16",
  "keywords" :[ "STL файл", "Формат", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за STL файловия формат и API, които могат да създават и отварят STL файлове.",
  "title" :"STL файлов формат",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е STL файл?

STL, съкращение за стереолитрография, е взаимозаменяем файлов формат, който представлява 3-измерна повърхностна геометрия. Файловият формат намира своето приложение в няколко области като бързо създаване на прототипи, 3D печат и компютърно подпомагано производство. Той представлява повърхност като поредица от малки триъгълници, известни като фасети, където всеки фасет е описан от перпендикулярна посока и три точки, представляващи върховете на триъгълника. Резултатните данни се използват от приложенията за определяне на напречното сечение на 3D формата, която трябва да бъде изградена от производителя. Няма налична информация във файловия формат STL за представяне на цвят, текстура или други общи [CAD](/bg/cad/) атрибути на модела.

## Кратка история ##

Разработването на файловия формат STL датира от 1987 г. Той е разработен от 3D Systems за използването му в търговски 3D принтери. Ревизирана версия на файловия формат STL, известна като STL 2.0, беше предложена през 2009 г. с актуализации на файловия формат.

## Спецификации на файловия формат ##

STL файлът представлява повърхностна геометрия с помощта на фасети. Фасетите определят повърхността на 3D обект и се идентифицират уникално чрез единична нормала, която е линия, перпендикулярна на триъгълника с дължина 1,0, и чрез три върха. Има общо 12 числа, съхранени за всеки фасет като нормален и всеки връх е определен с три координати всеки. StL файлът не съдържа информация за мащаба; координатите са в произволни единици.

Спецификациите на файловия формат STL могат да бъдат разгледани от следните два аспекта.

### Ориентация на фасетите ###

Ориентацията на фасет се определя от посоката на единичната нормала и реда, в който са изброени върховете. Ориентацията на фасетите се определя по два начина, както следва:

* Посоката на нормалата е навън
* Върховете са изброени в ред обратно на часовниковата стрелка отвън, като се подчиняват на правилото за дясната ръка.

### Правило от връх до връх ###

Според това правило всеки триъгълник споделя два върха с всеки от съседните му триъгълници. По този начин връх на един триъгълник не може да лежи на страната на друг триъгълник.

## Файлови формати ##

STL е наличен в ASCII, както и в двоични представяния за компактен файлов формат.

### STL ASCII формат ###

ASCII версията на файловия формат STL е написана в обикновен ASCII. Въпреки това, поради големия си размер, файловият формат не е избран като предпочитан формат за използване. Синтаксисът на ASCII STL файл е както следва:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
Думите с удебелен шрифт представляват ключови думи, които винаги трябва да са с малки букви. Символите в курсив са променливи, които трябва да бъдат заменени със зададени от потребителя стойности. Числените данни в редовете **faset normal** и **vertex** са плаващи единици с единична точност, например 1,23456E+789. Координатата на **фасет нормална** може да има водещ знак минус; координата **върх** може да не е така.

### STL двоичен формат ###

Двоичният формат използва IEEE цяло число и числено представяне с плаваща запетая. Файловият формат е представен по следния начин:

|Поле|Информация|
---|---|
|Заглавие|80 знака|
|Брой триъгълници|4-байтово цяло беззнаково число|
|Данни за всеки триъгълник|12 32-битови числа с плаваща запетая|

По-подробен изглед на файловия формат е както е показано по-долу.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Препратки ##

* [Форматът STL](http://www.fabbers.com/tech/STL_Format)
* [STL - от Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))

