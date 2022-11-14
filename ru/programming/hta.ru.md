{
  "date" : "2021-09-16", 
  "keywords" :[ "hta", "файл", "расширение", "формат файла", "реализация hta", "Руководство по программированию", "пример hta", "приложение HTML", "приложение языка гипертекстовой разметки", "файлы HTA", "Приложение Microsoft HTML"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA — файлы приложений HTML",
  "description":"Узнайте о формате файла HTA и API-интерфейсах, которые могут создавать и открывать файлы HTA.",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## .HTA вариант №

HTMLA расшифровывается как **Приложение для языка гипертекстовой разметки** — это программа, совместимая с Microsoft Windows. Исходный код этой программы включает более одного языка сценариев, например [HTML](/ru/web/html/) и [JavaScript](/ru/web/js/). Для пользовательского интерфейса предпочтительнее приложение HTML, в то время как для выполнения требований логики программы используется любой другой язык сценариев.

HTML-приложение не зависит от модели безопасности интернет-браузера и работает как полностью доверенное приложение. Расширение, используемое для файлов, относящихся к этим приложениям, — HTA. Эти приложения включают функции HTML наряду со свойствами других языков сценариев.


## Краткая история ##

HTA был впервые представлен Microsoft в 1999 году вместе с выпуском Internet Explorer 5. Он был совместим с Internet Explorer и поэтому мог выполняться только в операционной системе Windows. Эта технология была запатентована в 2003 году. Файлы HTA выполняются так же, как и любые другие файлы .exe. Файлы HTA также совместимы с сегодняшней обновленной версией Windows 11.


## Техническая спецификация ##

HTA имеют тот же формат, что и любая другая HTML-страница, а некоторые атрибуты используются для управления стилями границ или значков программ. Более того, приводятся аргументы в пользу запуска ОМТ. Эти приложения можно запустить с помощью программы mshta.exe. Доступ к нему можно получить, просто дважды щелкнув файл. Эти программы автоматически запускаются вместе с Internet Explorer. Помимо других спецификаций, они не зависят от браузера Trident Engine, но не зависят от Internet Explorer. Это означает, что их можно выполнять без использования Internet Explorer.

Теги используются для настройки внешнего вида этих приложений. Преобразование из приложения Microsoft HTML в формат HTA проще, т.е. вам нужно только изменить расширение. Поскольку мы знаем, что этим приложениям полностью доверяют, они содержат больше функций и преимуществ по сравнению с простыми файлами HTML. Для создания HTA можно использовать текстовые редакторы. Эти редакторы могут быть приобретены Microsoft или любым другим надежным источником.


## Пример формата файла HTA ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Ссылка ##

* [HTA — из Википедии] (https://en.wikipedia.org/wiki/HTML_Application)


