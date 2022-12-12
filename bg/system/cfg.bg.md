{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "разширение", "файл", "формат", "система", "конфигурация", "настройки", "програми", "компютър", "приложение"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - файлов формат",
  "description":"Научете за CFG файловия формат и API, които могат да създават и отварят CFG файлове.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Какво е CFG файл? ##

Файл с разширение .cfg е тип файл с "настройки". Това е широко използван тип файл и се използва за съхраняване на информация относно конфигурацията и настройките за компютърни програми. Повечето типове CFG файлове се съхраняват в текстов формат и не трябва да се отварят ръчно, вместо това трябва да се отварят с текстов редактор. Има обаче различни видове CFG файлове, които се различават по формата, в който се съхранява информацията. Функциите, които CFG файловете предлагат, варират от приложение до приложение. Някои компютърни приложения позволяват на потребителите да променят или развиват синтаксиса на своите конфигурационни файлове чрез използване на графични намеси, докато други позволяват модификации само с помощта на текстов редактор. След като модифицират тези файлове, потребителите могат да инструктират приложението да прочете тези файлове отново и да приложи модификациите към системата.


## CFG файлов формат ##

CFG файловете се поддържат от различни операционни системи като Unix и Unix-подобни операционни системи, MS-DOS, macOS, Microsoft Windows и IBM OS/2. Форматът, в който тези файлове се съхраняват и използват във всяка от тези операционни системи, е различен. Повечето системи са използвали и съхраняват тези файлове във формат на обикновен текст, който може да се чете и редактира, докато други съхраняват в него по-сложен формат, в зависимост от използването на файловете и изискванията на операционната система.

В Unix и Unix-подобни операционни системи, повечето CFG файлове се използват няколко различни стила на формат за CFG файлове, но най-често срещаният формат е лесно четим обикновен текстов формат и почти всички формати позволяват да се правят и редактират коментари. Най-често срещаните файлови разширения за CFG файлове в тези операционни системи са CNF, CONF, CF и INI.

В операционната система MS-DOS първоначално имаше само един конфигурационен файлов формат, а именно обикновен текст, но MS-DOS 6 донесе със себе си въвеждането на INI конфигурационен файлов формат.

macOS използва стандартен конфигурационен файл със стил на формат на списък със свойства.

В Microsoft Windows конфигурационните файлове в стил INI с обикновен текст бяха важен източник за съхранение и редактиране на информация, но през 1993 г. беше въведена нова система от бази данни, което доведе до намаляване на използването на конфигурационни файлове в Microsoft Windows след 1993 г.


## Пример за CFG ##

Примерен CFG файл може да се види по-долу:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```