{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл HTACCESS - формат файлу Apache HTACCESS",
  "description" :"Посібник із формату вашого файлу, щоб дізнатися, що таке файл HTACCESS",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл HTACCESS?

Файл HTACCESS — це файл конфігурації Apache, який забезпечує механізм, що дозволяє змінювати конфігурацію для різних папок/каталогів веб-сайту. Він містить директиви конфігурації, які застосовуються до каталогу та підкаталогів.

Файл HTACCESS виконує ряд перевірок, таких як визначення сторінки індексу веб-сайту, перелік сторінки помилки 404 (Сторінку не знайдено), виконання переспрямувань сторінок 301 або 302, блокування доступу з певної IP-адреси або інших веб-сайтів. Таким чином, використання файлів .htaccess сповільнює загальну продуктивність вашого сервера Apache [HTTP](/uk/web/http/).

## Формат файлу HTACCESS

Файли HTACCESS зберігаються на диску у форматі простого тексту. Це означає, що ви можете відкривати та редагувати ці файли в будь-якому текстовому редакторі. Немає імені перед "." у файлі .htaccess, показуючи, що це прихований файл у папці.

## Загальне використання файлу HTACCESS

Нижче наведено п’ять типових застосувань файлу HTACCESS.

### Mod_Rewrite

Файл HTACCESS можна використовувати для призначення та зміни того, як URL-адреси та веб-сторінки на веб-сайті відображаються користувачам.

### Автентифікація

Автентифікацію можна здійснити за допомогою .htaccess, створивши файл passowrd під назвою .htpasswd. Це дозволяє відвідувачам сайту вводити пароль, якщо вони хочуть відвідати певний розділ веб-сторінки.

### Спеціальні сторінки помилок

За допомогою файлу .htaccess можна створювати спеціальні сторінки помилок, наприклад 400 Поганий запит, 401 Потрібна авторизація, 403 Заборонена сторінка, 404 Файл не знайдено та 500 Внутрішня помилка. Однак це сповільнить роботу сервера, оскільки всі ці перевірки виконуватимуться під час доступу до сторінок.

### Типи MIME

Файли Apache HTACCESS можна змінити, щоб включити типи багатоцільових розширень Інтернет-пошти (MIME). Це дозволяє вашому серверу підтримувати доставку файлів програми, які не підтримувалися сайтом.

### SSI

Server Side Includes (SSI) чудово економить час на веб-сайті. SSI можна ввімкнути, вставивши наступний код у ваш файл .htaccess.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Приклад файлу Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Список літератури

* [Посібник з HTTP-сервера Apache: файли .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)
