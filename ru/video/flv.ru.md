---
date: 2019-10-11
keywords: flv, .flv, формат файла flv, формат файла .flv, расширение .flv, расширение flv, формат видео flv
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Узнайте о формате файлов FLV и API-интерфейсах, которые могут создавать и открывать файлы FLV."
title: Формат FLV-файла
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## .FLV вариант № ##

FLV (Flash Video) — это формат файла-контейнера с расширением .flv. FLV используется для доставки аудио/видео контента через Интернет с помощью Adobe Flash Player или Adobe Air. Данные в FLV-файлах кодируются так же, как и в SWF-файлах. Прямая поддержка была добавлена в Flash Player 7 в 2003 году. Системы Adobe создали F4V в 2007 году из-за ограничений FLV.

### Кодировка ###

Файлы FLV содержат битовые видеопотоки Sorenson Spark, которые являются проприетарным вариантом видеостандарта H.263. Это обязательный формат сжатия для Flash Player 6 и 7. Flash Player версии 8 поддерживает битовые видеопотоки On2 TrueMotion VP6. Это рекомендуемый формат сжатия для Flash Player 8 и выше. FLV поддерживает звук в формате MP3, кодек Nellymoser Asao и кодек Speex с открытым исходным кодом. Он также поддерживает несжатый звук или звук в формате ADPCM. AAC (HE-AAC/AAC SBR, основной профиль AAC и AAC-LC) поддерживаются последними версиями Flash Player 9.

## Структура ##

Файлы FLV состоят из заголовка и пакетов. Файл FLV начинается с заголовка. Заголовок имеет следующие поля.

- **Подпись**: значение FLV.
- **Версия**: значение по умолчанию — 1. Допустимо только 0x01.
- **Флаги**: 0x04 используется для аудио, 0x01 — для видео, поэтому 0x05 используется как для аудио, так и для видео.
- **Размер заголовка**: значение по умолчанию – 9. Оно используется для пропуска нового развернутого заголовка.

После заголовка идет Packets. Файл FLV разделен на несколько пакетов, называемых тегами FLV, которые имеют 15-байтовые заголовки. Пакеты содержат метаданные для аудио, видео, сценариев, информацию о шифровании и полезную нагрузку. Пакеты FLV имеют следующие поля.

- **Зарезервировано**: зарезервировано для FMS и должно быть равно 0.
- **Фильтр**: указывает, фильтруются ли пакеты или нет.
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **Тип пакета**: определяет тип содержимого в пакете.
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **Размер данных**: указывает длину сообщения.
- **Временная метка ниже**: здесь хранится временная метка в миллисекундах, в которой применяются данные тега. Для первого пакета установлено значение NULL.
- **Timestamp Upper**: расширение для создания значения uint32_be.
- **Идентификатор потока**: для первого потока установлено значение NULL.
- **Данные полезной нагрузки**: это данные, основанные на типе пакета.

## Использованная литература ##

- [Флэш-видео - Википедия](https://en.wikipedia.org/wiki/Flash_Video)

