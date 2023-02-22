{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу AWK - файл сценарію AWK",
  "description":"Дізнайтеся про формат файлу AWK та API, які можуть створювати та відкривати файли AWK.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Що таке файл AWK?

Файл AWK — це файл сценарію, створений для програми обробки тексту **AWK**, яка постачається в комплекті з операційними системами Unix і Linux. Він містить логічні інструкції для виконання дій над текстом або вмістом файлу, наприклад зіставлення, заміна та друк тексту. Це допомагає створювати звіти та форматований текст із вхідного файлу. У більшості дистрибутивів Linux/Unix утиліта awk зазвичай знаходиться в /usr/bin/awk.

## Як створити сценарій AWK?

Файл AWK можна створити або відкрити в будь-якому текстовому редакторі в ОС Linux/Unix. Новий файл сценарію AWK можна створити наступним чином.

```
$ vi script.awk
```

Це відкриє файл AWK у текстовому редакторі. Введіть кілька тверджень у текстовому редакторі, як показано нижче.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Перший рядок цього текстового вмісту пояснюється наступним чином.

* \#! – називається `Shebang`, який визначає інтерпретатор інструкцій у сценарії
* /usr/bin/awk – інтерпретатор
* -f – параметр інтерпретатора, який використовується для читання файлу програми

## Як запустити сценарій AWK?

Збережіть файл і зробіть сценарій виконуваним, виконавши команду нижче:
```
$ chmod +x script.awk
```

Потім сценарій можна запустити наступним чином.

```
$ ./script.awk
```

що призводить до наступного результату.

```
Writing my first Awk executable script!
```

## Посилання ##

* [Створення сценаріїв за допомогою мови програмування Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)
