{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла PDF/A",
  "description":"Узнайте о формате файлов PDF/A и API-интерфейсах, с помощью которых можно создавать и открывать файлы PDF/A.",
  "linktitle" : "PDF/A",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Что такое PDF/A? #

PDF/A — это стандартный формат ISO для архивирования электронных документов в формате PDF. Его основной причиной появления было удовлетворение требований долгосрочного архивирования. Стандарт обеспечивает открытие архивных файлов даже по прошествии длительного времени, накладывая определенные ограничения на неотъемлемые части документа для достижения соответствия. В настоящее время формат широко применяется во всех отраслях. Программы просмотра PDFA/A, такие как Adobe Acrobat Reader, гарантируют, что файлы, сохраненные в этом формате, можно будет открыть даже в будущем в соответствии с информацией, предоставленной этим стандартом.

## Версии PDF/A ##

PDF/A был принят в качестве стандарта ISO в октябре 2005 года. С тех пор он постоянно совершенствуется, и с течением времени было разработано несколько дополнительных стандартов. Информация о стандартах PDF/A, опубликованных с течением времени, и их детали следующие:

* **PDF/A-1:** опубликован в октябре 2005 г. как ISO 19005-1 и основан на PDF 1.4.
* **PDF/A-2:** опубликован в июне 2011 г. как ISO 19005-2 и основан на PDF 1.7 (ISO 32000-1:2008).
* **PDF/A-3:** опубликован в октябре 2012 г. как ISO 19005-3 и основан на PDF 1.7 (ISO 32000-1:2008).

## ПДФ/А-1 ##

Стандарт PDF/A-1 был основан на исходной версии PDF 1.4. Стандарт PDF/A-1 определяет два уровня соответствия файлов PDF.

### PDF/A-1a ###

Он соответствует уровню А и удовлетворяет всем требованиям спецификаций стандарта PDF/A-1. PDF/A-1a гарантирует, что текст можно извлечь из документа. Это также гарантирует сохранение естественного процесса чтения интегрированного текстового материала. PDF/A налагает требование на возможность представления текста на уменьшенных экранах за счет реструктуризации, известной как «теговый PDF». Он был предназначен для повышения доступности соответствующих файлов для пользователей с ограниченными физическими возможностями за счет использования вспомогательного программного обеспечения.

### PDF/A-1b ###

PDF/A-1b представляет собой более низкий уровень соответствия и касается внешнего вида электронных документов по отношению к стандарту ISO 19005. Это гарантирует, что текст и другой контент на страницах воспроизводятся одинаково. Это соответствие уровня B указывает на минимальное соответствие, чтобы гарантировать, что визуализированный внешний вид соответствующего файла сохраняется в течение длительного времени.

## ПДФ/А-2 ##

PDF/A-2 был выпущен стандартом ISO в июле 2011 года в качестве нового стандарта, известного как ISO 32001-1. Этот новый стандарт не только воспользовался всеми функциями версий PDF до 1.7, но и был представлен как новый стандарт. PDF/A-2 включает следующие функции как часть этого нового стандарта.

* PDF/A-2 поставляется с поддержкой [JPEG2000](/ru/image/jp2/), что полезно в случае отсканированных документов.
* Он поддерживает встраивание коллекций PDF/A, которые можно использовать для создания PDF-контейнера с другими похожими файлами.
* Он полностью поддерживает функцию прозрачности файлов PDF по сравнению с PDF/A-1, где она поддерживалась частично.
* PDF/A-2 обеспечивает поддержку дополнительного содержимого, полезного для картографических приложений и инженерных чертежей. Они также известны как слои, которые можно сделать видимыми или скрытыми в соответствии с требованиями пользователя.
* В нем указаны требования к пользовательским метаданным XMP.
* Добавляет некоторые новые типы комментариев в список запрещенных типов аннотаций. Кроме того, в список допустимых элементов были добавлены некоторые новые типы комментариев, такие как комментарии для редактирования текста.

## PDF/A-3 ##

PDF/A-3 включает все требования соответствия уровня 2 и позволяет встраивать дополнительные форматы файлов (такие как XML, [CSV](/ru/spreadsheet/csv/), [CAD](/ru/cad/), [обработка текста](/ru/word-processing/) , [spreadsheet](/ru/spreadsheet/) и другие) в соответствующие документы PDF/A.

## Использованная литература ##

* [PDF/A — Википедия](https://en.wikipedia.org/wiki/PDF/A)
* [Белая книга: PDF/A — Основы](https://www.pdf-tools.com/public/downloads/whitepapers/whitepaper-pdfa.pdf)

