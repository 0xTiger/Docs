{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Сценарий оболочки — как запустить его в Ubuntu и Linux",
  "description":"Узнайте, что такое Shell Script и как его запустить в Ubuntu и Linux.",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-ru",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Что такое Shell-скрипт?

Создание сценариев оболочки предполагает запись ряда команд в текстовый файл, который часто называют **сценарием оболочки**. Эти сценарии выполняются оболочкой, которая представляет собой интерпретатор командной строки. К наиболее распространенным оболочкам относятся

1. Баш (Bourne Again Shell)
2. Зш (Z Shell)
3. Рыба.

Сценарии оболочки могут варьироваться от простых однострочных строк до сложных программ и используются для выполнения широкого спектра задач, таких как манипулирование файлами, системное администрирование и автоматизация повторяющихся задач.

## Преимущества сценариев оболочки:

1.  **Автоматизация.** Скрипты оболочки позволяют пользователям автоматизировать повторяющиеся задачи, экономя время и снижая вероятность человеческой ошибки.
    
2.  **Настройка.** Пользователи могут создавать сценарии с учетом своих конкретных потребностей, обеспечивая высокую степень настройки.
    
3.  **Пакетная обработка.** Скрипты оболочки отлично подходят для выполнения задач пакетной обработки, когда необходимо последовательно выполнить несколько команд.
    
4.  **Системное администрирование.** Сценарии оболочки обычно используются для задач системного администрирования, таких как резервное копирование, ротация журналов и установка программного обеспечения.

## Написание простого сценария оболочки:

Давайте создадим базовый сценарий оболочки, который печатает приветственное сообщение. Откройте текстовый редактор и создайте файл с именем «greeting.sh». Добавьте следующие строки:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Сохраните файл и сделайте его исполняемым, выполнив в терминале следующую команду:

```
chmod +x greeting.sh
```

Теперь вы можете выполнить скрипт:

```
./greeting.sh
```

Результат должен быть:

```
Hello, welcome to the world of shell scripting!
```

## Запуск сценариев оболочки в Ubuntu и Linux:

Теперь мы обсудим **как запустить файл .sh в Ubuntu и Linux**.

1.  **Сделайте сценарий исполняемым.** Прежде чем запускать сценарий оболочки, убедитесь, что он является исполняемым. Используйте команду chmod, как показано ранее.
    
2.  **Перейдите в каталог сценариев:** Откройте терминал и используйте команду `cd`, чтобы перейти к каталогу, содержащему ваш сценарий оболочки.
    
3.  **Запустите скрипт:** Запустите скрипт, набрав `./scriptname.sh` в терминале, заменив «scriptname» фактическим именем вашего скрипта.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Использование команды Bash:** Если ваш скрипт начинается с `#!/bin/bash` (известного как **shebang**), вы также можете запустить его с помощью команды `bash`.

```
bash greeting.sh
```

## Что означает $@ в сценарии Shell?

В сценарии оболочки `$@` представляет все аргументы командной строки, передаваемые в сценарий. Он часто используется для ссылки на список аргументов как на отдельные сущности. При использовании в двойных кавычках, например `$@`, сохраняются отдельные аргументы с учетом пробелов и специальных символов.

Вот краткое объяснение:

- `$@`: представляет все позиционные параметры (аргументы), передаваемые в скрипт или функцию. Каждый аргумент рассматривается как отдельное слово.
    
- `$@`: при двойных кавычках сохраняется разделение аргументов, позволяя использовать пробелы или специальные символы внутри отдельных аргументов.
    

Вот простой пример для иллюстрации:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Когда вы запускаете этот скрипт с аргументами, например:

```
bash example.sh arg1 "argument 2" arg3
```

Это выведет:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Как видите, `$@` представляет все аргументы, а `$@` сохраняет отдельные аргументы, даже если они содержат пробелы.
