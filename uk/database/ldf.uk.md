{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "розширення", "файл", "формат файлу", "Тип файлу бази даних", "Формат файлу бази даних", "Файли бази даних" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу LDF та API, які можуть створювати та відкривати файли LDF.",
  "title" :"LDF - формат файлу головної бази даних SQL Server",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Що таке файл LDF?

Файл із розширенням .ldf — це файл журналу, який підтримується Microsoft SQL Server, який є системою керування реляційною базою даних (RDBMS). Усі транзакції, які виконуються з основними файлами бази даних ([MDF](/uk/database/mdf/)) (такі як вставка, оновлення, видалення), записуються у файл LDF. Файли LDF є критично важливими компонентами будь-якої бази даних. У разі системного збою файл журналу використовується для відновлення узгодженого стану бази даних. Файл журналу транзакцій може збільшуватися в розмірі, якщо транзакції не виконано повністю. Файли LDF можна відкрити за допомогою програми Microsoft SQL Server.

## Операції, записані у файлі LDF

Файл журналу SQL записує такі операції:

* Початок і кінець кожної операції.

* Кожна зміна даних даних (вставлення, оновлення або видалення). Це також включає зміни системними збереженими процедурами або операторами мови визначення даних (DDL) до будь-якої таблиці, включаючи системні таблиці.

* Кожне виділення або звільнення екстентів і сторінок.

* Створення або видалення таблиці чи індексу.

## Формат файлу LDF

Файл LDF складається із записів транзакцій SQL Server, які впорядковані як рядок записів журналу. Кожен запис журналу має порядковий номер журналу (LSN), вищий за LSN попереднього запису. Рядки об’єднані один за одним у файлі. Завдяки сучасним високошвидкісним комп’ютерам записи можна вставляти там, де LSN2 існує у файлі журналу перед LSN1. Оскільки операції записуються в послідовний номер, зміна, описана LSN2, була виконана після запису журналу LSN1. Записи для певної транзакції зв’язуються назад за допомогою покажчиків, які використовуються та прискорюють відкат транзакції.
 

## Список літератури

* [Файли бази даних і файлові групи](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Посібник з архітектури та керування журналом транзакцій](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server-ver15)

