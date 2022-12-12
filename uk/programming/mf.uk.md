{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - формат файлу маніфесту Java",
  "description":"Дізнайтеся про формат файлу MF та API, які можуть створювати та відкривати файли MF.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Що таке файл MF?

Файл із розширенням .mf — це файл маніфесту Java, який містить інформацію про окремі записи файлу [JAR](/uk/programming/jar/). Сам файл MF міститься у файлі JAR і містить усі розширення та визначення, пов’язані з пакетом. Файли JAR можна створити для використання як виконуваний файл. У такому випадку файл mainfest визначає головний клас програми, який містить оператор **`public static void main`**. Файли маніфесту називаються MANIFEST.MF і їх можна відкрити в будь-якому текстовому редакторі в операційних системах Windows, MacOS і Linux.

## Специфікації формату файлу маніфесту

[Специфікації формату файлу маніфесту](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) доступні Oracle у своєму посібнику щодо формату файлу JAR. Файл маніфесту складається з основних розділів, за якими йде список розділів для окремих записів у файлі JAR. Кожен розділ має певні правила та обмеження.

### Основні розділи

Основний розділ:

* містить інформацію про безпеку та конфігурацію файлу JAR
* містить інформацію про програму або розширення, частиною якої є файл JAR
* визначає основні атрибути для кожного окремого елемента маніфесту

**Примітка**: жодному атрибуту в цьому розділі не можна назвати «Назва».

### Окремі розділи

Окремий розділ визначає різні атрибути для пакетів або файлів JAR-файлу. Кожен розділ має починатися з атрибута з назвою «Ім’я», значення якого має бути відносним шляхом до файлу або абсолютною URL-адресою, яка посилається на дані поза архівом.

### Специфікації маніфесту

|Атрибути|Опис|
---|---|
|файл-маніфесту|новий рядок основного розділу *окремий розділ|
|основний-розділ|інформація про версію новий рядок *основний-атрибут|
|інформація про версію|Версія маніфесту : номер версії|
|номер-версії|цифра+{.цифра+}*|
|main-attribute|(будь-який допустимий головний атрибут) новий рядок|
|individual-section|Назва : значення нового рядка *perentry-attribute|
|perentry-attribute|(будь-який допустимий perentry атрибут) новий рядок|
|новий рядок|CR LF | LF | CR (без LF)|
|цифра|{0-9}|

## Список літератури

* [Oracle – формат файлу JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [Формат файлу JAR](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=Вони%20побудовані%20на%20розширенні%20файлу%20jar%20.)
