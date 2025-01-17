{
  "date" : "2019-10-11",
  "keywords" :[ "файл kmz", "що таке файл kmz", "файл", "приклад kmz", "розширення файлу kmz", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - формат архівованого файлу KML",
  "description":"Дізнайтеся про формат файлу KMZ та API, які можуть створювати та відкривати файли KMZ.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл KMZ?

Файл KMZ (KML Zipped) — це представлення заархівованого файлу [KML](/uk/gis/kml/), який містить геопросторову інформацію, доступну для перегляду в програмах ГІС, як-от Google Earth. Інформація про позначки місця представлена у файлі як широта та довгота разом із настроюваною назвою. Єдиним упакованим файлом KMZ можна легко поділитися з іншими користувачами. Файли KMZ можуть містити дані 3D-моделі, а також для географічного представлення моделі. Файл KMZ можна відкрити в Картах Google, зберігши файл в онлайн-розташуванні та ввівши URL-адресу в поле пошуку Карт Google.

## Структура файлу ##

Вміст файлу MKZ складається з основного файлу KML і нуля чи більше пов’язаних файлів. Його можна розпакувати за допомогою стандартної утиліти декомпресії, наприклад WinZIP. Формат файлу KMZ також стискається в архів із коефіцієнтом стиснення 10:1. Ви можете експортувати дані з програми Google Планета Земля безпосередньо у формат файлу KMZ. Основний файл KML має назву **doc.kml**. Під час пакування файлу KMZ до нього можна додати більше одного файлу KML, але це не принесе користі, оскільки Google Планета Земля шукає перший файл KML під час відкриття файлу KMZ і зчитує його. Він ігнорує будь-які інші файли KML, знайдені в архіві. Щоб переконатися, що Google Earth читає потрібний файл KML, у файл KMZ рекомендується розміщувати лише один файл KML.

Зображення, моделі, текстури, звукові файли та інші ресурси, на які посилається файл doc.kml, розміщуються в іншій вкладеній папці всередині основної папки. Це також може бути складним, залежно від кількості допоміжних файлів. Посилання на ці складові ресурси можуть бути відносними посиланнями або через абсолютні посилання.

### Відносне посилання ###

Коли ресурси розміщуються поруч із основним doc.kml у підпапці в межах основної папки, відносне посилання може вказувати на ці допоміжні файли, як показано в наступному прикладі (лише для значка).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Абсолютне посилання ###

Абсолютно також можна посилатися на ресурси. Абсолютні посилання містять повну URL-адресу пов’язаного файлу. Коли файли розміщуються на центральному сервері, абсолютне посилання гарантує, що вони залишаються однозначними порівняно з відносним посиланням. Категорично не рекомендується посилатися на локальний файл, оскільки ці посилання розірвуться під час переміщення файлів до нової системи. Приклад абсолютного посилання такий:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Дивіться також ##

* [GeoJSON](/uk/gis/geojson/)

## Посилання ##

* [Файли Google Earth і KMZ](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

