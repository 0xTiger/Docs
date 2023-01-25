{
  "date" : "2019-12-10",
  "keywords" :[ "XLTX", "файл", "разширение", "файлов формат", "Excel Open XML", "Електронна таблица" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Вашето ръководство за файлов формат, за да знаете какво е XLTX файл и API, които могат да ги създават и отварят.",
  "title" :"Какво е XLTX файл?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Какво е XLTX файл?

Файловете с разширение .xltx представляват шаблонни файлове на Microsoft Excel, които са базирани на спецификациите на файловия формат на Office OpenXML. Използва се за създаване на стандартен шаблонен файл, който може да се използва за генериране на [XLSX](/bg/spreadsheet/xlsx/) файлове, които показват същите настройки като посочените в XLTX файла.

## Кратка история

Беше в началото на 2000 г., когато Microsoft реши да направи промяната, за да приспособи стандарта за **Office Open XML**. Документи от различни видове съгласно този нов стандарт бяха идентифицирани чрез добавяне на „X“ в техните разширения, където „X“ е за XML. До 2007 г. този нов файлов формат стана част от Office 2007 и се поддържа и в новите версии на Microsoft Office. Новият файлов тип има добавени предимства на малки размери на файлове, по-малко промени на корупция и добре форматирано представяне на изображения.

## Спецификации на XLTX файлов формат

XLTX файловете са базирани на файловия формат Office OpenXML и използват XML и [ZIP](/bg/compression/zip/), за да намалят размера на файла. Създаден е с пускането на Microsoft Office 2007, за да замени двоичния файлов формат XLT. Подобно на XLTX, файловият формат XLT може да се използва за създаване на [XLS](/bg/spreadsheet/xls/) файлове с помощта на Microsoft Excel 2003 и 2007. Те могат да бъдат отворени с Microsoft Excel чрез двукратно щракване върху файла. Организацията на файловете във файлов формат XLTX може да се наблюдава чрез преименуване на файла в ZIP и след това извличане на съдържанието му на диск.

### [Content_Types].xml ###

Това е единственият файл, който се намира на базово ниво при извличане на zip. Той изброява типовете съдържание за частите в пакета. Всички препратки към XML файловете, включени в пакета, са посочени в този XML файл.

### \_rels (папка) ###

Това е папката Relationships, която съдържа един XML файл, който съхранява връзките на ниво пакет. Връзките към ключовите части на Xltx файловете се съдържат в този файл като URI. Тези URI идентифицират типа връзка на всяка ключова част с пакета. Това включва връзката с основния офис документ, разположен като xl/workbook.xml и други части в рамките на docProps като основни и разширени свойства.

### docProps ###

Тази папка съдържа общите свойства на документа. Те включват набор от основни свойства, набор от разширени или специфични за приложението свойства и миниатюрен преглед на документа. Празна работна книга има два файла в тази папка, а именно app.xml и core.xml. core.xml съдържа информация като автор, дата на създаване и записване и промяна. App.xml съдържа информация за съдържанието на файла.

### xl (Папка) ###

Това е основната папка, която съдържа всички подробности за съдържанието на работната книга. По подразбиране има следните папки:

* \_rels
* тема
* работни листове

и следните xml файлове:

* styles.xml
* работна книга.xml

## Препратки ##

* [[MS-XLSX] - .Xlsx файлов формат](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)
