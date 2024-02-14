{
"дата": "2023-05-15",
  "keywords": [
"csx файл",
"какво е csx файл",
"какво съдържа csx файлът",
"какъв е форматът на csx файла",
"файл",
"csx файлово разширение",
"разширение"
],
  "author": {
"показвано_име": "Шакил Фейз"
},
"draft": "false",
"toc": true,
"title": "CSX файлов формат - Visual C# скрипт",
  "description":"Научете за CSX формата и API, които могат да създават и отварят CSX файлове.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
      "parent": "programming"
}
},
"lastmod": "2023-05-15"
}

## Какво е CSX файл?

Visual C# Script (известен също като CSX) е файлов формат, използван от скриптовата машина Roslyn в .NET екосистемата на Microsoft. CSX файловете съдържат C# код, който може да се изпълнява директно без необходимост от отделна стъпка на компилиране.

Форматът CSX е специфичен за екосистемата на Microsoft и не е широко използван файлов формат в общото програмиране. CSX файловете често се използват в сценарии, при които се изисква бързо създаване на прототипи или функционалност за скриптове. Те ви позволяват да създавате и изпълнявате C# програми по по-лек начин в сравнение със създаването на пълноценно компилирано приложение.

За да изпълните CSX файлове, можете да използвате инструменти като .NET Interactive Notebooks, които предоставят интерактивна среда за изпълнение на C# код. Visual Studio Code с разширението C# и .NET Core SDK може също да се използва за работа с CSX файлове.

## Какво съдържа CSX файлът?

CSX (C# Script) файл съдържа C# код, който може да се изпълнява директно. Може да включва всеки валиден C# код като декларации на променливи, функции, класове и други програмни конструкции.

Ето пример какво може да съдържа CSX файлът:

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

CSX файловете могат също да включват инструкции за импортиране, препратки към външни библиотеки и други функции на езика C#, за да поддържат функционалността на кода. Кодът се интерпретира и изпълнява в движение без необходимост от компилация, което го прави подходящ за скриптове и задачи за бързо прототипиране.

## Какъв е форматът на CSX файла?

Форматът CSX (C# Script) следва прост текстово базиран формат. Обикновено има файлово разширение .csx, за да се разграничи от обикновените файлове с изходен код на C# (.cs).

CSX файловете могат да се редактират с помощта на всеки текстов редактор или интегрирана среда за разработка (IDE), която поддържа подчертаване на синтаксиса на C#. След като CSX файлът е готов, той може да бъде изпълнен с помощта на инструменти като .NET Interactive Notebooks, интерфейса на командния ред на .NET Core (CLI) или IDE с поддръжка на C# скриптове.

## Препратки
* [Програмиране на C# с Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)
