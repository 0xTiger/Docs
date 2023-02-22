{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу PDB - файл бази даних програми",
  "description":"Дізнайтеся про формат файлу PDB та API, які можуть створювати та відкривати файли PDB.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Що таке файл PDB?

Файл із розширенням .pdb — це файл бази даних програми, який містить інформацію про налагодження скомпільованого виконуваного файлу (EXE/DLL). Файли PDB генеруються компіляторами Microsoft, коли прикладна програма компілюється в режимі налагодження. Наявність файлу PDB може допомогти у зворотному проектуванні виконуваного файлу, оскільки він містить значну інформацію про всі символи модулів. Саме з цієї причини ці файли зберігаються окремо від остаточного виконуваного файлу. Microsoft [API DgbHelp](https://docs.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) може відкрити файл PDB, щоб отримати таку інформацію, як загальнодоступні та експортовані, глобальні символи, локальні символи, тип даних, вихідні файли та номери рядків.

## Формат файлу PDB

PDB — це власний формат файлу Microsoft, який ще ніде офіційно не задокументований. Однак початкова документація доступна [тут](https://github.com/Microsoft/microsoft-pdb), і на неї можна посилатися.

### Потоки PDB

Файли PDB складаються з кількох потоків, де кожен потік діє як окремий віртуальний файл і містить інформацію. Автори файлів PDB можуть писати в ці файли, і файл завершується лише після явного фіксації. Компілятор може продовжувати запис у файл PDB, але фіксувати, лише якщо весь код користувача буде успішно скомпільовано. Файл PDB складається з таких потоків:

|№ потоку |Зміст |Короткий опис|
---|---|---|
|1| Pdb (заголовок) |Інформація про версію та інформація для підключення цього PDB до EXE|
|2| Tpi (Менеджер типів) |Усі типи, що використовуються у виконуваному файлі.|
|3| Dbi (інформація про налагодження) |Зберігає внески розділу та список «Модів»|
|4| NameMap| Зберігає хешовану таблицю рядків|
|4-(n+4)| n Mod's (інформація про модуль)| Кожен потік Mod містить символи та номери рядків для однієї компіляції|
|n+4| Глобальний хеш символу| Індекс, що дозволяє здійснювати пошук у глобальних символах за назвою|
|n+5| Загальнодоступний хеш символу| Індекс, що дозволяє здійснювати пошук у публічних символах за адресами|
|n+6| Символьні записи| Актуальні символьні записи глобальних і публічних символів|
|n+7| Введіть hash| Хеш, який використовується потоком TPI.|

Кожен потік у файлі PDB складається з кількох сторінок, які не обов’язково мають послідовну нумерацію.

### Заголовок PDB

Файл PDB має заголовок, який складається з підпису для ідентифікації та підтвердження певного формату. Довжина підпису залежить від формату PDB. Заголовок може бути довшим за одну сторінку.

### Метадані PDB
Метадані PDB відповідають за розпізнавання всіх потоків компонентів, надаючи довжину та послідовність сторінок для кожного потоку. Накази віддаються потокам послідовно; починаючи з 0. Існує також невпорядкований кореневий потік, який містить деякі метадані.

## Список літератури
* [PDB – Вікіпедія](https://en.wikipedia.org/wiki/Program_database)
* [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)
