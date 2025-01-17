---
date: 2019-10-11
keywords: rm, .rm, формат файла rm, формат файла .rm, расширение .rm, формат файла RealMedia
автор:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Узнайте о формате файла RM и API-интерфейсах, которые могут создавать и открывать файлы RM."
title: Формат файла RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## .RM вариант № ##

RealMedia — это собственный формат контейнера мультимедиа, разработанный RealNetworks и использующий расширение .rm. Он используется с комбинацией [RealAudio (RA)](/ru/audio/ra/) и [RealVideo(RV)](/ru/video/rv/) для потоковой передачи через Интернет. Эти потоки имеют постоянный битрейт. Для переменного битрейта RealNetworks разработала формат RealMedia Variable Bitrate (RMVB). RealMedia подходит для потоковой передачи контента через Интернет и может использоваться, например, для потокового телевидения в прямом эфире.

## Структура файла RealMedia ##

Файл RealMedia состоит из серии фрагментов, каждый из которых имеет следующую структуру:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Ниже приведены типы фрагментов, присутствующих в файле RealMedia:

- **Заголовок файла RealMedia (.RMF)**: это должен быть первый блок в файле RealMedia. В одном файле присутствует только один фрагмент RMF. Он содержит информацию о количестве заголовков.
- **Заголовок свойств файла (PROP)**: содержит информацию об общих свойствах файла RealMedia. В каждом файле RealMedia есть только один фрагмент этого типа.
- **Заголовок свойств носителя (MDPR)**: этот фрагмент содержит информацию о свойствах потока. Он содержит информацию о типе потока и используемом кодеке. Для каждого потока в файле имеется один блок MDPR.
- **Заголовок описания контента (CONT)**: этот блок содержит текстовую информацию, такую как название или автор контента в файле RealMedia. Этот фрагмент предназначен только для информационных целей.
- **Заголовок данных (DATA)**: этот фрагмент содержит группу пакетов данных.
- **Заголовок индекса (INDX)**: этот фрагмент идет после всех фрагментов DATA и содержит элементы индекса. В одном файле может быть несколько фрагментов INDX.

## Поддерживаемые форматы аудио и видео ##

### Аудиоформаты ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
- днет: AC3
- сипр: Сипро
- повар: повар
- АЦП: ATRAC3
- ralf: формат RealAudio без потерь
- раак: LC-AAC
- рацп: HE-AAC

### Форматы видео ###

- CLV1: ClearVideo
- РВ10: Н.263
- РВ13: Н.263
- РВ20: Н.263+, РВ20
- RV30: предшественник H.264
- RV40: предшественник H.264, RV40
- РВТР: H.263+ (RV20)

## Использованная литература ##

- [RealMedia - Википедия](https://en.wikipedia.org/wiki/RealMedia)

