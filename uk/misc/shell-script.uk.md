{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Сценарій оболонки – як його запустити в Ubuntu та Linux",
  "description":"Дізнайтеся, що таке Shell Script і як його запускати в Ubuntu і Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-uk",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Що таке Shell Script?

Сценарії оболонки включають написання серії команд у звичайному текстовому файлі, який часто називають **сценарієм оболонки**. Ці сценарії виконуються оболонкою, яка є інтерпретатором командного рядка. До найпоширеніших оболонок відносяться

1. Bash (Bourne Again Shell)
2. Zsh (Z Shell)
3. риба

Сценарії оболонки можуть варіюватися від простих однострокових до складних програм, і вони використовуються для виконання широкого спектру завдань, таких як маніпулювання файлами, адміністрування системи та автоматизація повторюваних завдань.

## Переваги Shell Scripting:

1.  **Автоматизація:** сценарії оболонки дозволяють користувачам автоматизувати повторювані завдання, заощаджуючи час і зменшуючи ймовірність людської помилки.
    
2.  **Налаштування:** Користувачі можуть створювати сценарії, адаптовані до їхніх конкретних потреб, забезпечуючи високий ступінь налаштування.
    
3.  **Пакетна обробка:** Сценарії оболонки чудово підходять для виконання завдань пакетної обробки, коли кілька команд потрібно виконувати послідовно.
    
4.  **Системне адміністрування:** сценарії оболонки зазвичай використовуються для завдань системного адміністрування, таких як резервне копіювання, ротація журналів і встановлення програмного забезпечення.

## Написання простого сценарію оболонки:

Давайте створимо базовий сценарій оболонки, який друкує вітальне повідомлення. Відкрийте текстовий редактор і створіть файл під назвою `greeting.sh`. Додайте такі рядки:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Збережіть файл і зробіть його виконуваним, виконавши таку команду в терміналі:

```
chmod +x greeting.sh
```

Тепер ви можете виконати сценарій:

```
./greeting.sh
```

Результат має бути:

```
Hello, welcome to the world of shell scripting!
```

## Запуск сценаріїв оболонки в Ubuntu та Linux:

Тепер ми обговоримо **як запустити файл .sh в Ubuntu та Linux**.

1.  **Зробіть сценарій виконуваним:** перед запуском сценарію оболонки переконайтеся, що він виконуваний. Використовуйте команду `chmod`, як показано раніше.
    
2.  **Перейдіть до каталогу сценаріїв:** Відкрийте термінал і скористайтеся командою `cd`, щоб перейти до каталогу, що містить ваш сценарій оболонки.
    
3.  **Запустіть сценарій:** Виконайте сценарій, ввівши `./scriptname.sh` у терміналі, замінивши scriptname фактичною назвою вашого сценарію.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Використання команди Bash:** Якщо ваш сценарій починається з `#!/bin/bash` (відомий як **shebang**), ви також можете запустити його за допомогою команди `bash`.

```
bash greeting.sh
```

## Що означає $@ у сценарії оболонки?

У сценарії оболонки `$@` представляє всі аргументи командного рядка, передані сценарію. Його часто використовують для посилання на список аргументів як на окремі сутності. Якщо використовується в подвійних лапках, як-от $@, він зберігає окремі аргументи, враховуючи пробіли та спеціальні символи.

Ось коротке пояснення:

- `$@`: представляє всі позиційні параметри (аргументи), передані сценарію або функції. Кожен аргумент розглядається як окреме слово.
    
- `$@`: у подвійних лапках зберігає розділення аргументів, допускаючи пробіли або спеціальні символи в окремих аргументах.
    

Ось простий приклад для ілюстрації:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Коли ви запускаєте цей сценарій з аргументами, наприклад:

```
bash example.sh arg1 "argument 2" arg3
```

Це виведе:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Як бачите, `$@` представляє всі аргументи, а `$@` зберігає окремі аргументи, навіть якщо вони містять пробіли.
