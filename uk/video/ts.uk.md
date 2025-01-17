{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу TS – файл транспортного потоку відео",
  "keywords" :[ "ts", "flie", "extension", "extension", ".ts", "format" ],
  "description":"Дізнайтеся, що таке файл TS та API, які можуть створювати та відкривати файли TS.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## Що таке файл TS?

Файл із розширенням .ts — це відеопотік, який зберігає дані на DVD-дисках. Він використовує алгоритм стиснення MPEG-2 ([.mpeg](/uk/video/mpg/)), щоб досягти максимальної ефективності та сумісності з різними типами медіа, такими як потокове передавання в Інтернеті та трансляція. Формат файлу TS створено для того, щоб його можна було відтворювати на пристроях із поганим з’єднанням з Інтернетом, таких як Smart TV.

## Формат файлу TS – Додаткова інформація

Дані у файлі TS подібні до файлу [MP4](/uk/video/mp4/), але вони поділені на крихітні фрагменти. Кожна частина складається з крихітного фрагмента відео, за яким слідує фрагмент аудіо та необов’язковий підпис. Один файл TS складається з багатьох таких блоків. Окрім відео, аудіо та субтитрів, кожен фрагмент також містить деякі додаткові дані для виявлення помилок у фрагменті. Через це файли TS дещо більші за розміром.

### Навіщо використовувати формат файлу TS?

Отже, якщо файли TS дещо великі за розміром, яку перевагу пропонує використовувати їх замість інших форматів файлів? Що ж, у трансляції крихітні фрагменти відео та аудіо можна надсилати через засоби зв’язку (дротяні чи радіо) у режимі реального часу. Додаткові дані в блоках використовуються одержувачем для пропуску схильних до помилок блоків.

Крім того, використовуються файли TS, оскільки системі трансляції не потрібен весь потік для його відтворення. Передачу можна підібрати та використовувати в режимі реального часу, зібравши аудіо та відео.

## Як відтворювати файли TS?

Файли TS можна відкривати та відтворювати в популярному [VideoLAN VLC media player](https://www.videolan.org/vlc/features.html), який можна безкоштовно завантажити.

## Посилання ##

* [Транспортний потік MPEG – Вікіпедія](https://en.wikipedia.org/wiki/MPEG_transport_stream)

