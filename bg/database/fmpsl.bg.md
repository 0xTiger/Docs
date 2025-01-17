{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за файловия формат FMPSL и API, които могат да създават и отварят FMPSL файлове.",
  "title" :"FMPSL файлов формат – FileMaker Pro 12 Snapshot Link File",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## Какво е FMPSL файл?

FMPSL файлът е файл с моментна снимка на база данни, създаден с FileMaker Pro 12. Той съхранява заявените резултати от базата данни заедно с друга информация, като визуално оформление и видима информация. Файлът FMPSL може да се използва за възстановяване на всички тези данни в друг екземпляр на база данни FileMaker Pro. Този файлов формат беше въведен с пускането на FileMaker Pro v. 12. Преди тази версия, връзките за моментни снимки бяха въведени като файлов формат FPSL във FileMaker Pro v. 11. FMPSL файловете могат да се отварят със софтуера FileMaker Pro Advanced. Други файлови формати, поддържани от FileMaker Pro, включват [FP5](/bg/database/fp5/), [FP7](/bg/database/fp7/) и [FMP12](/bg/database/fmp12/).

## FMPSL файлов формат

Подробностите за вътрешния файлов формат на FMPSL файловете не са публично достъпни за справка от разработчиците.

### Как да запишете записи като FMPSL файл?

Данните от базата данни на FileMaker Pro могат да бъдат запазени като файл с връзка към моментна снимка, като се използват следните стъпки.

1. Търсене в записите от базата данни, които трябва да бъдат запазени като файл с връзка към моментна снимка.
1. Като използвате опцията Изпращане на запис като връзка към моментна снимка от менюто, запазете файла, като въведете име на файл.
1. Използвайте разглежданите записи, за да запазите целия намерен набор от записи.

Генерираният файл със снимка ще бъде записан на диск с посоченото име.

## Препратки

* [Конвертиране на по-ранни версии на FileMaker Pro файлови формати във файлов формат FMP12](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Запазване на записи като файл с връзка към моментна снимка](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

