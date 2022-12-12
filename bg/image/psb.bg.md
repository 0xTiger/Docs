{
  "date" : "2019-10-11",
  "keywords" :[ "psb файл", "psb файлов формат", "какво е psb файл", "файл", "psb пример", "psb файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Photoshop Big Image File Format",
  "description":"Научете за PSB файловия формат и API, които могат да създават и отварят PSB файлове.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е PSB файл?
Adobe photoshop записва файлове в два формата. Файлове с размер 30 000 на 30 000 пиксела се записват с разширение PSD, а файлове, по-големи от PSD до 300 000 на 300 000 пиксела, се записват с разширение PSB, известно като „Photoshop Big“. По-конкретно, PSB файловете могат да бъдат големи до 4 EB (над 4,2 милиарда GB) с изображения с височина и ширина до 300 000 пиксела. PSD, от друга страна, могат да бъдат с максимум до 2 GB и размери на изображението от 30 000 пиксела.

PSB е известен също като голям формат за Photoshop и поддържа всички функции на Photoshop като слоеве, ефекти и филтри. Photoshop може да конвертира PSB файл в [PSD](/bg/image/psd/), [JPG](/bg/image/jpeg/) , [PNG](/bg/image/png/), [EPS](/bg/page-description-language/eps/), [GIF](/bg/image/gif/) и други формати. Големият формат на документ на Photoshop е наличен, след като е активирана функцията за панел за обработка на файлове в диалоговия прозорец с предпочитания на Photoshop.

## Информация за файлов формат ##

Файловият формат на Photoshop е разделен на пет основни части с много маркери за дължина за преместване между секциите.

|Файлов формат
---|
|Заглавка на файл
| Данни за цветовия режим
| Ресурси за изображения
|Информация за слой и маска
|(((
Данни за изображения
)))

### Заглавка на файл ###

Хедърът на файла има фиксирана дължина от 26 байта и съдържа основните свойства на изображението.

BYTE Signature [4] – Равно на „8BPS“.

Версия на WORD [2] – Номер на версията, PSD # 1, PSB # 2.

BYTE Reserved [6] – Резервиран и винаги нула.

WORD Channels [2] – Брой цветни канали в изображението, включително алфа канали. Стойността му варира от 1 до 56.

ДЪЛГИ редове [4] – Височина на изображението в пиксели, PSD 1-30 000, PSB 1-300 000.

ДЪЛГИ колони [4] – Ширина на изображението в пиксели, PSD 1-30 000, PSB 1-300 000.

WORD Depth [2] – Брой битове на канал. Поддържаните стойности са 1,8,16 и 32.

Режим WORD [2] – Цветен режим на файла.

#### Описание на режима ####


|Режим|Описание
---|---|
|0|Растерно изображение (монохромно)
|1|Сива скала
|2|Индексиран
|3|RGB
|4|CMYK
|7|Многоканален
|8|Двутон (полутон)
|9|Лаборатория

### Данни за цветен режим ###

След раздела за заглавката на файла следва разделът с данни за цветовия режим. Блокът започва с ДЪЛГО число, което дава дължината на блока в байтове. Структурата на данните за цветовия режим е следната:

4 байта – Дължината на следните цветни данни.

Променлива – Данни за цвета

Ако стойността на полето за режим в секцията на заглавката не е индексиран цвят или дуотон, дължината на блока ще бъде 0 и няма да има данни след полето за дължина.

За индексирани цветни изображения дължината ще бъде 768 байта, които ще съдържат 256 цветова палитра. За duotone данните ще съдържат параметри на екрана и друга свързана информация.

### Ресурси за изображения ###

След секцията с данни за цветовия режим, третият блок е секцията с ресурси за изображения. Първите четири байта са ДЪЛГО число, указващо дължината на блока, последвано от серия от ресурсни блокове. Структурата на блока с ресурси на изображението е следната:

Тип BYTE [4] – Подпис „8BIM“

WORD ID [2] – ID на изображението. Има списък с идентификатори на ресурси, които могат да се видят от референтната връзка.

BYTE Име [променлива] – Име: Pascal низ с четна дължина. ** **

LONG Size [4] – Действителен размер на данните за ресурса, които следват.

BYTE Данни [Променлива} – Данни за ресурс. Подплатен е, за да направи равномерен размер.

Някои от форматите на ресурсите са обяснени накратко по-долу:

**Ресурсен формат за решетка и водачи: ** Информацията за решетка и водачи се съхранява в ресурсен блок. Тези ресурсни блокове съдържат 16-байтова решетка и насочваща заглавка, последвана от 5-байтови блокове с насочваща информация.

**Формат на ресурс за миниатюри: ** Информацията за миниатюри се съхранява в блока за ресурс на изображение за показване на предварителен преглед, който се състои от 28 байта заглавка и JFIF миниатюра в RGB.

**Формат на ресурси за цветни семплери:** Информацията за цветни семплери се съхранява в ресурсен блок за изображение с 8-байтова заглавка, последвана от блок с променлива дължина от информация за цветни семплери.

### Информация за слой и маска ###

Четвъртият блок е информационен блок за слой и маска и съдържа информация за слоевете и маските. Първо се съхранява информация за слоя и след това информация за маската.

**Информация за слоя:** Информацията за слоя започва със стойност LONG, която показва дължината на информацията за слоя. След това има преброяване на стойността на WORD, което показва броя на записите на слоя, които да следват.

[8] – дължина на слоевете

[2] – Брой слоеве

[Променлива] – Информация за всеки слой.

[Променлива] – Данни за изображение на канала.** **

**Информация за маската:** Структурата на маската има следния формат:


|Структура на данните|Име на поле| Описание
---|---|---|
|ДУМА| Цветно пространство на наслагване| (Не е документирано)
|БАЙТ[8]| Цветни компоненти| 4x2 байта цветни компоненти
|ДУМА| Непрозрачност| 0#прозрачен, 1#непрозрачен
|БАЙТ| вид| 0#инвертирано, 1#защитено, 128#използване на съхранена стойност
|БАЙТ| подплата| настроен на нула

### Данни за изображения ###

Последният раздел съдържа данните за пикселите на изображението. Данните за изображението се съхраняват като поредица от последователности в равнини, т.е. първо всички червени данни, след това всички зелени данни и т.н. ДУМАТА в началото на всеки ред показва размера в байтове, свързани с всеки сканиран ред.

[2] – Метод на компресия:

[Променлива] – Данни за изображението в планарен ред, т.е. RRRR, GGGG, BBBB и др.

Методи за компресиране:

0 – Raw Данни за изображения

1 – RLE Компресиран

2 – Цип без прогноза

3 – Цип с прогноза

## Референция ##

* [Файлов формат PSB – от Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB – Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)
