{
  "date" : "2022-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за файловия формат TRM и API, които могат да създават и отварят TRM файлове.",
  "title" :"TRM файлов формат - Oracle Trace Map File",
  "linktitle" : "TRM",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## Какво представлява файлът Oracle TRM?

TRM файлът е файлов формат с метаданни, използван от Oracle 11g система за управление на релационни бази данни (RDBMS). Той се съхранява заедно с файловете за проследяване на Oracle ([.trc](/bg/database/trc/)) и съдържа структурна информация за файла за проследяване. Целта на TRM файла е да улесни търсенето и навигацията в записите, използвайки информацията за метаданни. Софтуерът Oracle може да се използва за отваряне на TRM файлове.

## TRM файлов формат

TRM файловете се записват в собствения файлов формат на Oracle и подробностите за файловия формат TRM не са публично достъпни. Типичният TRC файл съдържа SID на процеса на Oracle, името на процеса и номера на процеса на OS. TRM файловете съдържат подробна информация за метаданни за тези TRC файлове за търсене и навигация.

## Препратки ##

* [Какво е .trm файл в oracle 11g?](https://community.oracle.com/tech/developers/discussion/945615/what-is-trm-file-in-oracle-11g)
