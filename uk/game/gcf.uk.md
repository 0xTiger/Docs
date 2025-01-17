{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу GCF та API, які можуть створювати та відкривати файли GCF.",
  "title" : "Файл GCF – формат гри Nadeo GCF",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-uk",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## Що таке файл GCF?

Файл .gcf — це файл кешу гри, який використовується ігровою платформою Steam. Він містить дані гри, такі як текстури, моделі та інші файли, які використовуються грою. Ці файли зберігаються на комп’ютері користувача та використовуються для зменшення обсягу даних, які необхідно завантажити під час оновлення або встановлення гри. Файли .gcf також можна використовувати для створення резервних копій інсталяції гри або перенесення гри між комп’ютерами.

Файли GCF можна читати та записувати за допомогою бібліотеки програмування C++ з відкритим кодом, **HLLib**.

## Формат файлу GCF

Файли GCF зберігаються на диску як двійкові файли. GCF спочатку використовувався як абревіатура Grid Cache File (рання кодова назва Steam була Grid), але пізніше його було прийнято як Game Cache File. Файл GCF — це архівний файл, у якому зберігаються ігри Steam. Весь офіційний вміст завантажується як файли GCF. Файли GCF також можна обмінювати між іграми.

ПРИМІТКА. GCF є попередником [VPK file format](/game/vpk/).
## Список літератури

* [Програмне забезпечення Valve](https://www.valvesoftware.com/en/)

* [Формат файлу GCF](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib – бібліотека програмування C++ з відкритим кодом для читання файлів GCF](https://developer.valvesoftware.com/wiki/HLLib)


