{
  "date" : "2019-10-11",
  "keywords" :[ "файл mov", "формат файлу mov", "що таке файл mov", "файл", "приклад mov", "розширення файлу mov", "розширення", "формат", "QuickTime", "MPEG- 4"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл MOV – формат файлу фільму Apple QuickTime",
  "description":"Дізнайтеся про формат файлу MOV та API, які можуть створювати та відкривати файли MOV.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Що таке файл MOV?

Файл MOV — це тип відеофайлу, розроблений компанією Apple Inc., який містить одну або кілька доріжок. Кожен трек зберігає фільм, аудіо, відеокліпи та субтитри. Це мультимедійний контейнер, який може зберігати різні типи медіа-елементів. Формат відео MOV сумісний із системами Windows і Macintosh. Він використовує кодування MPEG-4 для стиснення, а треки зберігаються в об’єктах, які називаються атомами, які розміщені в ієрархічній структурі даних.

## Коротка історія формату файлу MOV

Формат файлу MPEG-4 розвинувся на основі специфікації QuickTime File Format (**QTFF**) у 2001 році. Міжнародна організація стандартизації схвалила формат, а системні специфікації MPEG-4 Part 1 були опубліковані в 1999 році. У 2001 році файл перегляду формат [MP4](/uk/video/mp4/) було опубліковано.

Перша версія MP4 була переглянута в 2003 році як MPEG-4, частина 14 (ISO/IEC 14496-14:2003). У 2004 році MP4 було узагальнено, щоб визначити загальну структуру для всіх мультимедійних файлів на основі часу. Тому тепер він використовується як основа для різноманітних інших форматів мультимедійних файлів.

## Формат файлу QuickTime (QTFF) – Додаткова інформація

Для роботи з цифровим мультимедіа QTFF може зберігати багато видів даних. Це ідеальний формат для обміну цифровими медіафайлами, оскільки цей формат визначає стандарти для опису будь-яких медіаструктур. Формат файлу складається з гнучкого набору об'єктно-орієнтованих об'єктів. Для зберігання фільмів на дисках QuickTime використовує дві структури, тобто `atoms` і `QT atoms`.

### Атоми

Atom є основною одиницею файлу QuickTime. У будь-якому атомі перед будь-яким іншим полем є два основних поля: поля розміру та типу. Поле розміру показує розмір атома, а поле типу вказує тип даних, що зберігаються в атомі. За своєю природою атоми є ієрархічними, що означає, що один атом може містити інші атоми, які можуть містити інші. Розташування зразка атома показано на наступному зображенні.

Кожен атом має дві частини: "заголовок" і "дані". Заголовок містить поля розміру та типу, а частина даних містить фактичні дані. Крім того, кожне поле пояснюється нижче:

### Розмір атома

Заголовок і вміст атома позначаються 32-розрядним цілим числом, відомим як розмір атома. Поле розміру містить розмір атома в байтах, виражений 32-розрядним цілим числом без знаку.

### Тип атома

Тип атома також відображається 32-розрядним цілим числом, яке здебільшого розглядається як чотирисимвольне поле з кнемонічним значенням, наприклад «moov» (0x6D6F6F76) для атома фільму або «trak» (0x7472616B) для трековий атом. Як тільки тип атома відомий, це дозволяє інтерпретувати його дані.

### Атоми QT і контейнери атомів

Атоми QT забезпечують формат зберігання загального призначення та мають розширений заголовок, що складається з полів розміру, типу, ідентифікатора атома та кількості дочірніх атомів. Атоми QT загорнуті в атомний контейнер, унікальну структуру даних із заголовком із підрахунком блокувань. У кожному контейнері атома є один кореневий атом, який є атомом QT. Розташування атома QT показано на малюнку нижче.

Заголовок контейнера QT atom містить такі дані:

Зарезервовано: 10-байтовий елемент зі значенням 0.

Lock Count: 16-бітове ціле число зі значенням 0.

Заголовки атомів QT містять такі дані:

**Розмір -** Заголовок атома QT і вміст позначаються в байтах 32-бітним цілим числом. У випадку листкового атома це поле містить розмір одного атома.

**Тип -** Тип атома вказується 32-розрядним цілим числом. Якщо це кореневий атом, значення встановлюється на «sean».

**Atom ID -** Це 32-розрядне ціле число, яке показує атомний ID і має бути унікальним для всіх братів і сестер. Кореневий атом завжди має значення ID атома як 1.

**Зарезервовано -** 16-розрядне ціле число, яке має бути встановлено на 0.

**Число дочірніх елементів -** 16-розрядне ціле число, яке вказує кількість дочірніх атомів атома.

**Зарезервовано -** 32-розрядне ціле число, яке має бути встановлено на 0.

## Файлова структура файлів MOV

Файли MOV складаються з послідовних фрагментів. Кожна послідовність має 8-байтовий заголовок: 4-байтовий розмір послідовності (старший байт, перший старший байт) і 4-байтовий тип послідовності — один із попередньо визначених підписів: «ftyp», «mdat», «moov», «pnot». ", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Перший фрагмент має тип "ftype" і має підтип зі зсувом 8. MOV визначається підтипом, який має бути "qt ". Для створення файлу MOV потрібно повторювати фрагменти, доки не буде виявлено невідомий тип.

Ось `приклад прикладу`: Перевірка зразка двійкових даних файлу MOV стає очевидним, що він починається з підпису **ftyp** (шістнадцятковий: 66 74 79 70) зі зміщенням 4, який визначає тип файлу-контейнера QuickTime. Підтип файлу — **qt~_~_** (шістнадцятковий: 71 74 20 20), що вказує на тип файлу MOV. Розмір першого блоку дорівнює 32 (шістнадцятковий: 00 00 00 20, старший байт, перший старший байт), розмір, розташований за зсувом 0. За зміщенням 32 (шістнадцятковий: 20) розташований другий фрагмент, який має розмір 8 і введіть **mdat** (шістнадцятковий код: 6D 64 61 74).

Наступний фрагмент розташований за зсувом 32+8#40 (шістнадцятковий: 28) і має розмір 3 263 028 (шістнадцятковий: 00 31 CA 34) і тип **mdat** (шістнадцятковий: 6D 64 61 74) зі зміщенням 44 (шістнадцятковий : 2C). Наступний фрагмент розташований за зміщенням 40 + 3 263 028#3 263 068 (шістнадцятковий: 00 31 CA 5C) і має розмір 21 189 (шістнадцятковий: 00 00 52 C5) і тип **moov** (шістнадцятковий: 6D 6F 6F 76) за зміщенням 1,836,019,574 (шістнадцятковий: 00 31 CA 60). Це останній фрагмент, тому загальний розмір файлу становить 3 263 068+21 189#3 284 257 байт.

## Як конвертувати файл MOV?

Існує багато медіа-програвачів і програмних відеоредакторів для конвертації файлів MOV в інші популярні формати відеофайлів. Деякі медіапрогравачі, які можуть конвертувати файли MOV в інші формати, включають:

* Медіаплеєр VideoLAN VLC
* Eltima Elmedia Player

Кілька медіаплеєрів і відеоредакторів, зокрема медіаплеєр VideoLAN VLC і Eltima Elmedia Player, можуть конвертувати файли MOV в інші формати. Це програмне забезпечення може конвертувати файли MOV у такі формати відео.

* Відео MPEG-4 - [MP4](/uk/video/mp4/)
* Відео WebM - [WEBM](/uk/video/webm/)
* Транспортний відеопотік - [TS](/uk/video/ts/)
* Розширений системний формат - [ASF](/uk/video/ts/)
* Ogg Vorbis Audio - [OGG](/uk/audio/ogg/)
* MP3 Audio - [MP3](/uk/audio/mp3/)
* Безкоштовний аудіокодек без втрат - [FLAC](/uk/audio/flac/)
* WAVE Audio - [WAV](/uk/audio/wav/)

## API з відкритим кодом для файлів MOV

* [React Native API для перетворення MOV у MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [API Python для відновлення файлів MOV](https://github.com/nrosenstein-stuff/movrepair)
* [API Ruby для перетворення MOV у GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Список літератури

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

