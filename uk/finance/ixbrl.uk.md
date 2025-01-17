{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl", "файл ixbrl", "формат файлу ixbrl", "тип файлу ixbrl", "файл", "тип", "що таке файл ixbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL - Формат файлу бізнес-фінансової звітності",
  "description":"Дізнайтеся про формат файлу IXBRL та API, які можуть створювати та відкривати файли IXBRL.",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Що таке файл iXBRL?

Формат файлу iXBRL (ilnine XBRL) дозволяє вставляти дані [XBRL](/uk/finance/xbrl/) у файл HTML, щоб зробити його машинним і людиночитаним. Насправді це файл [xHTML](/uk/web/xhtml/), який використовує теги XBRL і був розроблений XBRL International відповідно до вимог HMRC Великобританії. За допомогою iXBRL можна створювати фінансові звіти, зберігаючи макет оригінального документа незмінним. Файли iXBRL можна відкривати в будь-якому текстовому редакторі, наприклад Блокноті в операційній системі Windows і TextEdit в MacOS.

## Формат файлу iXBRL

Всередині iXBRL вміст XBRL загорнуто у формат файлу xHTML, який використовує теги XML. Як XBRL,<xbrl> є кореневим елементом файлів iXBRL. Формат XHTML представляє свій вміст як набір різних типів документів і модулів. Усі файли в XHTML базуються на форматі файлів XML і відповідають стандартам документів XML. XHTML — це формат, який важливо використовувати для оперативного використання залежної [HTML](/uk/web/html/) об’єктної моделі документа (DOM) або [XML](/uk/web/xml/) об’єктної моделі документа. Для зовнішнього світу iXBRL відповідає специфікаціям формату файлу [xHTML](/uk/web/xhtml/).

### iXBRL проти XBRL

XBRL можна порівняти з iXBRL на основі таких факторів:

* Складність
* Параметри форматування
* Типи/розширення файлів
* Параметр візуалізації
* Процес подання

Наступна таблиця ілюструє ці відмінності.

|Параметр|XBRL|iXBRL|
---|---|---|
|Складність|Складніший, ніж iXBRL|Менш складний через існуючу схему організації XHTML|
|Параметри форматування|Обмежена гнучкість|Висока гнучкість для форматування вмісту|
|Типи файлів/розширення|Офіційно збережено з розширенням .xml|Зазвичай зберігається як розширення .html або .xhtml|
|Параметри візуалізації|Програми перегляду XBRL, необхідні для перегляду цього|зрозумілого для людини вмісту, який можна переглядати в браузерах|
|Процес подання| Документи екземплярів XBRL (машинозчитувані) і HTML (людиночитані) потрібно подавати окремо.|Як людиночитані, так і машинозчитувані формати доступні в одному екземплярі документа|

## Список літератури

* [XBRL - Вікіпедія](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

