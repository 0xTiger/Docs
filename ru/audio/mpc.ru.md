---
date: 2021-03-21
keywords: mpc, формат файла Musepack, расширение .mpc
автор:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Узнайте о формате файла MPC и API-интерфейсах, которые могут создавать и открывать файлы MPC."
title: MPC - формат файла сжатия аудио Musepack
linktitle: MPC
menu:
  docs:
    parent: "audio"
lastmod: 2021-03-28
---

## .MPC вариант №

Файл с расширением .mpc представляет собой формат аудиофайла [Musepack](https://musepack.net/), в котором используется сжатие звука с упором на высокое качество. Это позволяет вам даже не замечать различий в качестве звука исходного файла [WAV](/ru/audio/wav/) и сжатого файла MPC. Он использует алгоритмы MPEG-1 Layer-2 для достижения оптимизированного сжатия. Формат файла Musepack MPC является открытым исходным кодом с лицензией BSD/GNU LGPL. [Репозиторий SVN] (http://svn.musepack.net/) от Musepack позволяет получить последний обновленный код для кодека. Приложения, которые могут открывать файлы MPC, включают VLC Media Player, JetAudio и Winamp в дополнение к нескольким другим.

## Формат файла MPC

Файл MPC использует алгоритмы MPEG-1 Layer-2 для сжатия аудиофайлов. Это независимый от контейнера формат, который также позволяет кодировать исходный поток. Формат не использует внутреннюю обрезку и поддерживает потоковую передачу с точностью до семпла. Его пакетный поток позволяет мультиплексировать аудио- и видеоконтейнеры, такие как [MKV](/ru/video/mkv/).

## использованная литература

* [Musepack MPC — Википедия] (https://en.wikipedia.org/wiki/Musepack)
* [Musepack MPC] (https://musepack.net/)
