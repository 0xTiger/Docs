{
  "date" : "2021-26-08",
  "keywords" :[ "файл dcr", "формат файла dcr", "что такое файл dcr", "файл", "пример dcr", "расширение файла dcr", "расширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCR — файл изображения RAW цифровой камеры",
  "description":"Узнайте о формате файла DCR и API-интерфейсах, которые могут создавать и открывать файлы DCR.",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "identifier":"image-dcr",
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## .DCR вариант № ##
Файл с расширением dcr содержит содержимое цифровой фотографии, сохраненной в формате Kodak Digital Camera RAW (DCR). DCR — это сокращение от **Digital Camera Raw**; содержит несжатую и без потерь версию данных изображений, снятых цифровой камерой Kodak. Профессиональные фотографы любят использовать эти файлы, потому что они хранят изображения с более высоким качеством, чем форматы сжатых изображений низкого качества.

## Формат файла DCR
DCR — это собственный формат, разработанный компанией Eastman Kodak Company; называют просто Кодак. Файл изображения Digital Camera Raw (DCR) содержит минимально обработанные данные с датчика изображения цифровой камеры. Эти файлы еще не обработаны и поэтому не готовы к печати или редактированию в редакторе растровой графики.
Обычно преобразователь необработанных данных обрабатывает изображение во внутреннем цветовом пространстве с широкой гаммой, где точность и уточнение могут быть выполнены перед преобразованием в формат растрового файла, такой как TIFF или JPEG, для хранения, печати или дальнейшей обработки.
### Содержимое файла
Структура необработанных файлов часто следует общему шаблону:
- Короткий заголовок файла, который содержит индикатор порядка байтов в файле.
- Метаданные датчика камеры, необходимые для интерпретации данных изображения датчика, включая атрибуты CFA, размер датчика и его цветовой профиль.
- Метаданные изображения, которые могут быть полезны для включения в любую среду или базу данных CMS. Некоторые необработанные файлы содержат стандартизированный раздел метаданных с данными в формате Exif.
- Миниатюра изображения.
- Полноразмерное преобразование изображения в JPEG, которое используется для предварительного просмотра файла на ЖК-панели камеры.
- В случае сканирования кинопленки: временной код, ключевой код или номер кадра в файловой последовательности, представляющей последовательность кадров в отсканированном ролике.
- Данные изображения датчика
### Данные изображения датчика
Необработанный файл играет роль в цифровой фотографии, аналогичную роли фотопленки в пленочной фотографии. Таким образом, необработанные файлы содержат данные о полном разрешении, считанные с каждого пикселя датчика изображения камеры. На датчик камеры почти постоянно накладывается CFA (массив цветовых фильтров. Его можно использовать при преобразовании изображений с высоким динамическим диапазоном, когда доступны необработанные данные в формате; как более простую альтернативу подходу HDI с мультиэкспозицией для захвата трех отдельных изображений.


## Использованная литература ##

* [Формат необработанного изображения — Википедия] (https://en.wikipedia.org/wiki/Raw_image_format)
* [Что такое файл DCR] (https://expertphotography.com/dcr-file/)
