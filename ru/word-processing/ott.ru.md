{
  "date" : "2019-10-11",
  "keywords" :[ "файл ott", "формат файла ott", "что такое файл ott", "файл", "пример ott", "расширение файла ott", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT — файл шаблона OpenDocument",
  "description":"Узнайте о формате файла OTT и API-интерфейсах, которые могут создавать и открывать файлы OTT.",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## .OTT вариант №

Файлы с расширением OTT представляют собой шаблонные документы, созданные приложениями в соответствии со стандартным форматом OpenDocument OASIS. Они создаются с помощью приложений текстового процессора, таких как бесплатный OpenOffice Writer, и могут содержать настройки, которые можно использовать для создания новых документов из этих файлов шаблонов. Эти параметры включают поля страницы, границы, верхние и нижние колонтитулы и другие параметры страницы. Такие шаблоны используются в официальных документах, таких как бланки компаний и стандартизированные формы.

## Краткая история ##

Спецификации формата файлов ODP основаны на стандарте, разработанном как спецификации ODF. Эти спецификации развивались в прошлом в виде трех версий, разработанных и опубликованных OASIS следующим образом:

**2005 г.:** Версия 1.0 была опубликована в мае 2005 г.

**2007:** Версия 1.1 была опубликована в феврале 2007 г.

**2011:** Версия 1.2 была опубликована в сентябре 2011 г.

При переходе с версии ODF 1.0 на версию 1.1 произошли довольно незначительные изменения. [Версия ODF 1.2] (https://www.oasis-open.org/standards#opendocumentv1.2) является последней версией спецификаций ODF, и разработчики должны консультироваться с ней при разработке приложений, связанных с чтением/записью ODS.

## Спецификации формата файла

Формат OpenDocument поддерживает представление документа в виде одного XML-документа, а также набора нескольких вложенных документов внутри пакета в виде архива [ZIP](/ru/Compression/ZIP/). В каждом из файлов ZIP-архива хранится часть полного документа. Каждый вложенный документ хранит определенный аспект документа. Например, один вложенный документ содержит информацию о стиле, а другой вложенный документ содержит содержимое документа. Типичный документ ODF состоит из следующих компонентов:

* content.xml — содержимое документа и автоматические стили, используемые в нем.
* styles.xml — стили, используемые в содержимом документа, и автоматические стили, используемые в самих стилях.
* meta.xml — метаданные документа, такие как автор или время последнего действия сохранения.
* settings.xml — настройки приложения, такие как размер окна или информация о принтере.

Помимо этого, в пакете может быть много других вложенных документов, таких как миниатюры документов, изображения и т. д. Файлы документов — это подмножество файлов ODF, где содержимое (листы) хранится в //content.xml// вложенном документе.

## Использованная литература ##

* [OpenDocument — Википедия] (https://en.wikipedia.org/wiki/OpenDocument)
