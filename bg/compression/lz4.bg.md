{
  "date" : "2021-04-08",
  "keywords" :[ "lz4 файл", "lz4 файлов формат", "какво е lz4 файл", "файл", "lz4 пример", "lz4 файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - LZ4 компресиран файлов формат",
  "description":"Научете за файловия формат LBR и API, които могат да създават и отварят LZ4 файлове.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Какво е LZ4 файл?

Файл с разширение .lz4 е компресиран архивен файл, създаден с приложения/помощни програми, които поддържат [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)) компресия. Алгоритъмът LZ4 се фокусира върху компромис между скорост и степен на компресия. Компресирани LZ4 архиви могат да бъдат създадени с помощта на помощната програма за команден ред LZ4 и могат да бъдат декомпресирани с помощта на същата.

## LZ4 файлов формат

Файловият формат LZ4, базиран на алгоритъма за компресия LZ4, не зависи от типа на процесора, операционната система, файловата система и набора от символи. Подходящ е за компресиране на файлове и поточно компресиране с помощта на алгоритъма LZ4. Първоначалното внедряване на формата LZ4 беше извършено на [C](/bg/programming/c/) език от Yann Collet през 2011 г. и е достъпно за справка от разработчиците в [Github](https://github.com/lz4/lz4) .

### Формат на рамка LZ4

Общата структура на файловия формат LZ4 е както е показано по-долу.

|МагияNb|F. Дескриптор| Блок|(...)|EndMark |C. Контролна сума|
---|---|---|---|---|---|
|4 байта| 3-15 байта||| 4 байта| 0-4 байта|

#### Магическо число

4 байта, Little endian формат. Стойност: 0x184D2204

#### Дескриптор на рамка

Дескрипторът на рамката се състои от 3 t0 15 байта и е най-важната част от спецификациите. Заедно полетата Magic_Number и Frame_Descriptor се наричат LZ4 Frame Header и размерът му варира между 7 и 19 байта. Това е както е показано по-долу.

|FLG| BD| (Размер на съдържанието)| (ID на речника)| HC|
---|---|---|---|---|
|1 байт| 1 байт| 0 - 8 байта| 0 - 4 байта| 1 байт|

#### Блокове с данни

Всеки блок данни следва следния ред.

|Размер на блока| данни| (Блок контролна сума)|
---|---|---|
|4 байта| |0 - 4 байта|

#### EndMark

Потокът от блокове приключва, когато последният блок данни е последван от 32-битовата стойност 0x00000000.

#### Контролна сума на съдържанието

Content_Checksum проверява валидността на съдържанието, което се декодира правилно и се извършва с помощта на резултата от алгоритъма xxHash-32. Той валидира резултатите от успешното предаване на всички блокове в правилния ред и без грешка.

## Препратки

* [LZ4 формат на рамка](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [Алгоритъм за компресиране LZ4 - Уикипедия](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

