{
"дата": "12.06.2023",
  "keywords": [
"бак",
"bak файл",
"Резервне копіювання бази даних Microsoft SQL Server",
"що таке файл bak",
"як відкрити файл bak",
"файл",
"розширення файлу bak",
"розширення"
],
  "author": {
"display_name": "Шейкіл Фаїз"
},
"draft": "false",
"toc": true,
"title": "Формат файлу BAK - резервна копія бази даних Microsoft SQL Server",
  "description":"Дізнайтеся про формат резервного копіювання BAK SQL Server та API, які можуть створювати та відкривати файли BAK.",
  "linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
      "parent": "database"
}
},
"lastmod": "2023-06-12"
}

## Що таке файл BAK?

Файл ".bak" у контексті Microsoft SQL Server — це формат файлу резервної копії, який використовується для зберігання копій бази даних SQL Server. Ці файли містять знімок бази даних на певний момент часу, включаючи її схему, дані та іншу пов’язану інформацію. Вони створюються за допомогою вбудованої функції резервного копіювання та відновлення SQL Server і служать для кількох важливих цілей:

1. **Відновлення даних:** файли .bak надають засоби для відновлення бази даних у разі втрати даних, пошкодження чи інших проблем. Відновлюючи базу даних із файлу .bak, ви можете повернути її до попереднього стану, мінімізуючи час простою та втрату даних.

2. **Міграція та клонування:** Файли резервних копій часто використовуються для міграції баз даних між серверами або створення копій баз даних для цілей тестування, розробки чи звітування. Вони пропонують послідовний і ефективний спосіб переміщення баз даних між середовищами.

3. **Відновлення на певний момент часу:** SQL Server дозволяє виконувати відновлення на певний момент часу за допомогою файлів .bak. Це означає, що ви можете відновити базу даних до певного моменту часу, що може мати вирішальне значення для відповідності нормативним вимогам або аудиту даних.

4. **Аварійне відновлення:** файли .bak є важливою частиною планування аварійного відновлення. Вони гарантують безпеку ваших даних і можливість їх швидкого відновлення у разі збоїв апаратного забезпечення, стихійних лих чи інших катастрофічних подій.

## Створіть файл .BAK у SQL Server

Щоб створити файл .bak у SQL Server, ви зазвичай використовуєте команди SQL Server Management Studio (SSMS) або Transact-SQL (T-SQL), наприклад BACK DATABASE або BACKUP LOG. Ось спрощений приклад того, як можна створити резервну копію бази даних за допомогою T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Відновіть файл .BAK у SQL Server

Щоб відновити базу даних із файлу .bak, можна скористатися командою RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Як відкрити файл BAK у SQL Server?

Щоб відкрити та отримати доступ до даних, що зберігаються у файлі ".bak", зазвичай потрібно відновити його на примірнику Microsoft SQL Server. Ось загальні кроки для відкриття файлу ".bak" за допомогою SQL Server Management Studio (SSMS):

1. **Запустіть SQL Server Management Studio**: відкрийте SSMS на своєму комп’ютері. Зазвичай його можна знайти в меню "Пуск" або за запитом "SQL Server Management Studio".

2. **Підключіться до екземпляра SQL Server**: у SSMS підключіться до екземпляра SQL Server, де потрібно відновити базу даних. Для виконання цієї операції вам знадобляться необхідні дозволи.

3. **Відновити базу даних**:

a. На панелі Object Explorer ліворуч розгорніть екземпляр SQL Server.

b. Розгорніть вузол "Бази даних".

в. Клацніть правою кнопкою миші "Бази даних" і виберіть "Відновити базу даних".

4. **Укажіть джерело та місце призначення**:

a. На сторінці "Загальні" діалогового вікна "Відновити базу даних" введіть назву нової бази даних у полі "До бази даних". Це буде назва відновленої бази даних.

b. У розділі "Джерело" виберіть "Пристрій" як тип носія для резервного копіювання.

в. Натисніть кнопку "..." поруч із полем "Пристрій", щоб знайти файл ".bak", який потрібно відновити.

d. Виберіть файл ".bak", який потрібно відкрити, і натисніть "ОК".

5. **Параметри відновлення**: перегляньте та налаштуйте параметри відновлення за потреби. Ви можете вказати, чи перезаписувати існуючу базу даних, встановити параметри відновлення тощо. Обов’язково встановіть ці параметри відповідно до ваших вимог.

6. **Почніть відновлення**: після налаштування параметрів відновлення натисніть кнопку "OK" у діалоговому вікні "Відновити базу даних". SQL Server почне процес відновлення.

7. **Доступ до відновленої бази даних**: після успішного відновлення ви можете отримати доступ до відновленої бази даних у SQL Server Management Studio, як і до будь-якої іншої бази даних. Ви можете виконувати запити, переглядати таблиці та працювати з даними в базі даних.

## Інші файли BAK

Ось інші типи файлів, які використовують розширення файлу **.bak**.

**База даних**
- [BAK - файл резервної копії бази даних](/uk/database/bak/)
- [BAK - Swiftpage Act! Резервне копіювання бази даних](/uk/database/bak-act/)

**Гра**
- [BAK - Terraria World або резервна копія гравця](/uk/game/bak-terraria/)

**Різне**
- [BAK - Файл резервної копії](/uk/misc/bak-backup/)
- [BAK - Резервне копіювання закладок Chromium](/uk/misc/bak-chromium/)
- [BAK - резервна копія результатів фіналу 2012](/uk/misc/bak-finale/)
- [BAK - Резервне копіювання MobileTrans](/uk/misc/bak-mobiletrans/)
- [BAK - Резервне копіювання відеопроекту VEGAS](/uk/misc/bak-vegas/)

**Налаштування**
- [BAK - Резервне копіювання Holo Launcher](/uk/settings/bak-holo/)

## Список літератури
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)