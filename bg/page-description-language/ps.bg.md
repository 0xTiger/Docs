{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PS файлов формат",
  "description":"Научете за файловия формат PS и API, които могат да създават и отварят PS файлове.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е .PS файл? ##

PostScript (PS) е език за описание на страници с общо предназначение, използван в бизнеса с настолни и електронни публикации. Основният фокус на PostScript (PS) е да улесни двуизмерния графичен дизайн. Повечето езици изискват отделен етап на компилация преди изпълнението на кода, докато форматът Post Script (PS) поддържа пряка интерпретация по време на изпълнение. Неговата ранна версия дефинира графичните форми, различни изяви на текст и моделирани изображения върху отпечатани страници или показани страници, следвайки правилата на модела за изображения на Adobe. Програма на PS е в състояние да комуникира описание на документ между композиция и система за печат, като поддържа устройството независимо и на високо ниво. Освен това тази програма може също така да управлява външния вид на текст и графики на дисплея.

Описанието на PostScript страница е достъпно за изобразяване, показване на принтер и друго изходно устройство с помощта на PostScript интерпретатора на устройството. Тъй като командите за отпечатване на знаци, графични форми и изображения се изпълняват от интерпретатор, за това конкретно устройство описанието на PostScript от високо ниво се преобразува във формат на растерни данни от ниско ниво. Като цяло различни приложения като илюстратори, системи за композиране на документи и автоматизиран дизайн (CAD) са автоматизирани за генериране на описания на PostScript страници. Обикновено програмистите трябва да пишат PostScript програми по време на създаването на нови приложения. Програмистът обаче може да се възползва от възможностите на езика PostScript, които не са достъпни в нито едно приложение, като напише PS програма за тази специална ситуация.

## Кратка история ##

Концепцията за езика PostScript е въведена за първи път от Джон Уорнок. През 1966 г. той работи върху проект на пристанището на Ню Йорк. Той се опитваше да разработи интерпретатор за голяма триизмерна графика за базата данни на този проект. За обработката на тези графики Джон Уорнок създаде езика Design System. Междувременно Xerox PARC търсеше стандартно средство за дефиниране на изображения на страници за своя първи лазерен принтер. Въпреки че Боб Спроул и Уилям Нюман през 1975-76 г. разработиха формата Press (формат на данни), за да управляват лазерни принтери, все пак беше необходим език за повече гъвкавост. През 1978 г. Уорнок се присъединява към Мартин Нюел в Xerox PARC и пренаписва интерпретативния език JaM, който по-късно се разраства и разширява в езика Interpress. Уорнок основава Adobe Systems през декември 1982 г. с Чък Гешке, Дъг Броц, Ед Тафт и Бил Пакстън. Те започнаха да работят върху по-опростен език, наречен PostScript, подобен на Interpress, пуснат на пазара през 1984 г. Стив Джобс от Apple ги посети и ги посъветва да адаптират PostScript за управление на лазерни принтери.

През март 1985 г. първият принтер с вграден PostScript интерпретатор беше LaserWriter на Apple, който революционизира настолното публикуване (DTP). Техническата надеждност и широко разпространената достъпност направиха PostScript предпочитан език за настолни и електронни публикации. През 1990 г. интерпретаторът за езика PostScript беше съществена част от лазерните принтери.

## Основните функции ##

Възможностите на езика PostScript за работа с интерактивни графики и описание на страници притежават следните характеристики:

**Форми:** Произволни по своята същност, могат да се състоят от прави линии, криви, квадрати и кубични криви, които могат да бъдат както самостоятелно преминаващи, така и несвързани (в секции и дупки).

**Оператори за рисуване:** позволяват очертанията на формата с всякаква дебелина, цвят, запълване или позволяват формата да бъде начертана като изрезка, за да позволи изрязването на всяка друга графика.

**Цветовете:** имат разнообразие като нива на сивото, RGB, CMYK и CIE. Специални видове цветове се моделират като различни характеристики: спот цветове, цветово картографиране, равномерно засенчване и повтарящи се шарки.

**Текст:** напълно интегриран с графики. Освен това моделът за изображения на Adobe позволява текстовите знаци да се показват като графични форми, които могат да се управляват от всеки нормален графичен оператор.

**Извадкови изображения**: извлечени от оригинални източници (сканирани снимки) или могат да бъдат произведени синтетично. Езикът PostScript предлага разнообразни средства за регенериране на изображения с всякаква резолюция и според различни цветови модели на изходно устройство.

Езикът за програмиране с общо предназначение може да се възползва от графичните възможности на езика PostScript, като вгради Ps в своята рамка. Примитивните типове данни, като числа, знаци, масиви и низове; контролни примитиви, като цикли, процедури и условия; и някои нетрадиционни функции, като например речници, са посочени в езика. Тези функции улесняват програмистите да пишат команди за извикване на операции от по-високо ниво. Тези операции на високо ниво отговарят на нуждите на комплексното приложение. Такава практика е по-компактна и ефективна, вместо да използва фиксиран набор от основни операции.

Програми, написани на PostScript, могат да бъдат произведени, комуникирани и интерпретирани под формата на ASCII изходен текст. Целият език може да бъде дефиниран под формата на печатни знаци и бяло пространство. Това представяне помага на програмистите да създават, манипулират и разбират лесно езика. Освен това съхранението и предаването на файлове между различни компютри и операционни системи се поддържат удобни чрез машинна независимост.

Възможни са двоично кодирани форми на езика, когато програмата е гарантирана за напълно прозрачен комуникационен път към PostScript интерпретатора. Adobe препоръчва стриктно спазване на ASCII представянето на PS програмите за обмен на документи или архивно съхранение.

## Версии ##

PS(.ps) е файловото разширение за PostScript документ. Националните архиви на Обединеното кралство категоризират пет хронологични версии на PostScript файла, дефинирани във версията DSC: версии 1.0, 2.0, 2.1, 3.0, 3.1. Всяка версия дефинира важни коментари за структуриране. Encapsulated PostScript файл (EPS) е специален подтип на PostScript файл, който използва езика за указване на правоъгълна графика. PostScript Language Reference Manual описва EPS като: „Енкапсулиран PostScript (EPS) файл е PostScript програма, описваща най-много една страница във формуляр, който може да бъде импортиран от други приложения за вграждане в съдържащ документ.“ Файл с PostScript документ може да капсулира EPS файл в него. Допълнителна употреба на PostScript се споменава като Display PostScript (DPS). DPS генерира екранна графика чрез графичен двигател, който използва PostScript модел за изображения и език.

## Препратки ##

* [Семейство формати PostScript](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)
