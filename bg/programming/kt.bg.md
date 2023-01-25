---
date: 2019-10-11
keywords: kt, .kt, файлов формат kotlin, как да отваряте файлове kotlin, как да стартирате файлове kotlin, файлов формат .kt, kt файл, файлово разширение kotlin, разширение .kt, kotlin срещу java
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT файлов формат
linktitle: KT
description: "Научете за KT файловия формат и API, които могат да създават и отварят KT файлове."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## Какво е KT файл? ##

Изходният код, написан на Kotlin, се запазва с разширение .kt, което е известно като **файлово разширение Kotlin**. Kotlin е междуплатформен език за програмиране с общо предназначение, разработен от JetBrains, за да бъде напълно съвместим с [Java](/bg/programming/java/). Търговската марка Kotlin е защитена от Фондация Kotlin.

Kotlin беше обявен като предпочитан език за програмиране за разработка на приложения за Android от Google на 7 май 2019 г. Android Studio 3.0 започна да поддържа Kotlin като алтернатива за разработка на приложения за Android през октомври 2017 г.

## Кратка история на файловия формат Kotlin KT##

Kotlin беше представен от JetBrains през юли 2011 г. като нов език за програмиране за JVM. Ръководителят на JetBrains Дмитрий Джемеров каза, че на повечето от езиците липсват функции, които търсят, с изключение на Scala, но бавната компилация на Scala е недостатък. Една от основните цели на Kotlin беше да се компилира толкова бързо, колкото Java. Проектът Kotlin беше с отворен код под лиценз Apache 2 през февруари 2012 г.

Версия 1.0 на Kotlin беше пусната на 15 февруари 2015 г. Android обяви първокласна поддръжка за Kotlin на Android на Google I/O 2017. Kotlin 1.2 беше пуснат на 28 ноември 2017 г. с възможност за споделяне на код между JVM и JavaScript платформи. Kotlin 1.3 беше пуснат на 29 октомври 2018 г. с поддръжка за асинхронно програмиране. На 7 май 2019 г. Google обяви Kotlin за предпочитания език за програмиране за разработка на приложения за Android. Kotlin 1.4 беше пуснат през август 2020 г. с някои леки промени за поддържане на оперативна съвместимост със Swift/Objective-C.

## Синтаксис на Kotlin ##

Kotlin е проектиран да бъде по-добър от Java, но все пак да бъде оперативно съвместим с Java код, за да позволи постепенна миграция от Java към Kotlin.

* Точката и запетая не са задължителни в Kotlin. Нов ред е достатъчен, за да посочи края на израза.
* Kotlin поддържа два типа променливи, само за четене, дефинирани от ключовата дума *val*, и променливи, дефинирани от ключовата дума *var*.
* Класовете са частни и окончателни по подразбиране. За да произлезе от клас, базовият клас трябва да бъде деклариран с ключовата дума *open*.
* Kotlin поддържа и процедурно програмиране.
* Входната точка към програмата Kotlin е "основната" функция, подобна на Java, C# и т.н.

### Пример за синтаксис ###

Следното е пример за синтаксис на Kotlin.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

В горния код ключовата дума **fun** дефинира функцията с име main. Вътре във функцията се декларира променлива само за четене „audience“ с ключовата дума **val**. Чрез използването на метода **println** на конзолата се отпечатва „Hello World from Kotlin“. Стойността на променливата аудитория се инжектира в низа със знака **$**.

## Kotlin срещу Java
Kotlin е официален език за писане на приложения за Android с много разширени функции, но много експертни Java разработчици все още не проявяват интерес да преминат към Kotlin. Те смятат, че могат да направят всичко само с Java. Така че следното е сравнението между две технологии, които могат да убедят разработчиците на Java да сменят:

| Параметър | Java | Котлин |
|--------------------|-----------|---------------- -|
| Единични обекти | √ | √ |
| Типове заместващи знаци | √ | Χ |
| Компилация | Байт кодове | Виртуална машина |
| Ламбда израз | Χ | √ |
| Инвариантен масив | Χ | √ |
| Нелични полета | √ | Χ |
| Smart Casts | Χ | √ |
| Нулева безопасност | Χ | √ |
| Статични членове | √ | Χ |

## Препратки ##

- [Kotlin (програмен език) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))
