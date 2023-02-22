{
  "date" : "2019-10-11",
  "keywords" :["xoml", "Файл", "Розширення", "Формат файлу", "Розширення файлу", "Розширювана мова розмітки об'єктів"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XOML - формат файлу робочого процесу Windows",
  "description":"Дізнайтеся про формат файлу XOML та API, які можуть створювати та відкривати файли XOML.",
  "linktitle" : "XOML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл XOML?

XOML є акронімом Extensible Object Markup Language і є форматом серіалізації для об’єктів робочого циклу Windows Workflow Foundation. На основі **[XAML](/uk/web/xaml/)** він здебільшого використовується для створення інтерфейсів користувача у звичайному **[XML](/uk/web/xml/)**. Вони використовуються для оголошення робочого процесу для інтерфейсу користувача та компілюються разом з окремим файлом, що містить логіку реалізації. Він містить структуру на основі дерева, яка визначає кореневий вузол робочого процесу, вкладені піделементи та вбудовані сегменти коду. Коли новий робочий цикл створюється за допомогою Visual Studio для .NET, ви можете вибрати, у якому форматі він має бути: у форматі Code або Code Separated. Якщо ви виберете пізніший, IDE створить для вас два файли; один у форматі XOML (складається з макета робочого циклу та налаштувань), а інший у форматі [.CS](/uk/programming/cs/)/[.VB](/uk/programming/vb/), де міститься код програмування.
