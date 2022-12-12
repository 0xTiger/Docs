{
  "date" : "2019-10-11",
  "keywords" :[ "файл odt", "формат файлу odt", "що таке файл odt", "файл", "приклад odt", "розширення файлу odt", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODT - текстовий файл OpenDocument",
  "description":"Дізнайтеся про формат файлу ODT та API, які можуть створювати та відкривати файли ODT.",
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл ODT?

Файли ODT – це тип документів, створених за допомогою програм для обробки текстів, які базуються на форматі текстового файлу OpenDocument. Вони створюються за допомогою програм текстового процесора, таких як безкоштовний OpenOffice Writer, і можуть зберігати такий вміст, як текст, зображення, об’єкти та стилі. Файл ODT для текстового процесора Writer є таким же, як [DOCX](/uk/word-processing/docx/) для Microsoft Word. Кілька програм, зокрема Google Docs і текстовий веб-процесор Google, що входить до складу Google Drive, можуть відкривати файли ODT для редагування. Microsoft Word також може відкривати файли ODT і зберігати їх в інших форматах, наприклад [DOC](/uk/word-processing/doc/) і DOCX.

## Коротка історія ##

Специфікації формату файлів ODP базуються на стандарті, розробленому як специфікації ODF. Ці специфікації еволюціонували в минулому у вигляді трьох версій, розроблених і опублікованих OASIS, як показано нижче:

**2005** Версія 1.0 була опублікована в травні 2005 року

**2007:** Версія 1.1 була опублікована в лютому 2007 року

**2011:** Версія 1.2 була опублікована у вересні 2011 року

Під час переходу від версії ODF 1.0 до версії 1.1 відбулися досить незначні зміни. [Версія ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) є останньою версією специфікацій ODF, і розробники повинні звертатися до неї для розробки програм, пов’язаних із читанням/записом ODS.

## Характеристики формату файлу ##

Формат OpenDocument підтримує представлення документа як єдиного XML-документа, а також колекції кількох піддокументів у пакеті як [ZIP](/uk/Compression/ZIP/) архіву. Кожен із файлів ZIP-архіву зберігає частину повного документа. Кожен піддокумент зберігає певний аспект документа. Наприклад, один піддокумент містить інформацію про стиль, а інший піддокумент містить вміст документа. Типовий документ ODF містить такі компоненти:

* content.xml – вміст документа та автоматичні стилі, що використовуються у вмісті.
* styles.xml – стилі, що використовуються у вмісті документа, і автоматичні стилі, що використовуються в самих стилях.
* meta.xml – метаінформація документа, наприклад автор або час останнього збереження.
* settings.xml – параметри програми, такі як розмір вікна або інформація про принтер.

Крім них, у пакеті може бути багато інших піддокументів, як-от мініатюра документа, зображення тощо. Файли документів — це підмножина файлів ODF, у яких вміст (аркуші) зберігається у //content.xml// піддокументі.

## Посилання ##

* [OpenDocument – Вікіпедія](https://en.wikipedia.org/wiki/OpenDocument)
