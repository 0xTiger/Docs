{
"дата": "2023-06-08",
  "keywords": [
"hpp файл",
"какво е hpp файл",
"какво съдържа hpp файлът",
"пример за hpp файл",
"какъв е форматът на hpp файла",
"файл",
"hpp файлово разширение",
"разширение"
],
  "author": {
"показвано_име": "Шакил Фейз"
},
"draft": "false",
"toc": true,
"title": "HPP файлов формат - C++ заглавен файл",
  "description":"Научете за HPP формата и API, които могат да създават и отварят HPP файлове.",
  "linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
      "parent": "programming"
}
},
"lastmod": "2023-06-08"
}

## Какво е HPP файл?

Файловият формат ".hpp" обикновено се използва за заглавни файлове в езика за програмиране C++. Заглавните файлове обикновено съдържат декларации и дефиниции на функции, класове, променливи и константи, които се използват от други файлове с изходен код в C++ проекта.

Целта на използването на заглавни файлове е да предостави начин за споделяне на общ код в множество файлове с изходен код без дублиране на самия код. Когато изходният файл на C++ трябва да получи достъп до декларации или дефиниции от заглавния файл, той включва заглавния файл с помощта на директивата на препроцесора `#include`.

Файловото разширение ".hpp" често се използва, за да покаже, че даден файл е C++ заглавен файл. Не е изискване да използвате това конкретно разширение за заглавни файлове и може също да попаднете на заглавни файлове с ".h" или други разширения. Изборът на разширение до голяма степен е въпрос на конвенция и лични предпочитания.

Когато изходният файл на C++ включва заглавен файл с помощта на `#include`, компилаторът ефективно комбинира съдържанието на заглавния файл с изходния файл, преди да го компилира като единица. Това позволява на изходния файл да има достъп до декларации и дефиниции в заглавния файл, предоставяйки необходимата информация за компилатора, за да извърши проверка на типа и генериране на код.

## Какво съдържа HPP файлът?

Ето някои общи съдържания, които можете да намерите във файла ".hpp":

- **Функционални декларации:** Заглавните файлове често включват функционални декларации без действителните им реализации. Тези декларации предоставят информация за името на функцията, типа на връщане и параметрите, което позволява на други файлове с изходен код да използват функция, без да е необходимо да знаят подробности за изпълнението.
- **Декларации на класове:** Заглавните файлове могат да съдържат декларации на класове, включително име на клас, членски променливи, членски функции и спецификатори за достъп. Чрез включването на декларация на клас в заглавния файл, други файлове с изходен код могат да създават обекти от този клас и да имат достъп до неговите членове.
- **Декларации на константи:** Заглавните файлове могат да дефинират константи, като глобални променливи или enum стойности, които са предназначени да се споделят между множество файлове с изходен код. Тези константи могат да бъдат достъпни чрез включване на заглавен файл в други изходни файлове, което им позволява да използват дефинираните константи.
- **Дефиниции на типове:** Заглавните файлове могат да съдържат дефиниции на типове, използващи ключова дума "typedef" или псевдоними на типове, използващи ключова дума "using". Тези дефиниции създават нови имена за съществуващи типове, което прави кода по-четлив и поддържаем.
- **Вградени дефиниции на функции:** В някои случаи заглавните файлове може да съдържат вградени дефиниции на функции. Вградените функции са малки функции, които се разширяват в сайта за повикване, вместо да се извикват като отделна функция. Включването на вградена дефиниция на функция в заглавния файл позволява на компилатора да замени директно извикването на функция с тялото на функцията, което потенциално подобрява производителността.

## Пример за HPP файл

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

## Какъв е форматът на HPP файла?

HPP е обикновен текстов файл, но следва общите правила и синтаксис на езика за програмиране C++. Ето разбивка на общия формат и структура на файла ".hpp":

- **Предпазители на заглавки:** Обикновено файлът ".hpp" започва с предпазители на заглавки, за да се предотврати многократно включване на един и същи файл. Това се постига с помощта на директиви на препроцесора като `#ifndef`, `#define` и `#endif`. Защитата на заглавката гарантира, че съдържанието на файла е включено само веднъж по време на процеса на компилиране.
- **Изявления за включване:** След предпазителите на заглавките можете да включите други необходими заглавни файлове, като използвате директивата `#include`. Те могат да включват стандартни библиотечни заглавки или други персонализирани заглавки, изисквани от вашия код.
- **Декларации и дефиниции:** Основното съдържание на файла ".hpp" са декларациите и, в някои случаи, дефинициите на класове, функции, константи, псевдоними на типове и други елементи. Например, можете да декларирате класове, използвайки ключова дума `class`, функции, използвайки техния тип на връщане, име и списък с параметри, и константи, използвайки ключова дума `const`, последвана от техния тип и име.
- **Вградени дефиниции на функции:** В определени случаи можете да включите вградени дефиниции на функции директно във файла ".hpp". Вградените функции обикновено се дефинират в тялото на класа, което означава, че дефиницията на функцията е включена заедно с нейната декларация. Това може да стане чрез префикс на дефиницията на функция с ключова дума `inline`.
- **Декларации на пространства от имена:** Ако използвате пространства от имена във вашия код, можете да ги декларирате в рамките на файла ".hpp". Това се прави с помощта на ключова дума `namespace`, последвана от име на namespace и затваряне на съответния код в блока namespace.

## Препратки
* [Заглавни файлове (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
