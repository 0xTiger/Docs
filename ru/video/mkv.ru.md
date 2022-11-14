{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла MKV",
  "keywords" :[ "mkv", "матроска видео", "формат mkv", "как воспроизводить файлы mkv", "видео", "файл", "формат" ],
  "description":"Узнайте о формате файлов MKV и API-интерфейсах, которые могут создавать и открывать файлы MKV.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Что такое файл MKV? ##

MKV (Matroska Video) — это мультимедийный контейнер, аналогичный форматам [MOV](/ru/video/mov/) и [AVI](/ru/video/avi/), но он поддерживает более одной дорожки аудио и субтитров в одном файле. Файл MKV — это формат мультимедийного контейнера Matroska, используемый для видео. MKV основан на Extensible Binary Meta Language и поддерживает несколько форматов сжатия видео и аудио. Основное различие между MKV и другими видеоформатами заключается в том, что MKV — это контейнер, а не кодек. Файлы MKV сохраняются с расширением .mkv. MKV может включать аудио, видео и субтитры в один файл, даже если эти элементы используют разные типы кодирования. Например, у вас может быть файл MKV, содержащий видео H.264 и MP3 или AAC для аудио. MKV также поддерживает описания, рейтинги, обложки и даже точки глав. Есть несколько ключевых особенностей, благодаря которым MKV ориентирован на будущее. Эти функции включают в себя:

- Поддержка быстрого поиска.
- Возможность выбора различных аудио и видео потоков.
- Поддержка субтитров (жестко и программно).
- Поддержка метаданных, глав и меню.
- Возможность потоковой передачи онлайн.
- Возможность восстановления ошибочных файлов, которые обеспечивают возможность воспроизведения поврежденных файлов.

## Краткая история ##

Файл MKV возник в 2002 году в России. Ведущим разработчиком был Лассе Кярккяйнен, который работал с основателем Matroska Стивом Ломмом и командой программистов. MKV был разработан как проект с открытыми стандартами, что означает, что он имеет открытый исходный код и может использоваться бесплатно. Со временем формат был улучшен и стал основой мультимедийного формата WebM в 2010 году.

## Матроска Дизайн ##

Matroska добавляет в спецификацию EBML следующие ограничения.

- **docType** **заголовка EBML** должен быть 'matroska'.
- Значение **EBMLMaxIDLength** в **заголовке EBML** должно быть равно 4.
- **EBMLMaxSizeLength** **EBML Header** должен иметь значение от 1 до 8 (включительно).

Все элементы верхнего уровня кодируются 4 октетами.

- Языковые коды: Matroska (версии с 1 по 3) использовала языковые коды, которые могут быть либо трехбуквенной библиографической формой ISO-639-2 (например, «fre» для французского), либо дополнительным кодом страны, например, «fre-ca». "для канадского французского языка. Начиная с Matroska версии 4, для языковых кодов МОЖЕТ использоваться либо ISO 639-2, либо BCP 47, хотя BCP 47 рекомендуется.
- Физические типы: они имеют разное значение как для аудио-, так и для видеофайлов. Например, ChapterPhysicalEquiv = 60 означает (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) для аудио и (DVD / VHS / LASERDISC) для видео.
- Структура блока - Заголовок блока: Заголовок блока содержит информацию о номере дорожки, метках времени, типе шнуровки и т. д.
- Lacing: это механизм для экономии места при хранении данных, который обычно используется для небольших блоков данных (кадров). Существует 3 вида шнуровки:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- Структура SimpleBlock: она основана на **блочной структуре** с основным отличием в добавлении флагов **Keyframe** и **Discardable**. В остальном все то же самое.

## Структура Матроски ##

Документ Matroska должен состоять как минимум из одного **Документа EBML** с использованием **Типа документа Matroska**. Каждый **документ EBML** должен начинаться с **заголовка EBML**, за которым следует **корневой элемент EBML**, определяемый как сегмент. Matroska определяет несколько элементов верхнего уровня, которые могут встречаться в **сегменте**.

EBML использует систему элементов для составления документа EBML. Ниже приведен список элементов верхнего уровня в файле Matroska:

- **EBML-документ**: оболочка для всего файла.
- **Заголовок EBML**: содержит информацию о заголовке файла, например DocType.
- **Сегмент**: верхний элемент, содержащий все остальные элементы верхнего уровня.
- **SeekHead**: содержит положение сегментов других элементов верхнего уровня.
- **Информация**: содержит общую информацию о сегменте.
- **Треки**: элемент информации верхнего уровня с описанием множества треков.
- **Главы**: используется для определения основных меню и данных разделов.
- **Кластер**: элемент верхнего уровня, содержащий блочную структуру.
- **Cues**: элемент верхнего уровня, содержащий все записи, локальные для сегмента, которые ускоряют поиск доступа.
- **Вложения**: содержит вложенные файлы.
- **Теги**: этот элемент содержит метаданные, описывающие Треки, Издания, Главы, Вложения или Сегмент в целом.

В следующей таблице показана структура документа Matroska с большинством элементов, отображаемых в иерархии:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| Заголовок EBML | | | |
| Сегмент | Искатьголову| Искать | Искать ID |
| | | | ИскатьПозицию |
| | Информация | идентификатор сегмента | |
| | | СегментФайлимя | |
| | | ПредыдущийUID | |
| | | ПредыдущийИмяФайла | |
| | | СледующийUID | |
| | | СледующееИмяФайла | |
| | | СегментСемейный | |
| | | ГлаваПеревести | |
| | | Отметка времениШкала | |
| | | Продолжительность | |
| | | ДатаUTC | |
| | | Название | |
| | | MuxingApp | |
| | | Приложение для письма | |
| | Треки | Отслеживание | номер дорожки |
| | | | TrackUID |
| | | | Тип трека |
| | | | Имя |
| | | | Язык |
| | | | ID кодека |
| | | | КодекЧастный |
| | | | ИмяКодека |
| | | | Видео | ПометитьЧересстрочная |
| | | | | Порядок полей |
| | | | | Стереорежим |
| | | | | Альфа-режим |
| | | | | ПиксельШирина |
| | | | | ПиксельВысота |
| | | | | Ширина дисплея |
| | | | | Высота дисплея |
| | | | | Тип соотношения сторон |
| | | | | Цвет |
| | | | Аудио | Частота дискретизации |
| | | | | Каналы |
| | | | | Битовая глубина |
| | Главы | ИзданиеЗапись | EditionUID |
| | | | ИзданиеFlagСкрытый |
| | | | EditionFlagDefault |
| | | | ИзданиеФлагЗаказано |
| | | | ГлаваАтом | ГлаваUID |
| | | | | UID_строки_раздела |
| | | | | ГлаваВремяНачало |
| | | | | ГлаваВремяКонец |
| | | | | ГлаваФлагСкрытый |
| | | | | ГлаваДисплей | Чапстринг |
| | | | | | ГлаваЯзык |
| | Кластер | Отметка времени |
| | | Сайленттрекс |
| | | Позиция |
| | | ПредыдущийРазмер |
| | | простой блок |
| | | БлокГрупп |
| | | Зашифрованный блок |
| | Подсказки | ключевая точка | CueTime |
| | | | CueTrackPositions |
| | Вложения | Прикрепленный файл | Описание файла |
| | | | ИмяФайла |
| | | | FileMimeType |
| | | | ФайлUID |
| | | | ФайлРеферал |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Теги | Тег | Цели | таргеттипевалуе |
| | | | | Тип цели |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | простой тег | Имя тега |
| | | | | Язык тегов |
| | | | | ТегПо умолчанию |
| | | | | ТегСтрока |
| | | | | ТегДвоичный |
| | | | | простой тег |


### Использование кодеков ###

Если вам не нужен новый медиаплеер и вы предпочитаете использовать существующий плеер, вам потребуется установить некоторые кодеки (сокращение от сжатия/распаковки). Несмотря на то, что загрузка кодеков является допустимым вариантом, вы должны быть осторожны с источником, который может содержать вредоносное ПО.

## Использованная литература ##

- [Матроска из Википедии](https://en.wikipedia.org/wiki/Matroska)
