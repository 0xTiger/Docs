{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Файл EAZ - що таке файл EAZ і як його відкрити?",
  "description":"Дізнайтеся про формат файлу EAZ та API, які можуть створювати та відкривати файли EAZ.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-ukz"
}
},
  "lastmod" : "2023-12-23"
}

## Що таке файл EAZ?

Файл EAZ — це файл надбудови, який використовується ArcGIS Explorer, безкоштовною програмою, розробленою ESRI для дослідження карт, візуалізації та обміну. Він містить архів стисненого файлу, який містить [XML file](/web/xml/), скомпільований код і допоміжні файли, необхідні для надбудови. Ці файли використовуються для розширення базової функціональності програмного забезпечення шляхом додавання нових кнопок, закріплюваних вікон та інших розширень.

## Формат файлу EAZ - Додаткова інформація

Файли EAZ створюються за допомогою ArcGIS Explorer SDK, набору для розробки, розробленого для створення власних функцій у ArcGIS Explorer. Ці файли використовують стиснення [ZIP](/compression/zip/) для ефективного упаковування свого вмісту. В основі архіву файл **Addins.xml** знаходиться в кореневому каталозі, слугуючи життєво важливим компонентом, який описує та деталізує різноманітні налаштування, вбудовані у файл EAZ.

Файл Addins.xml по суті діє як дорожня карта, пропонуючи уявлення про конкретні вдосконалення, модифікації та розширення, які файл EAZ вводить в ArcGIS Explorer. Завдяки цій комплексній структурі розробники можуть інкапсулювати та легко інтегрувати нові функції, кнопки та закріплювані вікна, покращуючи загальну функціональність та досвід користувача програми ArcGIS Explorer.

## Список літератури

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)