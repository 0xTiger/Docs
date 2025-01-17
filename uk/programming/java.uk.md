---
date: 2019-10-11
keywords: java, .java, формат файлу java, як відкрити файли java, як запустити файли java, файл java, приклад коду java
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Формат файлу Java
linktitle: Java
description: "Дізнайтеся про формат файлів Java та API, які можуть створювати та відкривати файли Java."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Що таке файл Java? ##
Файл, що містить вихідний код Java і збережений із розширенням .java, називається файлом Java. Java є однією з найбільш широко використовуваних технологій для розробки ігор, мобільних, веб-додатків і настільних додатків. Оскільки Java не залежить від платформи, вона бездоганно працює на Windows, Mac, Linux, Raspberry Pi тощо. Java дуже схожа на C# і C++, тому простіше перемикатися між цими мовами.

## Коротка історія ##

Проект Java був ініційований у червні 1991 року Джеймсом Гослінгом, Майком Шеріданом і Патріком Нотоном. Ява спочатку називалася Дубом. Пізніше його було перейменовано в Green і, нарешті, на Java. Джеймс Гослінг розробив Java із синтаксисом, подібним до C/C++. Перша публічна версія Java була випущена в 1996 році компанією Sun Microsystems. Він міг працювати на всіх популярних системах, завдяки чому Java швидко стала популярною. З випуском Java 2 у грудні 1998 року було створено кілька конфігурацій для різних типів платформ. Версії були такі

- J2EE (Java EE): для корпоративних рішень
- J2ME (Java ME): для мобільних додатків
- J2SE (Java SE): для настільних програм

19 листопада 2006 року Sun випустила віртуальну машину Java (JVM) як безкоштовне програмне забезпечення з відкритим кодом. Після того, як Oracle Corporation придбала Sun Microsystems у 2009–2010 роках, Джеймс Гослінг пішов з Oracle 2 квітня 2010 року.

## Як запустити/виконати код Java ##

Щоб виконати код Java, його потрібно спочатку скомпілювати. Для цього потрібен Java SDK. Java SDK компілює код Java у файл класу байт-коду. Існують такі IDE, як Eclipse та IntelliJ Idea, які полегшують роботу з файлами Java, забезпечуючи автозавершення коду та простий у використанні інтерфейс для компіляції та виконання коду Java.

## Формат файлу Java ##

На синтаксис Java сильно вплинули C і C++, але на відміну від C++, Java була побудована майже виключно як об’єктно-орієнтована мова. У Java весь код написаний у класах, і кожен елемент даних є об’єктом. На відміну від C++, Java не підтримує перевантаження операторів або множинне успадкування.

### Зразок коду Java ###

Нижче наведено приклад синтаксису Java.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
У наведеному вище коді ключове слово **public** позначає модифікатор доступу. У ньому зазначено, що до цього класу можуть отримати доступ класи поза ієрархією класів. Модифікатор доступу також може бути **protected** (до нього можна отримати доступ у тому самому пакеті) або **private** (методи можуть бути доступні лише тому самому класу). **static** перед методом вказує на те, що метод можна викликати без певного екземпляра класу. **void** вказує на те, що метод нічого не поверне. Щоб вивести рядок на консоль. Використовується команда System.out.println. У цій команді клас *System* має статичне поле *out*, яке є екземпляром класу *PrintStream*, що містить метод *println*.

Ім’я файлів Java має збігатися з ім’ям класу. Отже, файл Java для прикладу коду матиме назву *ExampleApp.java*.

## Посилання ##

- [Java (мова програмування) - Вікіпедія](https://en.wikipedia.org/wiki/Java_(programming_language))

