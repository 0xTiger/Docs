{
"дата": "27.09.2023",
  "keywords": [
"кфг",
"cfg-файл",
"cfg файл языка разметки wesnoth",
"что такое файл cfg",
"как открыть файл cfg",
"файл",
"расширение файла cfg",
"расширение"
],
  "author": {
"display_name": "Шакил Фаиз"
},
"draft": "false",
"toc": true,
"title": "Формат файла CFG — файл языка разметки Wesnoth",
  "description":"Узнайте о формате файлов языка разметки CFG Wesnoth и API-интерфейсах, которые могут создавать и открывать файлы CFG.",
"linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
"parent": "game"
}
},
"lastmod": "27.09.2023"
}

## .CFG вариант №

Файл CFG также известен как **"Язык разметки Wesnoth" (WML)**. Это специальный язык разметки, используемый в основном в игре «Battle for Wesnoth», которая представляет собой пошаговую стратегическую игру. WML используется для определения и настройки различных аспектов игры, включая сценарии, кампании, юниты и многое другое. Это способ для моддеров и разработчиков создавать контент для игры.

Он написан в формате, напоминающем комбинацию XML и простых сценариев. Вот обзор некоторых общих элементов и структур, которые вы можете найти в файле WML:

1. **Теги.** WML использует теги для определения различных элементов игры. Теги заключаются в угловые скобки. Например:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Атрибуты.** В тегах вы можете определить атрибуты, чтобы указать свойства или значения, связанные с элементом. В приведенном выше примере «тип» и «поинты жизни» являются атрибутами.
    










3. **Массивы и массивы массивов:** Вы можете создавать массивы данных и даже массивы массивов для определения списков юнитов, типов местности или других игровых элементов.
    










4. **Условные операторы.** WML поддерживает условные операторы для управления ходом игры. Например:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Циклы.** Циклы можно использовать для перебора списков элементов или многократного выполнения действий.
    










6. **Включает:** Вы можете включать другие файлы WML в основной файл WML для организации и модульного представления вашего контента.
    










7. **Обработчики событий.** Вы можете определить обработчики событий, которые будут запускать действия при возникновении определенных событий в игре.
    











Вот упрощенный пример файла WML, который определяет пользовательскую единицу измерения:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## Битва за Веснот

«Битва за Веснот» — популярная пошаговая стратегическая игра с открытым исходным кодом. Он доступен для нескольких платформ, включая Mac, Windows, Linux и другие. Игра, разработанная преданным сообществом добровольцев, известна своим глубоким и увлекательным игровым процессом, а также богатым фэнтезийным миром.

Ключевые особенности «Битвы за Веснот» включают в себя:

1. **Сеттинг в стиле фэнтези.** Действие игры разворачивается в фантастическом мире с участием различных рас, включая людей, эльфов, гномов, орков и многих других. История и повествование игры являются неотъемлемой частью ее привлекательности.
    










2. **Пошаговая стратегия.** Геймплей пошаговый, в котором игроки не торопятся планировать и выполнять свои действия на шестиугольных сетках. Он сочетает в себе тактический бой с принятием стратегических решений.
    










3. **Кампании.** В игре представлен широкий выбор одиночных кампаний, каждая из которых имеет свою собственную сюжетную линию, персонажей и испытания. Игроки могут исследовать различные повествования и сценарии.
    










4. **Мультиплеер:** «Веснот» поддерживает многопользовательский режим онлайн, позволяя игрокам соревноваться друг с другом в стратегических битвах. Многопользовательские режимы включают совместную игру и соревновательные матчи.

## Как открыть файл CFG?

Файлы CFG, которые обычно связаны с языком разметки Wesnoth (WML), используемым в игре «Битва за Веснот», можно легко редактировать с помощью любого стандартного текстового редактора. Эти файлы содержат удобочитаемый код, написанный на WML, который определяет различные аспекты игры, включая сценарии, юниты и кампании.

Хотя для изменения файлов CFG можно использовать любой текстовый редактор, в некоторых продвинутых текстовых редакторах, таких как Emacs и Vi, доступны плагины для подсветки синтаксиса WML. Эти плагины обеспечивают полезное цветовое кодирование и форматирование, чтобы пользователям было легче различать различные элементы и структуры в коде WML.

Программы, которые открывают файлы CFG или ссылаются на них, включают в себя

- Битва за Веснот (бесплатно) для (Windows, MAC, Linux)
- Блокнот Майкрософт

## Другие файлы CFG

Ниже приведены другие типы файлов, использующие расширение **.cfg**.

**Настройки**
- [CFG - Файл конфигурации Celestia](/ru/settings/cfg-celestia/)
- [CFG — файл подключения к серверу Citrix](/ru/settings/cfg-citrix/)
- [CFG - Файл конфигурации MAME](/ru/settings/cfg-mame/)
- [CFG — Файл конфигурации LightWave](/ru/settings/cfg-lightwave/)

**Игра**
- [CFG — файл языка разметки Wesnoth](/ru/game/cfg-wesnoth/)
- [CFG - Файл конфигурации MUGEN](/ru/game/cfg-mugen/)
- [CFG — файл конфигурации исходного движка](/ru/game/cfg-sourceengine/)

**Система и прочее**
- [CFG - Файл CFG](/ru/system/cfg/)
- [CFG — файл конфигурации модели Cal3D](/ru/misc/cfg-cal3d/)

## Рекомендации
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)