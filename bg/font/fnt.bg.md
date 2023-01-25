{
  "date" : "2020-08-20",
  "keywords" :[ "fnt файл", "fnt файлов формат", "какво е fnt файл", "файл", "fnt пример", "fnt файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - файл с шрифтове на Windows",
  "description":"Научете за FNT файловия формат и API, които могат да създават и отварят FNT файлове.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Какво е FNT файл?

Файл с разширение .fnt е файл с шрифтове, който съхранява обща информация за шрифтове в операционни системи Windows. FNT файловете са заменени предимно от файлови формати TrueType (.TTF) и OpenType (.OTF) и към момента е остарял файлов формат за шрифтове. Тези файлове могат да съхраняват един оценъчен или векторен шрифт. Всички драйвери на устройства поддържат Windows 2.x шрифтове. Въпреки това, не всички драйвери на устройства
поддържат версията на Windows 3.0.

## FNT файлов формат

FNT файловете могат да съхраняват един растерен или векторен шрифт. Векторните формати се използват по-често от GDI в сравнение с растерните, където всеки глиф на хартата се дефинира с помощта на малко растерно изображение. Очевидната причина за замяната на .fnt с .ttf и .otf е неговият растерен формат.

### Заглавка на файла с шрифтове
Началото на файловете с растерни и векторни шрифтове е обичайно, последвано от различна информация за всеки тип файл. Заглавката на шрифтовия файл включва за Windows 3.0 включва шест нови полета, както следва, които са зададени на нула, за да се гарантира съвместимост с бъдещи версии на Windows.

* dФлагове
* dfAspace
* dfBspace
* dfCspace
* dfColorPointer
* dfReserved1

За подробна информация относно заглавките за Windows 3.0 и 2.0 посетете [Архив на Microsoft KnowledgeBase](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Препратки
* [Файлов формат на шрифта](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Как да инсталирате или премахнете шрифт в Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8 -7613-c76f-88d043b334b8)
