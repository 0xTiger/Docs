{
  "date" : "2021-10-20",
  "keywords" :[ ".pak", "формат файлу", "що таке файл pak", "файл", "приклад pak", "файл пакету відеоігор", "розширення"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про файл .pak і API, які можуть створювати та відкривати файли PAK.",
  "title" :"Формат файлу PAK – файл пакету відеоігор",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Що таке файл PAK?

Файл PAK — це файл пакета, створений різними відеоіграми для архівування даних гри. По суті, це формат файлу гри. Це може включати кілька ігрових елементів, таких як графіка, текстури, звуки, об’єкти та інші ігрові дані. Архів здебільшого зберігається як файл .zip і може бути розпакований за допомогою популярного програмного забезпечення для декомпресії, такого як WinZip і WinRAR. Приклади відеоігор, у яких використовуються файли PAK, включають Quake, Hexen, Crysis і Half-Life.

## Формат файлу PAK – додаткова інформація

У більшості випадків файли PAK зберігаються у [форматі файлу ZIP](/uk/стиснення/zip/). Але різні програми можуть використовувати різні формати файлів для зберігання цих файлів.


## Як відкрити файли PAK?

Файли PAK можна відкрити за допомогою таких програм, як [PakExplorer](https://www.quaketerminus.com/tools.shtml) і [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------ -------------------------------------------------- ----------------------**

## Формат файлу PAK – об’єктний файл Simutrans

Файл із розширенням .pak — це формат файлу гри для симуляції транспорту [Simutrans](https://www.simutrans.com/en/). Він містить об’єкти, які використовуються в симуляції, наприклад створені користувачем графіки та вміст даних. Він може містити кілька різних об’єктів, наприклад ігрові транспортні засоби, будівлі, рельєф тощо. Файли PAK генеруються за допомогою MakeObject, утиліти, яка компілює файли .dat і зображення .png для створення цих об’єктів моделювання. Simutrans дозволяє гравцям керувати успішною транспортною системою, будуючи та керуючи транспортними системами для пасажирів, пошти та товарів наземним транспортом

## Як створити файли PAK?

Simutrans навів приклади створення файлів PAK в ОС Windows і Linux.

### ОС Windows

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Список літератури

* https://simutrans-germany.com/wiki/wiki/en_doPak
* https://en.wikipedia.org/wiki/Simutrans
