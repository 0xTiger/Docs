{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LRC файлов формат - Какво е LRC файл?",
  "description":"Научете за файла LRC Lyric и API, които могат да създават и отварят LRC файлове.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Какво е LRC файл?

LRC файлът е текстов файл с текстове, който съдържа текстовете на аудио песен. Когато аудио песента се възпроизвежда с музикален плейър или софтуер за аудио плейър на компютър, LRC файлът се чете паралелно и се показва с времето. LRC файловете съдържат ключови точки за показване на текстове, когато песента се възпроизвежда. Като цяло LRC файловете имат същото име като съответния аудио файл, като audio.mp3 и audio.lrc. LRC файловете са подобни на файлове със субтитри като [SRT](/bg/video/srt/).

## LRC файлов формат - повече информация

Файловете с текстов формат LRC се записват като обикновени текстови файлове и могат да се отварят и редактират в текстов файл. Съдържанието на LRC файл съдържа цветова информация за показване на текстов текст.

## LRC формати

Има множество формати на LRC файлове, които са разработени с течение на времето. Тези

### Прост LRC формат

Етикетите за време на линията са във формат `[mm:ss.xx]`, където mm е минути, ss е секунди и xx е стотни от секундата.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Разширен прост формат

Включва възможността за промяна и определяне на пола на текстовете с помощта на M: мъжки, F: женски, D: дует.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Подобрен LRC формат

Подобреният LRC формат е разширена версия на Simple LRC формат. Добавя Word Time Tag във формата`<mm:ss.xx>` в края на предишната дума.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Препратки

* [LRC текстов формат - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

