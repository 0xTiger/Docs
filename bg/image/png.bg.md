{
  "date" : "2019-10-11",
  "keywords" :[ "png файл", "png файлов формат", "какво е png файл", "файл", "png пример", "png файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PNG файлов формат - файл с растерно изображение",
  "description":"Научете повече за PNG файловия формат и API, които могат да създават и отварят PNG файлове.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е PNG файл?

Файлът **PNG** (Portable Network Graphics) е файлов формат на растерно изображение, който използва компресия без загуби. Този файлов формат е създаден като заместител на формата за обмен на графики ([GIF](/bg/image/gif/)) и няма ограничения върху авторските права. Файловият формат PNG обаче не поддържа анимации. Файловият формат PNG поддържа компресиране на изображения без загуби, което го прави популярен сред потребителите. С течение на времето PNG се превърна в един от широко използваните файлови формати за изображения.

## Кратка история на файловия формат PNG

Основната причина за създаването на PNG файловия формат е патентованият алгоритъм за компресиране Lempel-Ziv-Welch, използван във файловия формат GIF. Това заедно с други GIF ограничения създаде необходимост от замяна на файловия формат [**GIF**](/bg/image/gif/). Първото предложение и име за PNG файлов формат дойде през януари 1995 г. Ключовите събития по отношение на PNG файловите формати са изброени по-долу:

* Октомври 1996 г.: Версия 1.0 на PNG спецификациите бяха пуснати и по-късно се появиха като [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. Същото стана препоръка на W3C през октомври 1996 г.
* Декември 1998: Версия 1.1, с някои малки промени и добавяне на три нови части, беше пусната.
* Август 1999: Версия 1.2, добавяща едно допълнително парче, беше пусната.
* Ноември 2003 г.: PNG става международен стандарт (ISO/IEC 15948:2003). Тази версия на PNG се различава само малко от версия 1.2 и не добавя нови части.
* Март 2004 г.: ISO/IEC 15948:2004

## Функционално сравнение на GIF и PNG

PNG файловият формат е проектиран да бъде прост и преносим, правно необременен, взаимозаменяем, гъвкав и здрав. Следващата таблица изброява GIF функциите, които са наследени от PNG файловия формат в допълнение към новите функции.

|Функция|GIF|PNG|
---|---|---|
|Индексни цветни изображения с до 256 цвята|Да|Да|
|Поддръжка за стрийминг|Да|Да|
|Прозрачност|Да|Да|
|Допълнителна информация|Да|Да|
|Независимост от хардуер и платформа|Да|Да|
|В сила|Да|Да|
|Truecolor изображения с до 48 бита на пиксел|Не|Да|
|Изображения в нива на сивото до 16 бита на пиксел|Не|Да|
|Пълен алфа канал (общи маски за прозрачност)|Не|Да|
|Информация за гамата на изображението|Не|Да|
|Надеждност|Не|Да|
|По-бързо първоначално представяне|Не|Да|

## PNG файлова структура

Почти всички операционни системи имат поддръжка за отваряне на PNG файлове. Например Microsoft Windows Viewer има способността да отваря PNG файлове, тъй като операционната система има по подразбиране поддръжката, налична като част от инсталацията. PNG файлът се състои от PNG „подпис“, последван от поредица от //късове//.

### Заглавка на PNG файл

Първите осем байта на PNG файл винаги съдържат следните (десетични) стойности:

{{{137 80 78 71 13 10 26 10 }}}

Този подпис показва, че останалата част от файла съдържа едно PNG изображение, състоящо се от поредица от части, започващи с част IHDR и завършващи с част IEND.

### парчета ###

Всяка част се състои от четири части:

**Дължина:** 4-байтово цяло число без знак, даващо броя на байтовете в полето с данни на частта. Дължината отчита само полето с данни, а не самото себе си, кода на типа парче или CRC. Нулата е валидна дължина. Въпреки че енкодерите и декодерите трябва да третират дължината като без знак, нейната стойност не трябва да надвишава 231 байта.

**Тип на парче:** 4-байтов код на тип на парче. За удобство при описанието и при разглеждането на PNG файлове, типовите кодове са ограничени да се състоят от главни и малки ASCII букви (AZ и az или 65-90 и 97-122 десетични знаци). Въпреки това енкодерите и декодерите трябва да третират кодовете като фиксирани двоични стойности, а не като символни низове. Например, не би било правилно да се представи кодът на типа IDAT чрез EBCDIC еквивалентите на тези букви. Допълнителни конвенции за именуване на типове парчета са обсъдени в следващия раздел.

**Данни на парчето:** Байтовете данни, подходящи за типа на парчето, ако има такива. Това поле може да бъде с нулева дължина.

**CRC:** 4-байтов CRC (циклична проверка на излишъка), изчислен върху предходните байтове в частта, включително кода на типа на частта и полетата с данни за частта, но не включително полето за дължина. CRC винаги присъства, дори за парчета, които не съдържат данни.

Дължината на данните на частта може да бъде произволен брой байтове до максимума; следователно, изпълнителите не могат да приемат, че парчетата са подравнени на граници, по-големи от байтове.

Частите могат да се появяват в произволен ред, предмет на ограниченията, поставени за всеки тип част. (Едно забележително ограничение е, че IHDR трябва да се появи първи, а IEND трябва да се появи последен; по този начин частта IEND служи като маркер за край на файла.) Могат да се появят множество части от един и същи тип, но само ако е специално разрешено за този тип.

#### Типове парчета

Типовете парчета са категоризирани в **Критични** и **Допълнителни** парчета въз основа на 4-байтовата ASCII стойност, чувствителна към главни и малки букви, присвоена на типа парче. Всички реализации трябва да разбират и рендират успешно стандартните критични парчета. Валидно PNG изображение трябва да съдържа IHDR парче, едно или повече IDAT парчета и IEND парче.

### Компресия

PNG метод за компресиране 0 (единственият метод за компресиране, който понастоящем е дефиниран за PNG) указва компресия за намаляване/раздуване с плъзгащ се прозорец от най-много 32768 байта. Компресирането на Deflate е производно на LZ77, използвано в zip, gzip, pkzip и сродни програми. Проведени са обширни изследвания в подкрепа на статута му на свободен от патенти. Компресираните данни в zlib потока от данни се съхраняват като поредица от блокове, всеки от които може да представлява необработени (некомпресирани) данни, LZ77-компресирани данни, кодирани с фиксирани кодове на Huffman, или LZ77-компресирани данни, кодирани с потребителски кодове на Huffman. Маркерен бит в последния блок го идентифицира като последен блок, което позволява на декодера да разпознае края на компресирания поток от данни.

#### Филтриране преди компресия

Прилагат се филтри за предварително компресиране, за да се подготвят данните за изображението за оптимално компресиране. PNG филтърният метод дефинира пет основни типа филтри, както следва:

|Тип филтър|Име|Предвидена стойност|
---|---|---|
|0|Няма|Линията за сканиране се предава непроменена|
|1|Sub|Предава разликата между всеки байт и стойността на съответния байт на предишния пиксел.|
|2|Up|Филтърът Up() е точно като Sub() филтъра, с изключение на това, че пикселът непосредствено над текущия пиксел, а не само отляво, се използва като предиктор.|
|3|Average|Филтърът Average() използва средната стойност на двата съседни пиксела (отляво и отгоре), за да предвиди стойността на пиксел.|
|4|Paeth|Филтърът Paeth() изчислява проста линейна функция на трите съседни пиксела (отляво, горе, горе вляво), след което избира като предиктор съседния пиксел, който е най-близо до изчислената стойност.|

Алгоритмите за филтриране се прилагат към „байтове“, а не към пиксели, независимо от битовата дълбочина или вида на цвета на изображението. Алгоритмите за филтриране работят върху последователността от байтове, образувана от линия за сканиране. Ако изображението включва алфа канал, алфа данните се филтрират по същия начин като данните за изображението.

Когато изображението е преплетено, всяко преминаване на шаблона на преплитане се третира като независимо изображение за целите на филтрирането. Филтрите работят върху последователностите от байтове, образувани от пикселите, действително предадени по време на преминаване, и "предишната сканираща линия" е тази, която е била предадена преди това в същото преминаване, а не съседната в пълното изображение. Обърнете внимание, че подизображението, предавано във всеки един проход, винаги е правоъгълно, но е с по-малка ширина и/или височина от цялото изображение. Филтрирането не се прилага, когато това подизображение е празно.

## Препратки ##

* [PNG - начална страница](http://www.libpng.org/pub/png/)
