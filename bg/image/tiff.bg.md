{
  "date" : "2019-10-11",
  "keywords" :[ "tiff файл", "tiff файлов формат", "какво е tiff файл", "файл", "tiff пример", "tiff файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - формат на файл с изображение",
  "description":"Научете за файловия формат TIFF и API, които могат да създават и отварят TIFF файлове.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е TIFF файл?

TIFF или TIF, Tagged Image File Format, представлява растерни изображения, които са предназначени за използване на различни устройства, които отговарят на този стандарт за файлов формат. Той е в състояние да опише двустепенни, скала на сивото, цветни палитри и пълноцветни изображения в няколко цветови пространства. Той поддържа схеми за компресиране със загуби и без загуби, за да избирате между пространство и време за приложения, използващи формата. Форматът не зависи от машината и е свободен от ограничения като процесор, операционна система или файлови системи.

## Кратка история на файловия формат TIFF

Файловият формат TIFF първоначално е създаден от Aldus Corporation през есента на 1986 г. след поредица от срещи с различни производители на скенери и разработчици на софтуер. Основната цел на файловия формат TIFF беше да предостави общ файлов формат за сканирани изображения за всички доставчици на настолни скенери. Започвайки с поддръжката само на двоичен формат на изображението, форматът еволюира до поддръжка на сиви и цветни изображения с течение на времето. Първоначалната версия на спецификациите на файловия формат TIFF може да бъде обозначена като Reivision 3.0, тъй като имаше две по-ранни чернови версии. Голяма ревизия 5.0 беше публикувана през 1988 г., която добави поддръжка за цветни изображения в палитра и LZW компресия. Ревизия 6.0 на файловите формати TIFF беше публикувана през 1992 г. след това. През 1994 г. Adobe Systems придоби Aldus и спецификациите вече са налични и се поддържат от Adobe Systems.

## Спецификации на файловия формат TIFF

Файловият формат TIFF е разширяем и е претърпял няколко ревизии, което позволява включването на неограничено количество лична информация или информация със специално предназначение. TIFF файлът започва с 8-байтово заглавие, където байтовете са числа от 0 до N. Най-големият възможен TIFF файл е с дължина 2**32 байта. Файлът започва с 8-байтово заглавие на файл с изображение, което сочи директно към файл с изображение (IFD). IFD съдържа информация за изображението, както и указатели към действителните данни за изображението.

### Заглавка на TIFF файл

Заглавката на 8-байтовия TIFF файл съдържа следната информация:

**Байтове 0-1:** Редът на байтовете, използван във файла. Законовите стойности са: „II” (4949.H) „MM” (4D4D.H).

Във формат „II“ редът на байтовете винаги е от най-маловажния байт до най-значимия байт както за 16-битови, така и за 32-битови цели числа. Това се нарича ред на байтовете от малкия край. Във формата „MM“ редът на байтовете винаги е от най-значим към най-малко значим както за 16-битови, така и за 32-битови цели числа. Това се нарича порядък на байтовете от голям ред.

**Байтове 2-3:** Произволно, но внимателно избрано число (42), което допълнително идентифицира файла като TIFF файл. Редът на байтовете зависи от стойността на байтовете 0-1.

**Байтове 4-7:** Отместването (в байтове) на първия IFD. Директорията може да бъде на всяко място във файла след заглавката, но трябва да започва от границата на думата. По-специално, директория с файлове с изображения може да следва данните за изображения, които описва. Читателите трябва да следват указателите, където и да ги водят. Терминът байтово отместване винаги се използва в този документ за обозначаване на местоположение по отношение на началото на TIFF файла. Първият байт на файла има отместване 0.

### Директория с файлове с изображения

IFD съдържа информация за изображението, както и указатели към действителните данни на изображението. Състои се от 2-байтов брой на записите в директорията (т.е. броя на полетата), последван от поредица от 12-байтови записи в полета , последвано от 4-байтово отместване на следващия IFD (или 0, ако няма). Трябва да има поне 1 IFD в TIFF файл и всеки IFD трябва да има поне един запис.

#### Вписване в IFD

Всеки 12-байтов IFD запис е в следния формат.


|Байтове|Описание
---|---|
|0-1|Етикетът, който идентифицира полето
|2-3|Типът на полето
|4-7|Брой на посочения тип
|8-11|Отместването на стойността, файловото отместване (в байтове) на стойността за полето. Очаква се стойността да започва от границата на думата; следователно съответното отместване на стойността ще бъде четно число. Това отместване на файла може да сочи навсякъде във файла, дори след данните за изображението

TIFF поле е логическа единица, състояща се от TIFF таг и неговата стойност. Тази логическа концепция се изпълнява като IFD запис плюс действителната стойност, ако не се вписва в частта стойност/отместване, последните 4 байта на IFD записа. Термините TIFF поле и IFD запис са взаимозаменяеми в повечето контексти.

### Базов TIFF ###

Базовият TIFF е ядрото на TIFF, най-важното, което всички масови разработчици на TIFF трябва да поддържат в своите продукти. Съответствието с TIFF формат зависи от спазването на базовите изисквания за TIFF. Тези изисквания са добре документирани в спецификационния документ 6.0.

#### Няколко изображения на файл ####

Може да има повече от един IFD в TIFF файл. Всеки IFD дефинира подфайл. Една потенциална употреба на подфайлове е да описват свързани изображения, като например страниците на факсимилно предаване. Базов TIFF четец не е задължен да чете други IFD освен първия.

#### Типове изображения ####

Базовото TIFF изображение има следните типове:

**Двустепенно:** Изображението на две нива съдържа два цвята — черен и бял. TIFF позволява на приложението да записва данни на две нива във формат бяло е нула или черно е нула. Полето, което записва тази информация, се нарича **PhotometricInterpretation**.

* RGB пълноцветен

Информацията за фотометрична интерпретация за двустепенни изображения е следната:

Етикет = 262 (106.H)
Тип = КРАТКО
**Стойности**

|Стойност|Описание|
---|---|
|0|За изображения на две нива и нива на сивото: 0 се изобразява като бяло. Максималната стойност е изобразена в черно. Това е нормалната стойност за Compression#2|
|1|Черното е нула. За изображения на две нива и нива на сивото: 0 се изобразява като черно. Максималната стойност е изобразена като бяла. Ако тази стойност е указана за Compression#2, изображението трябва да се показва и отпечатва обърнато.|

**Сива скала:** Изображенията с сива скала са обобщение на изображения на две нива. Двустепенните изображения могат да съхраняват само данни за черно-бели изображения, но изображенията в нива на сивото също могат да съхраняват нюанси на сивото. За да опишете такива изображения, трябва да добавите или промените следните полета. Другите задължителни полета са същите като тези, които се изискват за изображения на две нива. За изображения в сива скала, компресия # 1 или 32773 (PackBits). В Baseline TIFF изображенията в сивата скала могат или да се съхраняват като некомпресирани данни, или да се компресират с алгоритъма PackBits.

Информацията **BitsPerSample** за изображения в нива на сивото е както следва:

Етикет = 258 (102.H)
Тип = КРАТКО

Броят битове на компонент. Допустимите стойности за базови TIFF изображения в сива скала са 4 и 8, позволяващи 16 или 256 различни нюанса на сивото.

**Palette-Color:** Изображенията в палитра с цветове са подобни на изображенията в нива на сивото. Те все още имат по един компонент на пиксел, но стойността на компонента се използва като индекс в пълна таблица за търсене на RGB. За да опишете такива изображения, трябва да добавите или промените следните полета. Другите задължителни полета са същите като тези за изображения в сиви нюанси.
Информацията за фотометрична интерпретация за изображението Palette-Color е както следва:

Фотометрична интерпретация = 3 (цветна палитра).
ColorMapTag = 320 (140.H)
Тип = КРАТКО
N = 3 * (2 BitsPerSample)

Това поле дефинира червено-зелено-синя цветова карта (често наричана справочна таблица) за цветни изображения в палитра. В изображение с цвят на палитра се използва стойност на пиксел за индексиране в RGB таблица за търсене. Например, пиксел от цветова палитра със стойност 0 ще бъде показан според 0-ия триплет червено, зелено, синьо. В TIFF ColorMap всички червени стойности са първи, следвани от зелените стойности, след това сините стойности. В ColorMap черното е представено с 0,0,0, а бялото е представено с 65535, 65535, 65535.

**RGB пълноцветен:** В RGB изображение всеки пиксел се състои от три компонента: червен, зелен и син. Няма ColorMap. За да опишете RGB изображение, трябва да добавите или промените следните полета и стойности. Другите задължителни полета са същите като тези, които се изискват за цветни изображения в палитра.

BitsPerSample = 8,8,8. Всеки компонент е дълбок 8 бита в базово TIFF RGB изображение.

PhotometricInterpretation = 2 (RGB) и няма ColorMap.

Етикет = 277 (115.H)
Тип = КРАТКО
Броят компоненти на пиксел. Това число е 3 за RGB изображения, освен ако не са налични допълнителни проби.

## Препратки ##

* [TIFF файлов формат - Wikipedia](https://en.wikipedia.org/wiki/TIFF)
