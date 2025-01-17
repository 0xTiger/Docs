{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за файловия формат NMONEY и API, които могат да създават и отварят NMONEY файлове.",
  "title" :"Файл NMONEY – файлов формат на акаунт в Denaro",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Какво е NMONEY файл?

Файлът NMONEY е файл с база данни за съхранение на финансови данни, който съдържа запис на финансови транзакции. Той е разработен от Nickvision и е използван в софтуера Nickvision Denaro, който е лично финансово софтуерно приложение. Данните, съхранявани във файл NOMONEY, включват информация за кредитни и дебитни транзакции към сметка.

Файловете NOMONEY могат да се отварят с приложението [Github](https://github.com/NickvisionApps/Denaro).

## Относно Denaro Software

Denaro първоначално е разработен от [Nickvision](https://nickvision.org/) като продукт, който по-късно е преобразуван в софтуерно приложение с отворен код, хоствано на [Github](https://github.com/NickvisionApps/Denaro) . Оттогава приложението е модифицирано и актуализирано само в Github. Приложението е разработено на C# в потребителски интерфейс на Windows с SDK за приложения на Windows (WinUI 3 към този момент).

### Функции, предлагани от Denaro

* Управлявайте множество акаунти едновременно с най-популярния и познат интерфейс на раздела
* Филтрирайте транзакциите по тип, група или дата
* Повторете транзакции като сметки, които се случват всеки месец
* Прехвърляне на пари от една сметка в друга
* Експортирайте данните от акаунт като CSV файл и импортирайте CSV, OFX или QIF файл, за да добавите транзакции към акаунт

## Файлов формат Denaro - повече информация

Файловете Denaro се записват на диск в двоичен файлов формат. Финансовите данни се съхраняват като файл на база данни във файлов формат **.SQLITE3**. SQLITE е лек SQL файл с база данни, създаден със софтуера SQLite. Той осигурява самостоятелна база данни, която е в състояние да предостави напълно функционална и изключително надеждна база данни. Файловете с бази данни SQLite могат да се използват за споделяне на богато съдържание между системите чрез просто обмен на тези файлове по мрежата. SQLite свързвания съществуват за езици за програмиране като C, [C#](/bg/programming/cs/), [C++](/bg/programming/cpp/), [Java](/bg/programming/java/), [PHP](/bg/programming/php/), и много други.

## Препратки

* [Nickvision](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

