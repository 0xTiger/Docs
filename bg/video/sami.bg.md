{
"дата": "2023-05-16",
  "keywords": [
"сами файл",
"какво е сам файл",
"пример за sami файл",
"файл",
"сами файлово разширение",
"разширение"
],
  "author": {
"показвано_име": "Шакил Фейз"
},
"draft": "false",
"toc": true,
"title": "SAMI файлов формат - файл за обмен на субтитри и метаданни",
  "description":"Научете за SAMI формата и API, които могат да създават и отварят SAMI файлове.",
  "linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
      "parent": "video"
}
},
"lastmod": "2023-05-16"
}

## Какво е SAMI файл?

Файл с разширение ".sami" обикновено се отнася до файл за обмен на субтитри и метаданни (SAMI). SAMI е формат за надписи, използван за показване на субтитри или надписи във видеоклипове. Първоначално е разработен от Microsoft за техния Windows Media Player.

Файловете SAMI съдържат информация за времето и текстово съдържание за субтитри или надписи, което им позволява да бъдат синхронизирани с възпроизвеждане на видео. Форматът поддържа основни опции за форматиране като стил на шрифта, цвят и позициониране на субтитрите на екрана.

SAMI файловете обикновено са обикновени текстови файлове и могат да се отварят и редактират с помощта на текстов редактор. Съдържанието на SAMI файл обикновено включва заглавна секция, която предоставя информация за файла, последвана от отделни записи на субтитри със съответното време и текст.

Ето пример за това как може да изглежда SAMI файл:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI файловете обикновено се използват във връзка с видео плейъри или медийни плейъри, които поддържат показване на субтитри, като Windows Media Player или VLC Media Player. Плейърът чете SAMI файла и синхронизира субтитрите с видео съдържанието, което позволява на зрителите да четат надписите, докато гледат видеото.

## Поддържани HTML тагове

Файловете SAMI (обмен на субтитри и метаданни) поддържат ограничен набор от HTML-подобни тагове за форматиране и стилизиране на субтитрите. Ето някои от често използваните тагове, поддържани от SAMI:

- ``<SAMI> :`` Основният елемент, който капсулира целия SAMI файл.
- ``<HEAD> :`` Съдържа заглавна информация за SAMI файла.
<html>- ``<TITLE> :`` Указва заглавието на SAMI файла. </html>
- ``<BODY> :`` Огражда записите на субтитрите и тяхната информация за времето.
- ``<SYNC> :`` Представлява точка за синхронизация за запис на субтитри. Той определя времето, в което субтитрите трябва да бъдат показани.
- ``<P> :`` Огражда действителното текстово съдържание на субтитри. Обикновено се използва в рамките на a<SYNC> блок.
<html>- `` <FONT>:`` Определя свойствата на шрифта за затворения текст. Атрибути като цвят, лице, размер и стил могат да се използват за промяна на външния вид на шрифта.</font>
- ``<BR> :`` Вмъква нов ред в субтитри.
<html>- `` <B>:`` Извежда оградения текст с удебелен шрифт.</b>
<html>- `` <I>:`` Извежда оградения текст в курсив.</i>
<html>- `` <U>:`` Извежда оградения текст подчертан.</u>
- ``<C> :`` Указва позицията или подравняването на текста на субтитрите на екрана. Той поддържа атрибути като център, среда, ляво, дясно, горе, долу и техните комбинации.
- ``<LANG> :`` Указва кода на езика за текста на субтитрите. Помага при идентифицирането на езика на субтитрите.

Това са някои от основните тагове, поддържани от SAMI файлове. Важно е да се отбележи, че SAMI не поддържа пълния набор от HTML тагове и атрибути. Поддържаните тагове са фокусирани основно върху стилизирането и позиционирането на субтитрите, вместо да предоставят разширено структуриране или интерактивност на документа.

## Препратки
* [SAMI](https://en.wikipedia.org/wiki/SAMI)
