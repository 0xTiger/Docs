{
"date":"18 июля 2023 г.",
   "keywords":[
"ПАР",
"PAR-файл",
"как открыть номинальный файл",
"файл",
"Расширение файла PAR",
"расширение",
"файл"
],
   "author":{
"display_name":"Шакил Фаиз"
},
"draft": "false",
"toc": true,
"title":"Формат файла PAR — индексный файл архива",
   "description":"Узнайте о формате PAR и API, с помощью которых можно создавать и открывать файлы PAR.",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
"parent": "compression"
}
},
"lastmod":"18.07.2023"
}

## .PAR вариант №

В архивах Parchive (PAR) файл .par относится к индексному файлу, который содержит группу томов или блоков четности. Этот индексный файл используется для обнаружения ошибок и восстановления, когда один или несколько файлов в архиве потеряны или повреждены.

Архив Parchive обычно состоит как из исходных файлов данных, так и из соответствующих томов четности. Тома четности создаются с использованием алгоритмов исправления ошибок Рида-Соломона. Эти тома четности содержат избыточную информацию, которую можно использовать для восстановления исходных файлов данных.

Файл .par, также известный как набор томов четности, содержит информацию о структуре и расположении томов четности в архиве. Он служит индексом или картой процесса восстановления. Используя файл .par, специализированное программное обеспечение PAR может определить, какие тома четности необходимы и как их следует использовать для восстановления отсутствующих или поврежденных файлов.

Когда один или несколько файлов в архиве Parchive становятся недоступными или поврежденными, файл .par можно использовать вместе с доступными томами четности для восстановления потерянных данных. Программное обеспечение PAR считывает файл .par, определяет отсутствующие или поврежденные файлы и использует тома четности для их восстановления.

## Как открыть файл PAR?

Чтобы открывать и использовать файлы .par, вам понадобится специализированное программное обеспечение PAR. Вот несколько популярных вариантов программного обеспечения, которые могут обрабатывать файлы .par:

- **QuickPar:** QuickPar — широко используемое программное обеспечение PAR для Windows. Он позволяет создавать, проверять и восстанавливать файлы PAR. Вы можете открыть файл .par в QuickPar, чтобы проверить его целостность, или использовать его для восстановления поврежденных или отсутствующих файлов в архиве Parchive.

- **MultiPar:** MultiPar – еще одно популярное программное обеспечение PAR, доступное для Windows. Он поддерживает форматы файлов PAR и PAR2 и предоставляет расширенные функции для создания, проверки и восстановления архивов. MultiPar может открывать файлы .par и выполнять операции обнаружения ошибок и восстановления на основе предоставленных томов четности.

- **MacPAR deLuxe:** MacPAR deLuxe — это программное обеспечение PAR, разработанное специально для macOS. Он поддерживает форматы файлов PAR и PAR2 и обеспечивает те же функции, что и QuickPar и MultiPar. MacPAR deLuxe может открывать файлы .par и помогать в проверке архивов и восстановлении поврежденных или отсутствующих файлов.

## Формат файла PAR — дополнительная информация

Формат файла PAR, обычно называемый Parchive, представляет собой особый формат файла, используемый для создания данных четности и выполнения обнаружения ошибок и восстановления в файловых архивах. Формат файла PAR обычно состоит из трех типов: PAR, PAR2 и PAR3.

- **PAR:** Исходный формат файла PAR, также известный как PAR1, был разработан проектом Parchive. Он включает данные о четности, сгенерированные из исходных файлов данных. Файлы PAR обеспечивают базовый уровень обнаружения и восстановления ошибок, но имеют ограничения с точки зрения возможностей исправления ошибок.

- **PAR2:** PAR2 — это улучшенная версия формата файла PAR. Он предлагает более расширенные возможности исправления ошибок и улучшенные функции восстановления. Файлы PAR2 обычно используются для создания данных четности, которые могут восстановить потерянные или поврежденные файлы в архиве. Файлы PAR2 обеспечивают лучшую защиту от повреждения данных и широко используются для архивирования файлов.

- **PAR3:** PAR3 — это последняя версия формата файлов PAR, обеспечивающая дальнейшие улучшения в области исправления и восстановления ошибок. Он предлагает еще более высокий уровень резервирования и возможности исправления ошибок по сравнению с PAR2. Файлы PAR3 предназначены для обеспечения более надежной защиты и восстановления данных, хранящихся в архивах.

Форматы файлов PAR2 и PAR3 широко поддерживаются программным обеспечением PAR и дают возможность проверять целостность файлов в архиве и восстанавливать потерянные или поврежденные данные. Файлы PAR и PAR2 по-прежнему широко используются, тогда как файлы PAR3 постепенно получают распространение благодаря своим расширенным возможностям исправления ошибок.

## Рекомендации
* [Архив](https://en.wikipedia.org/wiki/Parchive)
