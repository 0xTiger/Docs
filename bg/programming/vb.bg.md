{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "файл", "разширение", "файлов формат", "Visual Basic", "Ръководство за програмиране" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - файл с код на Visual Basic",
  "description":"Научете за VB файловия формат и API, които могат да създават и отварят VB файлове.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е VB файл?

VB файлът е файл с изходен код, създаден на езика Visual Basic, който е създаден от Microsoft за разработка на .NET приложения. Друг подобен език с различен синтаксис е C#, чиито файлове се записват с файлово разширение [.CS](/bg/programming/cs/). Файловият формат предоставя език за програмиране на ниско ниво за писане на код, който се компилира за генериране на крайния изходен файл под формата на EXE или DLL. Те могат да бъдат създадени и компилирани с Microsoft Visual Studio. Microsoft Visual Studio Express може също да се използва за създаване и актуализиране на такива файлове, което е безплатна IDE. Един прост проект [решение] на Visual Studio (/bg/programming/sln/), създаден с език VB, може да се състои от един или повече такива файлове. Файловете, маркирани за включване в компилация, са изброени във файла [CSPROJ](/bg/programming/csproj/), който е част от проекта и указва на компилатора да използва маркираните файлове.

## VB файлов формат - повече информация

VB файловете са текстови файлови формати, които могат да бъдат отворени във всеки текстов редактор за редактиране. Въпреки това, когато се отвори в поддържана IDE с правилно подчертаване на синтаксиса, кодът е лесен за четене и подреждане. Прост VB файл съдържа:

* Декларация на пространства от имена - За позоваване на конкретна функционалност, дефинирана от това конкретно пространство от имена
* Декларация на променливи - За деклариране на променливи на ниво клас за конкретната реализация
* Декларация на методи - За деклариране на декларация на методи за конкретната функционалност

## Пример за VB файлов формат

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```


