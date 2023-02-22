{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "розширення", "файл", "формат файлу", "Тип файлу бази даних", "Формат файлу бази даних", "Файли бази даних" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу SQL та API, які можуть створювати та відкривати файли SQL.",
  "title" :"Формат файлу SQL - файл даних структурованої мови запитів",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Що таке файл SQL?

Файл із розширенням .sql — це файл мови структурованих запитів (SQL), який містить код для роботи з реляційними базами даних. Він використовується для написання операторів SQL для операцій CRUD (створення, читання, оновлення та видалення) у базах даних. Файли SQL поширені під час роботи з настільними комп’ютерами, а також з веб-базами даних. Існує декілька альтернатив SQL, наприклад Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL та деякі інші. Файли SQL можна відкривати за допомогою редакторів запитів Microsoft SQL Server, MySQL та інших текстових редакторів, таких як Блокнот в ОС Windows.

## Коротка історія

* Розроблено та представлено Доналом Д. Чемберліном і Реймондом Ф. Бойсом у IBM на початку 1970-х років
* Використовується для зберігання та отримання даних з оригінальної квазіреляційної системи керування базами даних IBM System R
* Почали використовуватися в комерційній базі продуктів на основі свого прототипу System R, включаючи System/38, SQL/DS і DB2, які були комерційно доступні в 1979, 1981 і 1983 роках відповідно.
* Офіційно прийнятий групами стандартів ANSI та ISO як стандарт «Мова бази даних SQL» для систем керування реляційними базами даних (RDBMS) до 1986 року

## Формат файлу SQL

Файли SQL мають звичайний текстовий формат і можуть складатися з кількох мовних елементів. До одного файлу SQL можна додати декілька операторів, якщо їхнє виконання можливе без залежності один від одного. Ці команди SQL можуть виконуватися редакторами запитів для виконання операцій CRUD.

### Елементи мови SQL

Елементи мови SQL перераховані нижче.

|Елемент|Опис|
---|---|
|Положення| Складові компоненти операторів і запитів.|
|Вирази| Може створювати або скалярні значення, або таблиці, що складаються зі стовпців і рядків даних|
|Предикати| Укажіть умови, які можуть бути оцінені як тризначна логіка SQL (3VL) (істина/хибність/невідомо) або логічні значення істинності та використовуються для обмеження ефектів операторів і запитів або для зміни потоку програми.|
|Запити| Отримати дані на основі конкретних критеріїв. Це важливий елемент SQL.|
|Заяви| Може мати постійний вплив на схеми та дані або може контролювати транзакції, потік програми, підключення, сеанси чи діагностику.|

### Приклад SQL
Наступний оператор SQL створює таблицю з іменем **DATA**, а потім додаткові команди `INSERT` для вставлення записів у цю таблицю.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Посилання ##

* [SQL від Wikipedia](https://en.wikipedia.org/wiki/SQL)
* [Синтаксис SQL](https://en.wikipedia.org/wiki/SQL_syntax)
