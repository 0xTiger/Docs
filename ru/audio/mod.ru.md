{
  "date" : "2021-08-04",
  "keywords" :[ "мод", "mp3", "файл", "расширение", "формат", "что такое формат файла мода", "музыка", "формат файла мода", "мод против MP3", "спецификация формата файла мода "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файла MOD и API-интерфейсах, которые могут создавать, конвертировать и открывать файлы MOD.",
  "title" :"MOD - файл музыкального модуля",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## .MOD вариант №
Файл с расширением .mod представляет собой файл музыкального модуля, созданный с использованием стандартного формата музыкального модуля, который основан на **формате модуля Amiga**, разработанном Карстеном Обарски и выпущенном с программным обеспечением **Ultimate Soundtracker** для Commodore. Система Амига. Подобно файлу [MIDI](/ru/audio/mid/), он состоит из образцов нот и звуковых образцов, представляющих различные инструменты, которые воспроизводятся в соответствии с нотами. Файлы MOD особенно часто используются в видеоиграх в качестве фоновой музыки и в субкультуре **демосцены** компьютерного искусства.

## Формат файла MOD

MOD — это компьютерный формат файла, основная функция которого заключается в представлении музыки, и это был первый модульный формат файла. Файлы MOD используют расширение файла .mod, за исключением **Amiga**, которая считывает заголовок файла для определения типа файла, поэтому он не зависит от расширений имени файла. Файл MOD состоит из набора различных инструментов в виде сэмплов, ряда паттернов, указывающих, как и когда сэмплы должны воспроизводиться, и списка паттернов, которые нужно воспроизводить в каком порядке.

### Спецификации формата файла MOD

Шаблон файла MOD фактически разработан в пользовательском интерфейсе секвенсора в виде таблицы с одним столбцом на канал. Таким образом, эта таблица имеет четыре столбца (по одному на каждый аппаратный канал Amiga. В каждом столбце 64 строки).

Ячейка в таблице может вызвать одно из следующих действий в канале своего столбца, когда достигнуто время его строки:

- Запустить инструмент, играющий новую ноту в этом канале с заданной громкостью, возможно, с применением к нему специального эффекта.
- Измените громкость или специальный эффект, применяемый к текущей ноте.
- Изменение схемы потока; перейти к определенной позиции песни или паттерна или зациклиться внутри паттерна
- Ничего не делать; любая существующая нота, играющая в этом канале, будет продолжать играть

Инструмент представляет собой отдельный семпл вместе с необязательным указанием того, какая часть семпла может быть повторена, чтобы содержать твердую ноту.

### Сроки
Минимальный временной интервал составлял 0,02 секунды в исходном файле MOD или интервал «вертикального гашения» (VSync), поскольку исходное программное обеспечение использовало синхронизацию VSync монитора, работающего с частотой 50 Гц (для PAL) или 60 Гц (для NTSC). для тайминга.

## использованная литература

* [MOD (формат файла) - По Википедии] (https://en.wikipedia.org/wiki/MOD_(формат_файла))
