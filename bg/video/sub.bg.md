{
"дата": "2023-06-21",
  "keywords": [
"подфайл",
"какво е подфайл",
"пример за файл със субтитри на MicroDVD",
"Разширения за субтитри",
"Отвори суб",
"Типове файлове със субтитри",
"как да отворя SUB файл",
"файл",
"SUB файлово разширение",
"разширение"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "SUB файлов формат - MicroDVD файл със субтитри",
  "description":"Научете за SUB формата и API, които могат да създават и отварят SUB файлове.",
  "linktitle": "SUB",
  "menu": {
    "docs": {
      "identifier": "video-sub",
      "parent": "video"
}
},
"lastmod": "2023-06-21"
}

## Какво е SUB файл?

SUB файлът е MicroDVD файлов формат за субтитри, използван за показване на субтитри във видеоклипове, обикновено има файлово разширение .sub. Тези файлове съдържат информация за времето и текст за всеки запис на субтитри.

MicroDVD файловете със субтитри използват прост текстов формат, където всеки запис на субтитри се състои от няколко реда. Първият ред съдържа информация за времето на субтитрите, включително началните и крайните времеви клейма. Следващите редове съдържат действителния текст на субтитрите.

Ето пример за файл със субтитри на MicroDVD:

```
{0}{100}Subtitle line 1
{150}{300}Subtitle line 2
{350}{550}Subtitle line 3
...
```

## Разширения за субтитри

Субтитрите могат да имат различни файлови разширения в зависимост от формата, в който са. Някои често срещани файлови разширения на субтитри включват:

- **.srt:** SubRip формат на субтитрите. Това е един от най-широко използваните формати на субтитри и се поддържа от много медийни плейъри и софтуер за редактиране на видео.
- **.sub:** Файлов формат на субтитри, който може да се използва от различни формати на субтитри, като MicroDVD, SubViewer и SubStation Alpha.
- **.ass или .ssa:** Advanced SubStation Alpha или SubStation Alpha формат на субтитрите. Той поддържа разширени функции като форматиране на текст, позициониране и ефекти.
- **.vtt:** WebVTT (Web Video Text Tracks) формат, използван за показване на субтитри в уеб видеоклипове. Обикновено се използва с HTML5 видео плейъри.
- **.idx/.sub:** Формат, използван от DVD субтитри. Файлът .idx съдържа информация за времето и форматирането, докато файлът .sub съдържа действителния текст на субтитрите.
- **.smi или .sami:** Синхронизиран формат за обмен на достъпни медии. Обикновено се използва за надписи и субтитри в Windows Media Player.

## Какво се разбира под Open Sub?

Open Sub обикновено означава OpenSubtitles, която е популярна онлайн платформа, която предоставя субтитри за филми и телевизионни предавания на множество езици. Той предлага огромна колекция от файлове със субтитри, предоставени от неговата общност от потребители. Можете да посетите уебсайта на OpenSubtitles (www.opensubtitles.org), за да търсите и изтегляте субтитри за желаните от вас филми или телевизионни сериали.

## Типове файлове със субтитри

Файловете със субтитри се предлагат в различни формати, всеки със собствен файлов тип или разширение. Ето някои често срещани типове файлове със субтитри:

- **SubRip Subtitle Format (.srt):** Това е един от най-широко използваните формати на субтитри. SRT файловете са обикновени текстови файлове, които съдържат записи на субтитри с времеви клейма и съответен текст.
- **Формат на субтитрите на SubViewer (.sub):** Файловете на SubViewer са подобни на SRT файловете, съдържат записи на субтитри с времеви клейма и текст, може да поддържат допълнителни функции като форматиране на текст и цветове.
- **SubStation Alpha (.ssa) и Advanced SubStation Alpha (.ass):** Тези формати поддържат разширени функции като форматиране на текст, стил, позициониране и анимационни ефекти. SSA и ASS файловете обикновено се използват за аниме субтитри.
- **MicroDVD формат на субтитри (.sub):** MicroDVD форматът използва .sub файлове и включва времева информация и текст за всеки запис на субтитри. Често се използва с медийни плейъри и софтуер за редактиране на видео.
- **DVD субтитри (.sub и .idx):** DVD субтитрите обикновено се състоят от два файла: .sub файл, който съдържа текст на субтитрите, и .idx файл, който съдържа информация за времето и форматирането.
- **WebVTT (.vtt):** WebVTT е формат на субтитри, използван за уеб видеоклипове, често използван с HTML5 видео плейъри и поддържа основни опции за форматиране.
- **MPL2 формат на субтитрите (.mpl):** MPL2 файловете се използват с MPlayer, медиен плейър за Unix-подобни системи, съдържат записи на субтитри с времеви клейма и текст.
- **iTunes Timed Text (.itt):** iTunes Timed Text файловете се използват за субтитри в iTunes на Apple и други платформи на Apple. Те поддържат функции като стилизиране и позициониране на текст.
- **Формат на субтитрите на телетекста (.srt или .txt):** Субтитрите на телетекста обикновено се използват в телевизионно излъчване. Те обикновено се записват като обикновени текстови файлове с разширения .srt или .txt.

## Как да отворя SUB файл?

Следните медийни плейъри могат да отварят SUB файл като песен със субтитри.

- VideoLAN VLC медиен плейър
- MPlayer

За да отворите SUB файл във VLC плейър, следвайте тези стъпки

- Отворете VLC плейър и пуснете вашето видео
- От лентата с менюта на VLC Media Player изберете **Субтитри > Добавяне на файл със субтитри ....**
- Отидете до SUB файла и го отворете

Ако трябва да редактирате SUB файл, можете да го отворите с всеки текстов редактор, например Microsoft Notepad (Windows) или Apple TextEdit (Mac).

## Препратки
* [MicroDVD](https://en.wikipedia.org/wiki/MicroDVD)

