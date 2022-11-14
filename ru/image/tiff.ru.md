{
  "date" : "2019-10-11",
  "keywords" :[ "файл tiff", "формат файла tiff", "что такое файл tiff", "файл", "пример tiff", "расширение файла tiff", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF — формат файла изображения",
  "description":"Узнайте о формате файлов TIFF и API-интерфейсах, с помощью которых можно создавать и открывать файлы TIFF.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .TIFF вариант №

TIFF или TIF, Tagged Image File Format, представляет собой растровые изображения, которые предназначены для использования на различных устройствах, соответствующих этому стандарту формата файлов. Он способен описывать двухуровневые, полутоновые, палитры и полноцветные данные изображения в нескольких цветовых пространствах. Он поддерживает схемы сжатия с потерями, а также без потерь, чтобы выбирать между пространством и временем для приложений, использующих формат. Формат не зависит от машины и свободен от ограничений, таких как процессор, операционная система или файловые системы.

## Краткая история формата файлов TIFF

Формат файла TIFF был первоначально создан корпорацией Aldus осенью 1986 года после серии встреч с различными производителями сканеров и разработчиками программного обеспечения. Основная цель формата файла TIFF заключалась в том, чтобы предоставить общий формат файла отсканированного изображения для всех поставщиков настольных сканеров. Начиная с поддержки только двоичного формата изображения, формат со временем превратился в поддержку изображений в градациях серого и цветных изображений. Первоначальная версия спецификаций формата файла TIFF может быть обозначена как Reivision 3.0, так как было два более ранних черновых выпуска. В 1988 году была опубликована основная версия 5.0, в которой добавлена поддержка изображений с цветовой палитрой и сжатие LZW. Версия 6.0 форматов файлов TIFF была опубликована в 1992 году после этого. В 1994 году Adobe Systems приобрела Aldus, и теперь спецификации доступны и поддерживаются Adobe Systems.

## Спецификации формата файла TIFF

Формат файла TIFF является расширяемым и претерпел несколько изменений, что позволяет включать неограниченное количество частной или специальной информации. Файл TIFF начинается с 8-байтового заголовка, где байты — это числа от 0 до N. Максимально возможный файл TIFF имеет длину 2**32 байта. Файл начинается с 8-байтового заголовка файла изображения, который указывает непосредственно на файл изображения (IFD). IFD содержит информацию об изображении, а также указатели на фактические данные изображения.

### Заголовок файла TIFF

8-байтовый заголовок файла TIFF содержит следующую информацию:

**Байты 0-1:** Порядок байтов, используемый в файле. Допустимые значения: «II» (4949.H) «MM» (4D4D.H).

В формате «II» порядок байтов всегда от младшего значащего байта до самого старшего байта как для 16-битных, так и для 32-битных целых чисел. Это называется порядком байтов с прямым порядком байтов. В формате «MM» порядок байтов всегда от старшего к младшему как для 16-битных, так и для 32-битных целых чисел. Это называется порядком байтов с прямым порядком байтов.

**Байты 2-3:** Произвольное, но тщательно выбранное число (42), которое дополнительно идентифицирует файл как файл TIFF. Порядок байтов зависит от значения байтов 0-1.

**Байты 4-7:** Смещение (в байтах) первого IFD. Каталог может находиться в любом месте файла после заголовка, но должен начинаться на границе слова. В частности, каталог файлов изображений может следовать за данными изображения, которые он описывает. Читатели должны следовать указателям, куда бы они ни вели. Термин «байтовое смещение» всегда используется в этом документе для обозначения положения относительно начала файла TIFF. Первый байт файла имеет смещение 0.

### Каталог файлов изображений

IFD содержит информацию об изображении, а также указатели на фактические данные изображения. Он состоит из 2-байтового подсчета количества записей каталога (т. е. количества полей), за которым следует последовательность 12-байтовых записей полей. , за которым следует 4-байтовое смещение следующего IFD (или 0, если его нет). В файле TIFF должен быть как минимум 1 IFD, и каждый IFD должен иметь хотя бы одну запись.

#### Запись ИФД

Каждая 12-байтовая запись IFD имеет следующий формат.


|Байты|Описание
---|---|
|0-1|Тег, идентифицирующий поле
|2-3|Тип поля
|4-7|Счетчик указанного типа
|8-11|Смещение значения, смещение в файле (в байтах) значения поля. Предполагается, что значение начинается на границе слова; соответствующее смещение значения, таким образом, будет четным числом. Это смещение файла может указывать в любом месте файла, даже после того, как данные изображения

Поле TIFF представляет собой логический объект, состоящий из тега TIFF и его значения. Эта логическая концепция реализуется как запись IFD, плюс фактическое значение, если оно не помещается в часть значения/смещения, последние 4 байта записи IFD. Термины «поле TIFF» и «запись IFD» взаимозаменяемы в большинстве контекстов.

### Базовый TIFF ###

Базовый формат TIFF — это ядро TIFF, основные элементы, которые все основные разработчики TIFF должны поддерживать в своих продуктах. Соответствие формату TIFF зависит от соблюдения базовых требований TIFF. Эти требования хорошо документированы в документе спецификаций 6.0.

#### Несколько изображений в файле ####

В файле TIFF может быть более одного IFD. Каждый IFD определяет подфайл. Одним из возможных вариантов использования подфайлов является описание связанных изображений, таких как страницы факсимильного сообщения. Базовый считыватель TIFF не требуется для чтения каких-либо IFD, кроме первого.

#### Типы изображений ####

Базовое изображение TIFF имеет следующие типы:

**Двухуровневое.** Двухуровневое изображение содержит два цвета — черный и белый. TIFF позволяет приложению записывать двухуровневые данные в формате «белое — ноль» или «черное — ноль». Поле, которое записывает эту информацию, называется **Фотометрическая интерпретация**.

* Полноцветный RGB

Информация PhotometricInterpretation для изображений Bilevel выглядит следующим образом:

Тег = 262 (106.H)
Тип = КОРОТКИЙ
**Ценности**

|Значение|Описание|
---|---|
|0|Для двухуровневых изображений и изображений в градациях серого: 0 отображается как белый. Максимальное значение отображается черным цветом. Это нормальное значение для Compression#2|
|1|ЧерныйНоль. Для двухуровневых изображений и изображений в градациях серого: 0 отображается как черный. Максимальное значение отображается белым цветом. Если это значение указано для Compression#2, изображение должно отображаться и печататься в перевернутом виде.|

**Оттенки серого:** Изображения в градациях серого представляют собой обобщение двухуровневых изображений. Двухуровневые изображения могут хранить только данные черно-белого изображения, но изображения в градациях серого также могут хранить оттенки серого. Для описания таких изображений необходимо добавить или изменить следующие поля. Другие обязательные поля такие же, как и для двухуровневых изображений. Для изображений в градациях серого используйте Compression # 1 или 32773 (PackBits). В Baseline TIFF изображения в градациях серого могут храниться как несжатые данные или сжиматься с помощью алгоритма PackBits.

Информация **BitsPerSample** для изображений в градациях серого выглядит следующим образом:

Тег = 258 (102.H)
Тип = КОРОТКИЙ

Количество битов на компонент. Допустимые значения для изображений в градациях серого Baseline TIFF: 4 и 8, что позволяет использовать 16 или 256 различных оттенков серого.

**Цветовая палитра:** изображения с цветовой палитрой аналогичны изображениям в градациях серого. У них по-прежнему есть один компонент на пиксель, но значение компонента используется в качестве индекса в полной таблице поиска RGB. Для описания таких изображений необходимо добавить или изменить следующие поля. Остальные обязательные поля такие же, как и для изображений в градациях серого.
Информация PhotometricInterpretation для изображения Palette-Color выглядит следующим образом:

Фотометрическая интерпретация = 3 (цветовая палитра).
ColorMapTag = 320 (140.H)
Тип = КОРОТКИЙ
N = 3 * (2 бита на выборку)

Это поле определяет цветовую карту «красный-зеленый-синий» (часто называемую таблицей поиска) для цветовых изображений палитры. В изображении с цветовой палитрой значение пикселя используется для индексации в таблице преобразования RGB. Например, пиксель цвета палитры, имеющий значение 0, будет отображаться в соответствии с 0-м триплетом «Красный, Зеленый, Синий». В ColorMap черный представлен 0,0,0, а белый представлен 65535, 65535, 65535.

**Полноцветный RGB:** В изображении RGB каждый пиксель состоит из трех компонентов: красного, зеленого и синего. Отсутствует ColorMap. Для описания RGB-изображения необходимо добавить или изменить следующие поля и значения. Другие обязательные поля такие же, как и для изображений с цветовой палитрой.

Битсперсэмпл = 8,8,8. Каждый компонент имеет глубину 8 бит в изображении Baseline TIFF RGB.

PhotometricInterpretation = 2 (RGB) и нет ColorMap.

Тег = 277 (115.H)
Тип = КОРОТКИЙ
Количество компонентов на пиксель. Это число равно 3 для изображений RGB, если нет дополнительных выборок.

## Использованная литература ##

* [Формат файла TIFF — Википедия] (https://en.wikipedia.org/wiki/TIFF)
