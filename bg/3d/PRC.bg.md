---
date: 2019-10-11
keywords: prc, .prc, файлов формат prc, как да отваряте prc файлове, разширение .prc, разширение prc
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC файлов формат
linktitle: PRC
description: "Научете за файловия формат PRC и API-тата, които могат да създават и отварят PRC файлове."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Файловите формати на PRC
Разширенията „.prc“ се използват за компактен 3D файлов формат за представяне на продукта и файлов формат за електронна книга от MobiPocket.

## Какво е компактен файл за представяне на продукта (PRC)?

PRC (Product Representation Compact) е 3D файлов формат, който е оптимизиран за съхраняване, зареждане и показване на 3D данни, особено идващи от CAD (компютърно подпомагано проектиране) системи. Това е последователен двоичен файл, написан по преносим начин. PRC може да се използва за вграждане на 3D данни в PDF файл. PRC поддържа повечето от основните конструкции на CAD като възли и части, дървета на 3D обекти, точно представяне на геометрията, триъгълно представяне и маркиране. PRC използва разширението .prc и използваният тип интернет медия е *model/prc*.

PRC е многофункционален файлов формат, който въз основа на използването му може или да се съхранява с помощта на редовно компресиране за директно представяне на CAD данни, или да се съхранява с помощта на висока компресия за намаляване на размера на файла. 3D данните, съхранявани в PDF, използвайки PRC формат, са съвместими с CAM и CAE приложения.

### Спецификация на файловия формат за продуктово представяне Compact (PRC).

PRC файлът има една основна секция на заглавката, последвана от една или повече файлови структури, последвани от един моделен файл в края. Файловата структура има една заглавка, последвана от следните секции с данни:

- **Globals**: Съдържа референтните файлови структури и цветове, стилове на линии и координатни системи за всеки дървовиден обект на файловата структура.
- **Дърво**: Съдържа описание на дървото от елементи като възникване на продукти, дефиниции на части, елементи за представяне и маркиране.
- **Теселация**: Съдържа всички теселирани (триангулирани) данни в листовите обекти на дървото (представителни елементи и маркировки).
- **Геометрия**: Съдържа всички точни данни за геометрията и топологията на листовите обекти на дървото (представителни елементи).
- **Допълнителна геометрия**: Съдържа обобщените данни за геометрията. Това позволява файлът да бъде частично зареден, без да се зарежда цялата геометрия.

Следва структурата на типичен PRC файл.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## Какво е файл с електронна книга MobiPocket с разширение PRC
Файлов формат за електронни книги, въведен от френска компания, наречена **Mobipocket**, също използва разширението „.prc“. Първоначално Mobipocket пусна безплатно приложение за множество интелигентни устройства като таблети, PDA устройства и смартфони. Разширението ".prc" всъщност е идентично с .mobi, но се използва особено за PDA, които поддържат само разширения **.prc** или **.pdb**.

### Спецификации на файловия формат на Mobipocket PRC
Файловият формат MobiPocket PRC е базиран на стандарта Open eBook, използващ XHTML, а също така може да включва JavaScript и рамки. Налична е и поддръжка за собствени SQL заявки, които да се използват с вградени бази данни.

Mobipocket Reader има библиотека за начална страница. Читателите могат да вмъкват празни страници във всяка част от книга и да добавят променливи рисунки. Обектите като анотации, отметки, корекции, бележки и чертежи се управляват от едно място. Изображенията се конвертират в GIF формат и имат максимален размер от 64K, което е достатъчно за мобилни телефони с малки екрани. Mobipocket Reader има електронни отметки и вграден речник.

Четецът има режим на цял екран за четене и поддръжка за много PDA устройства, комуникатори и смартфони. Продуктите Mobipocket поддържат повечето операционни системи Palm, Windows, Symbian, BlackBerry, но не и Android. Четецът работи под Linux или Mac OS X с помощта на WINE.

## Препратки

- [КНР - Уикипедия](https://en.wikipedia.org/wiki/PRC_(file_format))
- [Спецификация на PRC формат](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
– [Сравнение на формати на електронни книги – от Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)
