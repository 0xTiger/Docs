{
"дата":"20.07.2023",
   "keywords":[
"БІН",
"Файл BIN",
"файл",
"Розширення файлу BIN",
"розширення",
"файл"
],
   "author":{
"display_name":"Шейкіл Фаїз"
},
"чернетка":"хибний",
"toc":true,
"title":"Формат файлу BIN - файл у кодуванні MacBinary",
   "description":"Дізнайтеся про формат BIN та API, які можуть створювати та відкривати файли BIN.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
         "parent":"compression"
}
},
"lastmod":"20.07.2023"
}

## Що таке файл BIN?

Файл BIN у контексті комп’ютерів Macintosh може стосуватися файлу, збереженого у форматі MacBinary. MacBinary — це формат файлів, спеціально розроблений для передачі файлів Macintosh через Інтернет, електронну пошту, FTP або портативні носії. Метою MacBinary є збереження повної файлової структури та атрибутів файлів Macintosh, включаючи як відгалуження даних, так і відгалуження ресурсів, в одному файлі.

Формат MacBinary досягає цього шляхом інкапсуляції відгалуження ресурсів ієрархічної файлової системи Macintosh (HFS) і відгалуження даних у стиснутий файл. Він також містить заголовок пошуку, який містить важливі метадані про файл. Об’єднавши всі ці компоненти в один файл, MacBinary гарантує, що файл збереже свою цілісність і його можна легко передавати та спільно використовувати на різних платформах.

З удосконаленням файлових систем Apple і протоколів передачі файлів використання файлів BIN і формату MacBinary стало менш поширеним. Поява таких форматів файлів, як ZIP, і перехід до більш сучасних файлових систем, таких як HFS+ і APFS, зменшили потребу у файлах, закодованих MacBinary. Ці нові файлові системи забезпечують ефективніші способи обробки атрибутів файлів, розгалужень ресурсів і даних, що робить формат MacBinary менш потрібним у сучасному комп’ютерному ландшафті.

## Формат файлу BIN - Додаткова інформація

На початку комп’ютерів Macintosh файли зберігалися в двох окремих "форках" через обмеження даних. "Вилка ресурсів" містила структуровані дані, тоді як "вилка даних" містила неструктуровані дані. У той час як класична Mac OS розглядала ці розгалуження як один файл, передача файлів на системи, відмінні від Mac, призводила до втрати даних, оскільки вони не розпізнавали розгалуження як одну сутність. Щоб вирішити цю проблему, такі особи, як брати Денніс, Гаррі Чеслі та Ів Лемперьор, створили формат MacBinary. MacBinary стиснув і об’єднав розгалуження в один файл, відомий як файл BIN, для передачі в системи, відмінні від Mac. Після повернення до Mac OS форки знову будуть розділені. З переходом від HFS на основі форка у 2000-х роках використання формату MacBinary значно скоротилося. Сьогодні файл BIN, закодований MacBinary, трапляється рідко, якщо ви не натрапите на старий файл у системі, відмінній від Mac, або не завантажите його з Інтернету.

Формат MacBinary з часом пройшов кілька версій, щоб врахувати зміни в системах Macintosh і обробці файлів. Ось кілька різних версій формату MacBinary:

- **MacBinary I:** початкова версія MacBinary, представлена наприкінці 1980-х років. Він об’єднав форк ресурсів і форк даних в єдиний бінарний файл, дозволяючи передавати файли Macintosh між платформами.

- **MacBinary II:** Ця версія, випущена на початку 1990-х років, покращила оригінальний формат MacBinary, додавши до заголовка двійкового файлу додаткову інформацію, таку як тип файлу та коди творця. Ці коди допомогли зберегти цілісність та ідентифікацію файлів Macintosh під час передачі.

- **MacBinary III:** Формат MacBinary III, представлений у середині 1990-х років, ще більше вдосконалив попередні версії, включивши додаткові метадані, такі як ім’я файлу та дати створення та модифікації файлу, у заголовок двійкового файлу. Це дозволило більш повно зберегти атрибути файлів Macintosh під час перенесення.

- **MacBinary IV:** MacBinary IV було розроблено для вирішення проблем сумісності з новою операційною системою Mac OS X на початку 2000-х років. Він містить зміни для адаптації до нової структури файлової системи та атрибутів, представлених у Mac OS X.

## Як відкрити файл BIN?

Файли MacBinary Encoded BIN можна відкривати за допомогою різних утиліт стиснення. Для користувачів macOS підходящим варіантом є **Apple Archive Utility**. Користувачі Windows можуть використовувати таке програмне забезпечення, як **Smith Micro StuffIt Deluxe**, щоб видобути вміст файлу MacBinary Encoded BIN. Іншим варіантом для користувачів macOS є **The Unarchiver**, який є універсальним інструментом, здатним працювати з кількома форматами файлів, включаючи MacBinary.

Важливо зауважити, що розширення файлу .bin використовується різними форматами файлів, а не лише MacBinary. Тому, якщо ви зіткнетеся з BIN-файлом, який неможливо відкрити за допомогою вищезгаданих утиліт, він може бути збережений в іншому форматі. У таких випадках вам може знадобитися визначити конкретний формат файлу та скористатися відповідним програмним забезпеченням або утилітою, розробленою для цього формату, щоб отримати доступ до вмісту файлу.

## Інші файли BIN

Ось інші типи файлів, які використовують розширення **.bin**.

- [BIN - двійковий файл образу диска](/uk/disc-and-media/bin/)
- [BIN - Виконуваний файл Unix](/uk/executable/bin/)
- [BIN - файл політики IT BlackBerry](/uk/settings/bin/)
- [BIN - Sega Genesis Game ROM](/uk/game/bin/)
- [BIN - Образ BIOS PSX PlayStation](/uk/game/bin-pcsx/)

## Список літератури

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

