{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Файл CUBE - Файл куба Гауса - Що таке файл .cube і як його відкрити?",
  "description" : "Дізнайтеся про файл куба Гауса та як його відкрити.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-uk-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Що таке файл CUBE?

Формат файлу CUBE, також відомий як файл куба Гауса (.cube), використовується в обчислювальній хімії для зберігання молекулярних даних, зокрема інформації про електронну густину, отриманої в результаті розрахунків квантової хімії. Цей формат зазвичай асоціюється з **пакетом програмного забезпечення Гауса**, який широко використовується для виконання розрахунків електронної структури ab initio.

Файли Gaussian Cube зберігають тривимірні дані, які зазвичай представляють електронну густину або інші властивості молекул, отримані за допомогою обчислень квантової хімії. Файл містить розділ заголовка з метаданими (такими як походження, кількість точок даних уздовж кожної осі та відстань), а потім таблицю числових значень, що представляють цікаву властивість (наприклад, густину електронів) у кожній точці сітки в просторі.

Файл куба Гауса (.cube) — це звичайний текстовий файл зі спеціальною структурою. Заголовок містить інформацію про молекулярну систему та сітку даних, а значення даних упорядковано у форматі тривимірної сітки. Файли Gaussian Cube часто використовуються для візуалізації молекулярних властивостей за допомогою програмного забезпечення для молекулярної візуалізації. Такі програми, як **VMD (Visual Molecular Dynamics)** або **PyMOL**, можуть читати файли куба Гауса, щоб відображати молекулярні поверхні, електронну густину чи інші обчислені властивості.

## Спрощений приклад файлу куба Гауса:

```
Приклад Cubefile
Створено Гауссом
   0 1 0 0 0 0 0 0 0 0
   0.0000000000000000E+00 0.0000000000000000E+00 0.0000000000000000E+00
  50 0,1000000000000000E+01 0,0000000000000000E+00 0,0000000000000000E+00
  50 0.0000000000000000E+00 0.1000000000000000E+01 0.0000000000000000E+00
  50 0.0000000000000000E+00 0.0000000000000000E+00 0.1000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (значення даних для електронної густини в кожній точці сітки)
```

## Про Гаусса

Gaussian — це набір програмних додатків для квантової хімії та комп’ютерної хімії. Основна увага Gaussian зосереджена на методах квантової хімії ab initio, які є високоточними, але обчислювально інтенсивними підходами до вивчення електронної структури молекул. Програмне забезпечення широко використовується в дослідницьких і академічних умовах для різних застосувань, зокрема для прогнозування молекулярних властивостей, вивчення механізмів реакцій і вивчення молекулярних структур.

## Про NWChem

NWChem — це програмне забезпечення для обчислювальної хімії з відкритим кодом, розроблене для високопродуктивного моделювання квантової хімії. Він використовує методи ab initio, такі як Хартрі-Фока та теорію функціоналу густини, підтримує паралельні обчислення для ефективних обчислень у кластерах і знаходить застосування в різноманітних наукових галузях, включаючи обчислювальну хімію, біохімію та матеріалознавство. NWChem відомий своєю універсальністю, що дозволяє дослідникам вивчати різні хімічні системи, а його природа з відкритим кодом заохочує внески спільноти та налаштування.

## Про VMD

VMD, що означає Visual Molecular Dynamics, є потужною та широко використовуваною програмою молекулярної візуалізації для відображення, аналізу та анімації траєкторій молекулярної динаміки (MD), а також статичних молекулярних структур. Він особливо популярний у сферах обчислювальної хімії, молекулярної біології та структурної біоінформатики. VMD відмінно підходить для візуалізації молекулярних структур, забезпечуючи високоякісну 3D-візуалізацію молекул і молекулярних комплексів. Він підтримує різні формати молекулярних файлів.

## Про PyMOL

PyMOL — це система молекулярної візуалізації та програмний інструмент, який використовується для тривимірної візуалізації молекулярних структур. Він особливо популярний у сферах структурної біології, біоінформатики та обчислювальної хімії. PyMOL забезпечує високоякісну 3D-візуалізацію молекулярних структур, що дозволяє користувачам візуалізувати та досліджувати форми, поверхні та взаємодії біологічних макромолекул.

## Як відкрити файл CUBE?

CUBE файл можна відкрити та посилатися на нього за допомогою наступних програм.

- **NWChem** (безкоштовно) для (Windows, MAC, Linux)

## Посилання
* [Формат файлу куба Гауса](https://paulbourke.net/dataformats/cube/)