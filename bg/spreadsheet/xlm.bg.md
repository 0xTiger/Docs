{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "файл", "разширение", "файлов формат", "Макро файл на Microsoft Excel", "Електронна таблица"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Вашето ръководство за файлов формат, за да знаете какво е XLM Macros файл и API, които могат да създават и отварят XLM файлове.",
  "title" :"Какво е XLM файл?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Какво е XLM файл?

XLM, за Excel Macro, е вид файлове с електронни таблици, които се използват за съхраняване на макроси. От гледна точка на приложението макросът е набор от инструкции, които се използват за автоматизиране на процеси. Макросът се използва за записване на стъпките, които се изпълняват многократно за [XLS](/bg/spreadsheet/xls/) файлов формат и улеснява извършването на действията чрез повторно изпълнение на макроса. Макросите се програмират с Microsoft Visual Basic for Applications (VBA) от работната книга на Excel с помощта на редактора на Visual Basic и могат да се изпълняват/отстраняват директно от там.

## Кратка история ##

Microsoft Excel поддържа програмиране на макроси от първото си публично пускане. Функциите на макросите останаха същите през следващите версии на Excel с разширение според новите функции. XLM беше езикът за макроси по подразбиране за Excel до Excel 4.0. Excel 5.0 записва макроси във VBA по подразбиране, но с версия 5.0 XLM записът все още е разрешен като опция. След версия 5.0 тази опция беше прекратена. Всички версии на Excel, включително Excel 2010, могат да изпълняват XLM макрос, въпреки че Microsoft не препоръчва използването им.

## Записване на макрос в XLM ##

Excel предоставя лесни за използване стъпки за запис на макрос. Изисква да имате инсталирани инструменти за разработчици, за да работите с макроси. След като макро записът е в процес, той записва всяко действие на потребителя, за да бъде възпроизведено по-късно. Макрозаписът всъщност включва всички стъпки, които потребителят изпълнява след началото на записа. По този начин, ако направите съдържанието на клетка удебелено, курсив и зададете нейното подравняване на текста след стартиране на запис на макрос, всички тези команди ще бъдат записани. На всеки записан макрос може да бъде присвоен пряк път за бързо възпроизвеждане по-късно. Записването на макроси генерира VBA код под формата на макрос, който може да се редактира с помощта на редактора на Visual Basic (VBE).

## Обектен модел на Excel ##

Макросите използват VBA съчетания отзад и следват [обектния модел на Excel](https://docs.microsoft.com/en-us/office/vba/api/overview/excel/object-model) за тази цел. Този модел идентифицира обектите на електронна таблица за взаимодействие с електронната таблица чрез дефинирани от потребителя командни ленти с инструменти, командни ленти или кутии за съобщения. Например достъпът до свойствата на работната книга се предоставя с обекта Workbook. По същия начин в модела има обект Worksheet за програмна работа с работните листове на работната книга.

## Макроси и сигурност ##

VBA позволява достъп до всички области на приложение, както и до файловата система и също може да бъде опасно. Това поражда опасения при споделяне на работна книга с някой, който може да стартира файла от своя страна. Тоест Microsoft Excel предупреждава за отваряне на такъв файл. Макросите могат да бъдат сертифицирани с цифров подпис, за да могат другите потребители да проверят дали те са надеждни. По този начин макросите могат да бъдат активирани след проверка на техния източник.

## Препратки ##

* [[MS-XLS] - структура на двоичен файлов формат на Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Програмиране на макроси](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)
