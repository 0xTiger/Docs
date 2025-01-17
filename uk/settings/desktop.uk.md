{
"дата": "31.05.2023",
  "keywords": [
"файл робочого столу",
"що таке файл робочого столу",
"що містить файл робочого столу",
"приклад файлу робочого столу",
"як відкрити файл робочого столу",
"який формат файлу робочого столу",
"файл",
"розширення файлу робочого столу",
"розширення"
],
  "author": {
"display_name": "Шейкіл Фаїз"
},
"draft": "false",
"toc": true,
"title": "Формат файлу DESKTOP - файл запису робочого столу",
  "description":"Дізнайтеся про формат DESKTOP та API, які можуть створювати та відкривати файли DESKTOP.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
      "parent": "settings"
}
},
"lastmod": "2023-05-31"
}

## Що таке файл DESKTOP?

Файл .desktop — це файл конфігурації, який використовується робочим середовищем Linux для визначення ярликів програм і засобів запуску. Він надає метадані про програму, наприклад її назву, значок, команду для виконання та інші властивості. Ці файли зазвичай використовуються для створення ярликів у меню програм, панелях запуску на робочому столі та в системах на базі Linux.

## Що містить файл DESKTOP?

Файл .desktop має певний формат і містить кілька ключових полів:

- **[Desktop Entry]:** Це головний заголовок розділу для файлу .desktop.
- **Назва:** Вказує назву програми.
- **Коментар:** містить короткий опис або коментар до програми.
- **Exec:** визначає команду для виконання під час запуску програми.
- **Значок:** вказує шлях до файлу значка, пов’язаного з програмою.
- **Термінал:** визначає, чи потрібно запускати програму у вікні терміналу.
- **Тип:** визначає тип запису, наприклад "Програма" або "Посилання".
- **Категорії:** Визначає категорії або групи, у яких програма має відображатися в меню.
- **StartupNotify:** визначає, чи середовище робочого столу має показувати сповіщення про запуск програми.
- **NoDisplay:** Визначає, чи потрібно програму приховувати в меню.
- **Дії:** Визначає додаткові дії, які можна виконати над програмою, як-от відкриття певного файлу.

## Приклад файлу DESKTOP

Ось приклад файлу .desktop для фіктивного текстового редактора під назвою "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

У цьому прикладі файл .desktop визначає програму "MyTextEditor" із пов’язаними властивостями. Він також містить дві додаткові дії "Відкрити нове вікно" та "Відкрити існуючий файл", доступ до яких можна отримати з контекстного меню засобу запуску програм.

Розмістивши файл .desktop у певних каталогах, таких як `/usr/share/applications` або `~/.local/share/applications`, середовище робочого столу розпізнає його та відповідно відобразить програму в меню або дозволить її запуск із робочий стіл.

## Як відкрити файл DESKTOP?

Декілька програм можуть відкривати та обробляти файли .desktop. Ці програми зазвичай є файловими менеджерами або робочими середовищами в системах на базі Linux. Ось кілька прикладів:

- **Nautilus (файли):** файловий менеджер за умовчанням для робочого середовища GNOME.
- **Nemo:** файловий менеджер для робочого середовища Cinnamon.
- **Dolphin:** типовий файловий менеджер для робочого середовища KDE Plasma.
- **Thunar:** файловий менеджер за умовчанням для робочого середовища Xfce.
- **Редактор меню KDE:** Спеціальний інструмент для робочого середовища KDE Plasma, який дозволяє переглядати та редагувати файли .desktop.

Ці файлові менеджери та робочі середовища забезпечують графічний інтерфейс для керування файлами .desktop. Вони дозволяють переглядати та редагувати властивості файлів .desktop, створювати засоби запуску програм і організовувати ярлики в меню програм або на робочому столі.

Файли .desktop — це звичайні текстові файли, тому ви також можете відкривати та редагувати їх за допомогою текстового редактора на свій вибір. Просто клацніть правою кнопкою миші файл .desktop і виберіть "Відкрити за допомогою" або "Відкрити за допомогою іншої програми", щоб вибрати текстовий редактор зі списку встановлених програм.

## Який формат файлу DESKTOP?

Формат файлу .desktop відповідає певній структурі та формату. Це звичайний текстовий файл із набором пар ключ-значення, організованих у розділи. Ось огляд формату:

- **Заголовки розділів:** Кожен розділ починається із заголовка, укладеного в квадратні дужки ([]). Основний розділ зазвичай називається [Desktop Entry], який містить основні метадані програми або засобу запуску.
- **Пари ключ-значення:** у кожному розділі ви визначаєте властивості за допомогою пар ключ-значення. Формат: "Ключ=Значення". Ключ ідентифікує властивість, а значення надає відповідні дані.
- **Синтаксис властивостей:** Значення властивостей можуть бути різних типів, включаючи рядки, логічні значення, шляхи до файлів або списки. Формат кожного значення властивості залежить від його типу.
- **Коментарі:** Ви можете додати коментарі до файлу .desktop за допомогою символу "#". Усе, що йде після "#" у рядку, вважається коментарем і ігнорується.

## Список літератури
* [Вхідні файли робочого столу](https://www.baeldung.com/linux/desktop-entry-files)

