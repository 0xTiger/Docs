{
  "date" : "2021-04-08",
  "keywords" :[ "файл dar", "формат файлу dar", "що таке файл dar", "файл", "приклад dar", "розширення файлу dar", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - формат файлу архіватора диска",
  "description":"Дізнайтеся про формат файлу DAR та API, які можуть створювати та відкривати файли DAR.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Що таке файл DAR?

Файл із розширенням .dar — це стислий архів, створений за допомогою архіву DAR Disk. Він може створити резервну копію/архів для всього диска або групи файлів. Він був створений для заміни формату файлу [TAR](/uk/compression/tar/) в ОС UNIX і може бути створений як розділений архів для великої кількості файлів. Архів DAR підтримує опцію видалення файлів із системи, які пов’язані з основними файлами в архіві. Його можливості щодо забезпечення диференціального, інкрементального та декрементального резервного копіювання роблять його кращим, ніж файли TAR.

## Формат файлу DAR

Файли DAR — це стиснуті архіви, які можуть використовувати будь-яке стиснення для кожного файлу, наприклад [gzip](/uk/стиск/gz/), [bzip2](/uk/стиснення/bz2/), lzo, xz або lzma. Точний формат файлу DAR залежить від того, який тип форматування використовується для стиснення вмісту архіву. Він також підтримує додаткове шифрування Blowfish, Twofish, AES, Serpent, Camellia, а також шифрування з відкритим ключем і підпис (OpenPGP).

### Функції DAR

Нижче наведено деякі функції формату файлу DAR.

* Піклується про будь-який тип inode (каталог, звичайні файли, символічні посилання, спеціальні пристрої, іменовані канали, сокети, двері, ...)
* Піклується про жорстко пов’язані inode (жорстко пов’язані прості файли, пристрої char, блокові пристрої, жорстко пов’язані символічні посилання)
* Доглядає за розрідженими файлами
* Піклується про розширені атрибути файлів Linux,
* Піклується про ACL файлу Linux
* Піклується про розгалуження файлів Mac OS X
* Піклується про деякі специфічні атрибути файлової системи, як-от дата народження файлової системи HFS+ і незмінні атрибути, журналювання даних, безпечне видалення, без злиття, невидалення, noatime файлової системи ext2/3/4.
* Стиснення файлів за допомогою gzip, bzip2, lzo, xz або lzma (на відміну від стиснення всього архіву). Особа може вибрати не стискати вже стиснуті файли на основі суфікса імені файлу.
* Швидке витягування файлів з будь-якого місця в архіві
* Швидке перерахування вмісту архіву шляхом збереження каталогу файлів в архіві
* Резервне копіювання файлової системи в реальному часі: визначає, коли файл було змінено під час його читання для резервного копіювання, і може повторно зберегти його до заданої максимальної кількості повторів
* Хеш-файл (MD5, SHA1 або SHA-512), створений на льоту для кожного фрагмента, отриманий файл сумісний з md5sum або sha1sum, щоб можна було швидко перевірити цілісність кожного фрагмента
* Незалежність від файлової системи: його можна використовувати для відновлення системи на розділі іншого розміру та/або на розділі з іншою файловою системою[5]

## Список літератури

* [DAR](http://dar.linux.free.fr/)
* [Архіватор дисків DAR](https://en.wikipedia.org/wiki/Dar_(disk_archiver))
