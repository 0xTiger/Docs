{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "файл", "розширення", "формат", "що таке формат файлу m4a", "музика", "формат файлу m4a", "M4A проти MP3", "специфікація формату файлу m4a "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу M4A та API, які можуть створювати, конвертувати та відкривати файли M4A.",
  "title" :"M4A - аудіофайл MPEG-4",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Що таке файл M4A?

**Формат файлу M4A** – це аудіофайл, створений за допомогою AAC (Advanced Audio Coding), відомого як стиснення з втратами. Слово M4A скорочено MPEG 4 Audio. Ці аудіофайли зазвичай мають розширення .m4a. Особливо це стосується незахищеного вмісту. Він може зберігати різні типи аудіовмісту, наприклад аудіокниги, пісні та подкасти. M4A зазвичай реалізується як більш просунутий формат, ніж MP3, який зазвичай не розроблявся лише для аудіо. Це просто аудіошар у відеофайлах MPEG 1 або 2.

Формат M4A зашифровано за допомогою FairPlay Digital Rights Management, тому що продаються через iTunes Store із розширенням .m4p. Apple iPhone використовує аудіо MPEG-4 для мелодій, але ці аудіофайли мають розширення .m4r.


## M4A проти MP3

І M4A, і [MP3](/audio/mp3/) є форматами лише аудіофайлів.

**M4A**: кращий за MP3 з точки зору якості та розміру за умови кодування з однаковою швидкістю передачі даних. Розширення файлу .m4a настільки поширене, тому що воно використовується Apple для використання в iTunes Music Store. M4A — це аудіофайл, стиснутий за технологією MPEG-4; алгоритм стиснення з втратами. Він в основному пов’язаний із “MPEG-4 Audio Layer”, файли з розширенням .m4a є аудіошаром фільмів MPEG-4. Він має витіснити MP3 і стати новим стандартом стиснення звуку. Він дуже близький до MP3 у багатьох відношеннях, але введений для кращої якості при тому самому чи навіть меншому розмірі файлу. Формат M4A вперше представила Apple. Тип формату також реалізований як Apple Lossless Encoder (ALE).

Таким чином, наразі M4A не може досягти такого успіху, як MP3, оскільки цей аудіоформат ще не можна відтворити. Він чомусь обмежений лише MacOS, iPod та іншими продуктами Apple.

**Mp3**: найвідоміший формат цифрового аудіо. Це також був один із перших форматів стиснення на сцені та став дуже популярним серед любителів музики. Його основний успіх настільки швидкий, що цей тип файлу можна відтворювати повсюдно та майже будь-чим, апаратним чи програмним забезпеченням. У загальному розумінні M4A створюватиме кращу якість звуку, але багато хто сперечатиметься, що, правда це чи ні, різниця у звукі не помітна, і було б марною тратою часу, намагаючись перетворити файли MP3 у файли M4A. Зрештою, перетворення призведе до втрати оригінальної якості звуку.

## Специфікація формату файлу M4A

Файли M4A складаються з послідовних блоків. Кожна послідовність має 8-байтовий заголовок і поділений на:
- 4-байтний розмір фрагмента (старший байт, старший байт спочатку)
- 4-байтовий тип блоку - один із попередньо визначених підписів: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt ", "ssrc", "PICT".

Перший фрагмент матиме тип "ftype" і матиме підтип зі зсувом 8. M4A, визначений підтипом, який має бути "M4A_", для підтипу M4B має бути "M4B_", а для підтипу M4P має бути "M4P_".

Ітерація фрагментів, доки не буде виявлено фрагмент невідомого типу, створить файл M4A (MPEG-4 Audio).

## Посилання ##

* [MPEG-4, частина 14 – Вікіпедія](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Приклад формату та відновлення MPEG-4, частина 14 аудіо (M4A, M4B, M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

