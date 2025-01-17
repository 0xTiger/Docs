{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKS файлов формат",
  "keywords" :[ "mks", "matroska видео", "mkv формат", "файл", "формат", "видео"],
  "description":"Научете за файловия формат MKS за субтитри, създадени само от Matroska и API, които могат да създават и отварят MKS файлове.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Какво е MKS файл?

MKS файловете обикновено са известни като Matroska файлове, съдържащи само субтитри. Въпреки че Matroska е общ файлов контейнер, той избягва съхраняването на информация в специфични формати. Тъй като субтитрите се използват в някои от аудио или видео контейнерите, Matroska обръща внимание на съхраняването на някои общи формати на субтитри. Помага на Matroska да бъде в съответствие с темпа на растеж. Трябва да следвате точките, дадени по-долу, за да съхраните субтитрите в Matroska:

- „.mks“. разширението ще се използва от файла Matroska (съдържащ само субтитри).
- **CodecPrivate** се използва за съхраняване на цялата информация, свързана с кодеци, която е глобална за целия поток.
- Премахнете клеймата за начало и спиране, които се използват във формат за съхранение на клеймо за време. Вместо това използвайте клеймото за време и продължителност на блоковете.
- Можете да използвате всичко с прозрачен слой, включително видео.

## Често срещани формати на субтитри

Ето някои кратки бележки относно по-често срещаните формати на субтитри, съхранявани в Matroska:

### Изображения Субтитри
Форматът на субтитрите VobSub е първият формат на субтитрите на изображения, който се импортира в Matroska. Този формат се генерира чрез експортиране на субтитрите от DVD. Пистите трябва да бъдат разделени, докато се съхраняват в Matroska, ако VobSub се състои от набор от множество потоци.

### SRT субтитри
SRT е най-простият и основен от всички формати на субтитри. Състои се от четири части, както е дадено по-долу:
 



1. Число, което показва последователността на субтитрите.
2. Времето за появяване и изчезване на субтитрите на екрана.
3. Самите субтитри.
4. Празен ред за обозначаване на началото на следващия субтитър.
 



### SSA/ASS Субтитри
Sub Station Alpha (SSA) е файлов формат, използван от популярния редактор на субтитри SubStation Alpha. Субтитрите SSA се използват широко от феновете. Има способността да показва модерни функции, напр. караоке, позициониране, стил и др.
 



### WebVTT субтитри
Консорциумът на световната мрежа (W3C) разработи WebVTT, който е съкратен като „Формат за уеб видео текстови записи“. Този формат се използва за маркиране на външни текстови ресурси за проследяване във връзка с HTML елемента.

### HDMV презентационни графични субтитри
Форматът на HDMV презентационни графични субтитри (HDMV PGS) е поредица от растерни изображения и изобщо не можем да го кажем като текст. С други думи, можете да кажете, че това е просто времева поредица от графични изображения. За да извлечете информацията, конвертирането на PGS в SRT е необходим процес.

### HDMV текстови субтитри
HDMV текстът е известен като формат на текстови субтитри, използван на Blu-ray. Matroska позволява само UTF-8 набор от знаци, когато съхранява TextST субтитрите.

### Субтитри за цифрово видео излъчване (DVB).
Форматът на субтитрите DVB е въведен за регулиране на предаването и показването на субтитри на няколко езика на телевизионни сигнали. Типичният формат на субтитри също би позволил на всеки зрител да гледа DVB субтитрирани предавания, без значение кой е производителят на предавателните системи.


## Препратки ##

- [Субтитри на Matroska](https://www.matroska.org/technical/subtitles.html)

