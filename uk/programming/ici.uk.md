{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "файл", "розширення", "формат файлу", "реалізація ICI", "Посібник з програмування", "приклад ici", "мова програмування ICI", "модулі ICI", "модель даних ICI ", "документація ICI", "Мова ICI" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - файл мови програмування",
  "description":"Дізнайтеся про формат файлу ICI та API, які можуть створювати та відкривати файли ICI.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## Що таке файл ICI?

Мова програмування загального призначення, яка інтерпретується та містить кілька функцій, таких як динамічне введення разом із гнучкими типами даних, відома як мова програмування ICI (не абревіатура). Вважається, що вона схожа на мову [Perl](/uk/programming/pl/). Ця мова ICI містить конструкції керування потоком, а також деякі оператори мови C. Це не об’єктно-орієнтована мова, але деякі особливості ООП можуть бути досягнуті за допомогою спеціального методу успадкування, відомого як надбудови. Подібно до [C](/uk/programming/c), ця мова програмування ICI має той самий системний інтерфейс і стандартну бібліотеку для вбудованих функцій.


## Коротка історія ##

Наприкінці 1980-х років її розробив Тім Лонг як інтерпретовану мову програмування загального призначення. Більшість функцій цієї мови схожі на C, і вона також може досягти деяких функцій, застосовуючи деякі спеціальні методи. Ця мова є суспільним надбанням і доступна як мова для перепродажу, і ніхто не зобов’язаний згадувати, звідки він отримав вихідний код. Авторські права на документацію ICI належать Canon Information System Research Australia.

## Технічна специфікація ##

У цій мові використовуються два різних типи даних. Ці два типи даних є простими та агрегатними. Обидва вони містять різні вирази відповідно до їх попередньо визначеного складу в мові. Ця мова підтримує різні модулі, такі як вкладені та підпрограми. Оскільки деякі його властивості подібні до Perl, він має сувору інтеграцію з регулярними виразами.

Набори обмежені як неоднорідні та вкладені. Ці набори забезпечують підтримку широко використовуваних операцій із наборами, таких як Union і Intersection тощо. Здебільшого він використовується як мова для базової реалізації програм, що належать багатонаціональним організаціям.

Майже всі типи програм можуть бути написані цією мовою, і переважно конкретні програми, які включають складні структури даних, написані мовою програмування ICI. Додатки можуть включати реалізацію ICI таким чином, щоб вони були в ній написані. Функціональні частини програми можуть бути реалізовані модулями ICI. Мова ICI дещо нагадує мову C, але модель даних ICI має досить високий рівень і відрізняється такими типами, як словники (struct), набори, динамічні масиви, регулярні вирази та (дійсні) рядки.


## Приклад формату файлу ICI ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Посилання ##

* [Мова програмування ICI](http://atrn.org/ici/doc/ici.html)



