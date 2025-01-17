{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла PDF/UA",
  "description":"Узнайте о формате файлов PDF/UA и API, которые могут создавать и открывать файлы PDF/UA.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Что такое файл PDF/UA? #

PDF/UA был опубликован как [Стандарт ISO 14289-1](https://en.wikipedia.org/wiki/ISO_14289) в августе 2012 г. и на сегодняшний день является первым полным определением набора требований к общедоступным PDF-документам. Термин «универсально доступный» означает понимание того, что информация, содержащаяся в документе [PDF](/ru/pdf/), должна быть одинаково и независимо доступна для всех в целом и для людей с ограниченными возможностями в частности. Внедрение стандарта PDF/UA можно считать важным шагом в создании инструментов и приложений для создания и чтения PDF-контента.

## Требования к формату файла ##

PDF/UA имеет в своей основе определенные требования, которые являются сущностью этого стандарта. По сути, они основаны на тегировании PDF-файлов, что означает, что все документы PDF/UA должны быть правильно тегированы. Также требуется, чтобы теги были семантически подходящими и располагались в логическом порядке. Это гарантирует, что конечный документ, созданный с помощью спецификации PDF/UA, будет более надежным и доступным. Это может заставить авторов PDF задаться вопросом, нужно ли им знать все обо всех таких требованиях? К счастью, это не так, поскольку инструменты соответствия PDF/UA берут на себя ответственность за добавление и сохранение доступности PDF.

Требования к формату файла для PDF/UA следующие.

* Контент классифицируется одним из двух способов: осмысленный контент и артефакты, такие как декоративные элементы страницы. Весь значимый контент должен быть помечен тегами и интегрирован в дерево структуры всех тегов в документе. Артефакты, с другой стороны, должны быть только помечены как таковые.
* Значимый контент должен быть помечен тегами и вместе с другими тегами в документе создавать полное дерево структуры.
* Осмысленный контент должен быть помечен соответствующими смысловыми тегами.
* Дерево структуры, создаваемое тегами документа, должно отражать логический порядок чтения документа.
* Можно использовать только стандартные теги, определенные в PDF 1.7; если используются какие-либо другие теги, запись о назначении ролей должна записывать, какой стандартный тег представляет каждый из них.
* Информация не может быть передана только с помощью визуальных средств (например, контраст, цвет или положение на странице).
* Запрещено мерцание, мерцание или мерцание содержимого как в виде эффектов, управляемых JavaScript, так и в составе любых видео, встроенных в PDF-файл.
* Должен быть указан заголовок документа, и документ должен быть настроен так, чтобы заголовок (а не имя файла) отображался в заголовке окна.
* Язык всего контента должен быть указан, а изменения языка должны быть явно отмечены как таковые.

## Соответствие PDF/UA ##

Стандарт PDF/UA определяет спецификации контента, устройств чтения и вспомогательных технологий. Эти три аспекта связаны друг с другом на основе содержания документа. Требования соответствия для каждого из них указаны ниже.

## Соответствующие файлы ##

Файлы, соответствующие стандарту PDF/UA, должны содержать функции, соответствующие [спецификациям PDF 1.7](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf). Однако функции, запрещенные PDF/UA, должны быть исключены.

## Соответствующие читатели ##

Соответствующий читатель должен соблюдать правила, прописанные в спецификациях PDF 1.7. В частности, он должен поддерживать:

* все теги, атрибуты и ключевые значения, указанные для специальных возможностей. Он также должен иметь возможность обрабатывать и представлять цифровые подписи, аннотации и дополнительный контент.
* обрабатывать и представлять цифровые подписи, аннотации и дополнительный контент
* перемещаться по документу различными способами

## Соответствующие вспомогательные технологии ##

Соответствующая вспомогательная технология предназначена для поддержки функций PDF/UA. К ним относятся, например, функции контента и средства чтения, и они должны обеспечивать навигацию по меткам страниц, структуре документа или структуре. Это также должно позволять пользователю переопределять масштаб навигации по умолчанию.

## Использованная литература ##

* [PDF/UA - По Википедии](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA в двух словах](https://pdfa.org/pdfua-in-a-nutshell/)

