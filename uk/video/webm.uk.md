---
date: 2019-10-11
keywords: WEBM, що таке файл WEBM, формат файлу WEBM
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Дізнайтеся про формат файлів WEBM та API, які можуть створювати та відкривати файли WEBM."
title: WEBM - формат відеофайлу WebM
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Що таке файл WEBM?

Файл із розширенням .webm — це відеофайл, заснований на відкритому безоплатному форматі файлу WebM. Він був розроблений для обміну відео в Інтернеті та визначає структуру контейнера файлів, включаючи формати відео та аудіо. WebM є на 100% безкоштовним, реалізуючи високу якість на основі відкритих технологій, таких як HTML, HTTP та TCP/IP, які відкриті для впровадження будь-ким. WebM був спеціально розроблений для обслуговування відео в Інтернеті, що робить його оптимізованим для потокового передавання з низьким обчислювальним слідом. Це робить його придатним для відтворення відео на будь-якому пристрої, особливо на малопотужних нетбуках, кишенькових комп’ютерах і планшетах.

## Формат файлу WEBM

Файлова структура WebM базується на підмножині формату файлу-контейнера Matroska [MKV](/uk/video/mkv/). Відеопотоки, доступні у файлі WebM, стискаються за допомогою високоефективних технологій стиснення VP8 або VP9. Так само аудіопотоки у файлі WebM стискаються за допомогою кодеків Vorbis або Opus, розроблених [Xiph Foundation](https://www.xiph.org/). Усі ці відео та аудіокодеки є безоплатними та можуть використовуватися безкоштовно.

Нижче наведено зведені специфікації для формату файлу WebM.

|Поле|Опис|
---|---|
|типу MIME |video/webm|
|Тип MIME лише аудіо |audio/webm|
|Уніфікований ідентифікатор типу| org.webmproject.webm|
|Назва відеокодеку| VP8 або VP9|
|Назва аудіокодека| Vorbis або Opus|

### Елементи WebM

WebM, будучи підмножиною специфікацій Matroska, забезпечує підтримку деяких функцій Matroska. Нижче наведено опис підтримуваних елементів.

#### EBML

|Найменування |Опис|
---|---|
|EBML|Встановіть характеристики EBML для даних, які слід дотримуватися. Кожен документ EBML повинен починатися з цього.|
|EBMLVersion |Версія синтаксичного аналізатора EBML, використана для створення файлу.|
|EBMLReadVersion|Мінімальна версія EBML, яку має підтримувати аналізатор для читання цього файлу.|
|EBMLMaxIDLength |Максимальна довжина ідентифікаторів, які ви знайдете в цьому файлі (4 або менше в Matroska).|
|EBMLMaxSizeLength|Максимальна довжина розмірів, які ви знайдете в цьому файлі (8 або менше в Matroska). Це не скасовує розмір елемента, вказаний на початку елемента. Елементи, розмір яких перевищує дозволений EBMLMaxSizeLength, вважаються недійсними.|
|DocType|Рядок, який описує тип документа, який слідує за цим заголовком EBML (у нашому випадку "webm").|
|DocTypeVersion|Версія інтерпретатора DocType, використана для створення файлу.|
|DocTypeReadVersion|Мінімальна версія DocType, яку інтерпретатор має підтримувати для читання цього файлу.|

#### Глобальні елементи

На даний момент підтримується лише елемент `Void`, який використовується для анулювання пошкоджених даних, щоб уникнути несподіваної поведінки під час використання пошкоджених даних. Вміст відкидається. Також використовується для резервування місця у піделементі для подальшого використання.

#### Відрізок
Цей елемент містить усі інші елементи верхнього рівня (рівень 1). Зазвичай файл Matroska складається з 1 сегмента.

#### Інформація про пошук мета

Підтримується пошук такої інформації.

|Назва елемента |Опис|
---|---|
|SeekHead |Містить позицію іншого елемента рівня 1.|
|Пошук |Містить один запис пошуку до елемента EBML.|
|SeekID |Двійковий ідентифікатор, що відповідає назві елемента.|
|SeekPosition |Позиція елемента в сегменті в октетах (0 = перший елемент рівня 1).|

## Список літератури

* [WebM](https://www.webmproject.org/)
* [Сховища коду WebM](https://www.webmproject.org/code/#webp-repositories)

