{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Дізнайтеся про формат файлу DSN та API, які можуть створювати та відкривати файли DSN.",
  "title" : "Формат файлу DSN – файл вихідного імені бази даних",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-uk",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Що таке файл DSN?

DSN означає «Ім’я джерела даних», і це формат файлу, який використовується для зберігання інформації про з’єднання з базою даних. Файли DSN зазвичай використовуються в поєднанні з ODBC (Open Database Connectivity) і дозволяють легко отримати доступ до певної бази даних, надаючи необхідну інформацію для підключення до неї, таку як ім’я сервера, ім’я користувача та пароль. Зазвичай файл має звичайний текст і його можна створювати та редагувати за допомогою текстового редактора. Його можна використовувати в різних операційних системах, таких як Windows, Linux і Mac.

## Як створити файл DSN?

Спосіб створення файлу DSN може відрізнятися залежно від операційної системи та доступних інструментів. Наступні кроки надають загальний огляд процесу створення файлу DSN у системі Windows.

1. Відкрийте адміністратор джерел даних ODBC, ввівши в меню «Пуск» пошук «Джерела даних ODBC».
2. Виберіть вкладку «System DSN» і натисніть кнопку «Add».
3. Виберіть відповідний драйвер для бази даних, до якої ви хочете підключитися, і натисніть «Готово».
4. Заповніть необхідну інформацію для підключення до бази даних, таку як ім’я сервера, ім’я користувача та пароль.
5. Натисніть «OK», щоб зберегти файл DSN.

Крім того, ви можете створити файл DSN вручну, створивши звичайний текстовий файл із розширенням .dsn і ввівши необхідну інформацію про підключення у форматі:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Потім ви можете використовувати шлях до цього файлу як DSN у своєму коді/сценарії для підключення до бази даних.

## Програми, які відкривають файл DSN

Файл DSN — це простий текстовий файл, у якому зберігається інформація, яка використовується для підключення до бази даних, наприклад ім’я сервера, ім’я користувача та пароль. Зазвичай він використовується в поєднанні з ODBC (Open Database Connectivity), щоб забезпечити легкий доступ до конкретної бази даних.

Щоб відкрити та переглянути вміст файлу DSN, ви можете скористатися будь-яким текстовим редактором, таким як Notepad, Sublime Text, Atom тощо. Ці програми дозволять вам відкрити файл DSN і переглянути інформацію про підключення, що зберігається в ньому.

Однак для використання файлу DSN для підключення до бази даних і виконання таких операцій, як SELECT, INSERT, UPDATE, DELETE тощо, потрібна програма з підтримкою ODBC, наприклад мова програмування, як-от Python, Java, C#, або інструмент керування базами даних, як-от Microsoft Access , потрібна програма SQL Server Management Studio. Ці програми можуть використовувати інформацію у файлі DSN для підключення до бази даних і виконання потрібної операції.

## Список літератури

* [Що таке DSN (назва джерела даних)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



