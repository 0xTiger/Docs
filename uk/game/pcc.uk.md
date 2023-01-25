{
  "date" : "2021-09-08",
  "keywords" :[ "файл pcc", "формат файлу pcc", "що таке файл pcc", "файл", "приклад pcc", "розширення файлу pcc", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу PCC Mass Effect та API, які можуть створювати та відкривати файли PCC.",
  "title" :"PCC - файл пакета Mass Effect",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Що таке файл PCC?

Файл із розширенням .pcc — це файл [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3), який містить дані гри для зміни вмісту гри, як-от моделі, текстури та кімнати. Mass Effect 2 і 3 — це перші шутери, засновані на ігровому двигуні Unreal Engine 3. Гру спочатку розробила [Bioware](https://www.bioware.com/about/), яка зберігала більшість ігрових ресурсів у своєму власному форматі файлу PCC. Компанія Bioware була придбана Electronic Arts, провідним світовим видавцем інтерактивних розваг.

## Формат файлу PCC - Додаткова інформація

Файли PCC містять стиснені та/або нестиснені структури, які сприяють загальній організації файлів.

### Стиснута структура PCC

Стислий PCC-файл складається з таблиць і даних, сегментованих на фрагменти. Кожен фрагмент містить змінну кількість стиснутих блоків.

* `Заголовок фрагментів` - 16-байтовий загальний заголовок, що містить інформацію про блоки.
* `Chunk Header` - 16-байтовий заголовок, що містить інформацію про необроблені стиснені дані, що містяться у формі блоку.

### Структура PCC без стиснення

Нестиснуті файли PCC поділяються на наступні п'ять частин.

* `Заголовок` - містить основну інформацію про структуру файлу PCC.
* `Таблиця імен` - містить назву, знайдену всередині пакета, включаючи класи імпорту, експорт і властивості експорту.
* `Таблиця імпорту` - містить усі класи та об'єкти, імпортовані PCC.
* `Таблиця експорту` - містить усі об'єкти, що зберігаються в пакеті. Кожен експорт може відрізнятися за розміром.

## Список літератури

* [Me3Explorer - формат файлу PCC](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Гра Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)
