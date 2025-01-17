{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "файл", "расширение", "формат файла", "CSharp", "язык программирования" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS — файл кода CSharp",
  "description":"Узнайте о формате файла CS и API, которые могут создавать и открывать файлы CS.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## .CS вариант №

Файлы с расширением .cs представляют собой файлы исходного кода для языка программирования C#. Представленный Microsoft для использования с .NET Framework, формат файла предоставляет язык программирования низкого уровня для написания кода, который компилируется для создания конечного выходного файла в форме EXE или DLL. Их можно создать и скомпилировать с помощью Microsoft Visual Studio. Microsoft Visual Studio Express также можно использовать для создания и обновления таких файлов, что является бесплатной IDE. Файлы CS используются для разработки приложений, которые могут варьироваться от простых настольных приложений до более сложных программ. Простой проект Visual Studio [solution](/ru/programming/sln/), созданный с помощью языка C#, может состоять из одного или нескольких таких файлов. Файлы, помеченные для включения в компиляцию, перечислены в файле [CSPROJ](/ru/programming/csproj/), который является частью проекта и указывает компилятору использовать помеченные файлы.

## Формат файла CS ##

Файлы CS представляют собой текстовые форматы файлов, которые можно открывать в любом текстовом редакторе для редактирования. Однако при открытии в поддерживаемой среде IDE с правильной подсветкой синтаксиса код легко читать и упорядочивать. Простой файл CS содержит:

* Объявление пространств имен — для ссылки на конкретную функциональность, определенную этим конкретным пространством имен.
* Объявление переменных — для объявления переменных уровня класса для конкретной реализации.
* Объявление методов — для объявления объявлений методов для конкретной функциональности.

### Синтаксис ###

* Точка с запятой используется для обозначения конца оператора.
* Фигурные скобки используются для группировки операторов. Операторы обычно группируются в методы (функции), методы в классы, а классы в пространства имен.
* Переменные присваиваются с использованием знака равенства, но сравниваются с использованием двух последовательных знаков равенства.
* Квадратные скобки используются с массивами как для их объявления, так и для получения значения по заданному индексу в одном из них.

### Пример ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

