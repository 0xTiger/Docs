{
  "date" : "2021-07-08",
  "keywords" :["HAR", "Файл", "Розширення", "Формат файлу", "Розширення файлу", "JSON", "Архівний файл"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - формат архівного файлу HTTP",
  "description" :"Посібник із формату вашого файлу, щоб дізнатися, що таке файл HAR та API, які можуть створювати та відкривати файл HAR.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## Що таке файл HAR?

Файл із розширенням .har (архів [HTTP](/uk/web/http/)) — це архівний файл HTTP, у якому зберігаються дані сеансу, що передаються через багато браузерів (таких як Chrome, Safari, IE, Firefox тощо) у [JSON] (/uk/web/json/) формат файлу. Дані, що передаються через Інтернет між сервером і клієнтом (у даному випадку браузером користувача), містять заголовки HTTP-запиту та відповіді, які зберігаються у файлі HAR. Крім того, він містить детальну інформацію про продуктивність веб-сторінок, завантажених у браузері. Файли HAR можна відкрити в будь-якому текстовому редакторі, наприклад у Блокноті в ОС Microsoft Windows і TextEdit в Apple MacOS.

## Формат файлу HAR - Додаткова інформація

Файли HAR зберігають інформацію про сеанс у звичайному текстовому файлі з використанням популярного формату JSON. Специфікації для формату файлу HAR були створені групою Web Performance Group Консорціуму World Web (W3C), але їх не вдалося опублікувати. Однак він успішно визначив формат архіву для транзакцій HTTP.

На додаток до моніторингу передачі інформації про запити та відповіді, файли HAR використовуються розробниками для реєстрації продуктивності веб-браузера з точки зору швидкості завантаження сторінки, тривалості завантаження вмісту, завантаженого вмісту, запитів, виконаних для отримання відповіді від браузера, і багатьох інших .

## Навіщо використовувати файли HAR?

Файли HAR можуть бути корисними для покращення продуктивності веб-сайту шляхом оцінки тривалого часу завантаження, часу візуалізації сторінки та часу відповіді. Файли HAR можна проаналізувати, щоб виявити такі проблеми та вирішити будь-які проблеми з веб-сайтом для покращення продуктивності.

## Як створити файл HAR?

Отже, як створити файл HAR? Що ж, це залежить від типу браузера, який ви використовуєте для створення файлу HAR. У цьому посібнику ми перелічуємо кроки для браузера Google Chrome. Методи створення файлів HAR за допомогою Safari, Firefox тощо можна легко знайти в Інтернеті та слідувати їм.

### Кроки для створення файлу HAR за допомогою Google Chrome

Наступні кроки можна виконати на веб-сторінці, де виникають проблеми.

1. Відкрийте веб-сторінку в Google Chrome, де виникла проблема.
1. Відкрийте інструмент розробника (перегляньте елемент).
1. Перейдіть ліворуч від панелі, щоб почати запис файлу. У цьому розділі є маленька кругла червона кнопка.
1. Натисніть «Піктограму очищення», щоб видалити будь-які записи журналу, які зберігаються в браузері.
1. Щоб зберегти потрібний вміст, як показано вище, клацніть правою кнопкою миші та виберіть «Зберегти як файл HAR».

## Список літератури

* [Формат файлу HAR - Вікіпедія](https://en.wikipedia.org/wiki/HAR_(формат_файлу))
