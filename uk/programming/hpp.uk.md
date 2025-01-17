{
"дата": "08.06.2023",
  "keywords": [
"файл hpp",
"що таке файл hpp",
"що містить файл hpp",
"приклад файлу hpp",
"який формат файлу hpp",
"файл",
"розширення файлу hpp",
"розширення"
],
  "author": {
"display_name": "Шейкіл Фаїз"
},
"draft": "false",
"toc": true,
"title": "Формат файлу HPP - файл заголовка C++",
  "description":"Дізнайтеся про формат HPP і API, які можуть створювати та відкривати файли HPP.",
  "linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
      "parent": "programming"
}
},
"lastmod": "2023-06-08"
}

## Що таке файл HPP?

Формат файлу ".hpp" зазвичай використовується для файлів заголовків у мові програмування C++. Файли заголовків зазвичай містять оголошення та визначення функцій, класів, змінних і констант, які використовуються іншими файлами вихідного коду в проекті C++.

Мета використання файлів заголовків полягає в тому, щоб забезпечити спосіб спільного використання спільного коду в кількох файлах вихідного коду без дублювання самого коду. Коли вихідний файл C++ потребує доступу до декларацій або визначень із файлу заголовка, він включає файл заголовка за допомогою директиви препроцесора `#include`.

Розширення файлу ".hpp" часто використовується, щоб вказати, що файл є файлом заголовка C++. Використовувати це конкретне розширення для файлів заголовків не обов’язково, і ви також можете натрапити на файли заголовків із ".h" або іншими розширеннями. Вибір розширення значною мірою залежить від традицій і особистих уподобань.

Коли вихідний файл C++ включає файл заголовка за допомогою `#include`, компілятор ефективно поєднує вміст файлу заголовка з вихідним файлом перед тим, як компілювати його як одиницю. Це дозволяє вихідному файлу отримувати доступ до декларацій і визначень у файлі заголовка, надаючи компілятору необхідну інформацію для виконання перевірки типу та генерації коду.

## Що містить файл HPP?

Ось деякий загальний вміст, який ви можете знайти у файлі ".hpp":

- **Оголошення функцій:** Файли заголовків часто містять оголошення функцій без їх фактичної реалізації. Ці оголошення надають інформацію про назву функції, тип повернення та параметри, що дозволяє іншим файлам вихідного коду використовувати функцію без необхідності знати деталі реалізації.
- **Оголошення класу:** Файли заголовків можуть містити оголошення класу, включаючи назву класу, змінні-члени, функції-члени та специфікатори доступу. Включивши оголошення класу у файл заголовка, інші файли вихідного коду можуть створювати об’єкти цього класу та отримувати доступ до його членів.
- **Оголошення констант:** Файли заголовків можуть визначати константи, такі як глобальні змінні або значення enum, які призначені для спільного використання в кількох файлах вихідного коду. Доступ до цих констант можна отримати, включивши файл заголовка в інші вихідні файли, дозволяючи їм використовувати визначені константи.
- **Визначення типів:** Файли заголовків можуть містити визначення типів за допомогою ключового слова "typedef" або псевдоніми типів за допомогою ключового слова "using". Ці визначення створюють нові імена для існуючих типів, роблячи код більш читабельним і зручним для обслуговування.
- **Вбудовані визначення функцій:** У деяких випадках файли заголовків можуть містити вбудовані визначення функцій. Вбудовані функції — це невеликі функції, які розгортаються на місці виклику, а не викликаються як окрема функція. Включення вбудованого визначення функції у файл заголовка дозволяє компілятору замінювати виклик функції безпосередньо тілом функції, потенційно покращуючи продуктивність.

## Приклад файлу HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Який формат файлу HPP?

HPP — це звичайний текстовий файл, який відповідає загальним правилам і синтаксису мови програмування C++. Ось розподіл загального формату та структури файлу ".hpp":

- **Захисні заголовки:** Як правило, файл ".hpp" починається з запобіжних заголовків, щоб запобігти багаторазовому включенню того самого файлу. Це досягається за допомогою директив препроцесора, таких як `#ifndef`, `#define` і `#endif`. Захист заголовка гарантує, що вміст файлу буде включено лише один раз під час процесу компіляції.
- **Інструкції Include:** Після захисту заголовків ви можете включити інші необхідні файли заголовків за допомогою директиви `#include`. Вони можуть включати стандартні бібліотечні заголовки або інші користувацькі заголовки, необхідні для вашого коду.
- **Оголошення та визначення:** Основним вмістом файлу ".hpp" є оголошення та, у деяких випадках, визначення класів, функцій, констант, псевдонімів типів та інших елементів. Наприклад, ви можете оголошувати класи, використовуючи ключове слово `class`, функції — використовуючи їх тип повернення, ім’я та список параметрів, а константи — використовуючи ключове слово `const`, за яким слідує їхній тип і ім’я.
- **Визначення вбудованих функцій:** У деяких випадках ви можете включити визначення вбудованих функцій безпосередньо у файл ".hpp". Вбудовані функції зазвичай визначаються всередині тіла класу, тобто визначення функції включено разом із її оголошенням. Це можна зробити, додавши до визначення функції ключове слово `inline`.
- **Оголошення простору імен:** Якщо ви використовуєте простори імен у своєму коді, ви можете оголосити їх у файлі ".hpp". Це робиться за допомогою ключового слова `простір імен`, за яким іде ім’я простору імен і вкладення відповідного коду в блок простору імен.

## Список літератури
* [Файли заголовків (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

