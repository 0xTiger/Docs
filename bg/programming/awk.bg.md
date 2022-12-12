{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AWK файлов формат – AWK скрипт файл",
  "description":"Научете за AWK файловия формат и API, които могат да създават и отварят AWK файлове.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Какво е AWK файл?

AWK файлът е файл със скрипт, създаден за приложението за обработка на текст **AWK**, което идва в комплект с операционни системи Unix и Linux. Той съдържа логически инструкции за извършване на действия върху текст или съдържание на файл, като съпоставяне, заместване и отпечатване на текст. Това помага за генериране на отчети и форматиран текст от входния файл. Помощната програма awk обикновено се намира в /usr/bin/awk на повечето дистрибуции на linux/unix.

## Как да създадете AWK скрипт?

AWK файл може да бъде създаден или отворен във всеки текстов редактор на Linux/Unix OS. Нов AWK скрипт файл може да бъде създаден, както следва.

```
$ vi script.awk
```

Това ще отвори AWK файла в текстов редактор. Въведете някои твърдения в текстовия редактор, както следва.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Първият ред от това текстово съдържание е обяснено, както следва.

* \#! – наричан „Shebang“, който указва интерпретатор за инструкциите в скрипт
* /usr/bin/awk – е интерпретаторът
* -f – опция за интерпретатор, използвана за четене на програмен файл

## Как да изпълним AWK скрипт?

Запазете файла и направете скрипта изпълним, като издадете командата по-долу:
```
$ chmod +x script.awk
```

След това скриптът може да се стартира, както следва.

```
$ ./script.awk
```

което води до следния резултат.

```
Writing my first Awk executable script!
```

## Референция ##

* [Напишете скриптове с помощта на езика за програмиране Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)
