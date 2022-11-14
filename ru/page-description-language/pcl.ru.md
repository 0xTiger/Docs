{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ПКЛ",
  "description":"Узнайте о формате файла PCL и API-интерфейсах, которые могут создавать и открывать файлы PCL.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## .PCL вариант № ##

PCL означает язык команд принтера, который представляет собой язык описания страниц, представленный Hewlett Packard (HP). Компания HP создала PCL, чтобы обеспечить эффективный способ управления функциями принтера на различных печатающих устройствах. Первоначально формат был разработан для матричных и струйных принтеров HP, но с течением времени стал частью различных термопринтеров, матричных и страничных принтеров. Формат претерпел несколько различных изменений, в результате чего были созданы разные версии, каждая из которых была улучшена, чтобы соответствовать требованиям времени в отношении функций управления принтером. На сегодняшний день PCL является наиболее распространенным языком печати на рынке принтеров для ластчерных принтеров.

## Версии PCL ##

Версии PCL различаются функциональностью (например, поддержка типов шрифтов: растровые шрифты, масштабируемые шрифты (шрифты Intellifonts, TrueType), методы сжатия растровой графики, поддержка графики HP-GL/2).

**PCL 1:** примерно в 1980 году. Функциональность «Печать и пробел» — это базовый набор функций, предназначенных для простого и удобного вывода на однопользовательскую рабочую станцию.

**PCL 2:** около 1980 г. — EDP (электронная обработка данных)/функции транзакций являются надмножеством PCL 1. Были добавлены функции общего назначения, многопользовательской системной печати.

**PCL 3**: 1984 г. — функциональные возможности обработки текстов Office являются расширенным набором функций PCL 2. Были добавлены функции для создания высококачественных офисных документов и увеличено разрешение до 300 dpi. Это позволяло использовать ограниченное количество растровых шрифтов и графики и поддерживало HP-GL. PCL 3 широко копировался другими производителями принтеров, и эти компании называли его «Эмуляция LaserJet Plus».
(Принтеры: семейство HP DeskJet, принтер серии HP LaserJet, принтер серии HP LaserJet Plus)

**PCL3+:** Используется принтерами семейства DeskJet и DesignJet.

**PCL3c:** Используется принтерами семейства DeskJet и DesignJet.

**PCL3e**: используется принтерами семейства DeskJet и DesignJet. Теперь используется и в PhotoSmart.

**PCL3GUI**: использует RTL и используется принтерами семейства DeskJet и DesignJet.

**PCLSLEEK**: использует RTL и используется принтерами семейства DeskJet и DesignJet.

**PCL 4**: 1985. Функции форматирования страниц являются расширенным набором функций PCL 3. Поддерживаются макросы, более крупные растровые шрифты и графика. (Принтеры: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 — Функциональность Office Publishing является расширенным набором функций PCL 4. Новые возможности публикации включают масштабирование шрифтов и графику HP-GL/2 (векторную). (Принтеры: HP LaserJet III)

**PCL 5e:** 1994 — это основная версия, которая включает новые функции, такие как адаптивная система сжатия, 2-байтовая кодировка символов, поддержка векторных шрифтов и двунаправленные команды настройки. Включает логические операции (соответствует ROP GDI) для улучшения поддержки Windows перед обрезкой путей. (Принтеры: HP LaserJet 4)

**PCL 5j:** Новые функции, такие как поддержка 2-байтовых символов для японских резидентных масштабируемых шрифтов, вертикальное письмо, размеры японской бумаги и строки шрифтов. (Принтеры: HP LaserJet 4PJ)

**PCL 5c:** 1995 г. — в PCL5 добавлена поддержка цвета и логические операции. PCL5c предшествует PCL5e. Некоторые модели также поддерживают обтравочные контуры. (Принтеры: HP Color LaserJet, HP PaintJet 300 XL (первый принтер с PCL5c), HP DeskJet 1200C/1600C (эти номера моделей использовались повторно, а более новые модели не относятся к PCL 5c)

**PCL 5ce:** поддерживает масштабируемые шрифты Agfa Microtype. (Принтеры: принтер HP 2500c Pro)

**PCL 6 / XL:** 1996 г. — PCL 6 или PCL XL — это новый формат, представленный в 1995 г., который несовместим ни с какими предыдущими версиями PCL. (Принтеры: HP LaserJet 5, 5M и 5N)

## Обзор PCL 6 ##

HP представила PCL 6 в 1996 году, который стал следующей эволюцией языка PCL и связанных с ним технологий. Он имеет следующие компоненты:

**PCL 6 Enhanced:** предоставляет оптимизированную версию для печати из графических пользовательских интерфейсов (GUI), таких как MS Windows и OS/2.

**Стандарт PCL 6:** обеспечивает полную обратную совместимость с предыдущими принтерами HP LaserJet.

**Синтез шрифтов PCL:** обеспечивает масштабируемые шрифты, управление шрифтами и хранение форм и шрифтов.

Расширенная версия PCL XL ближе к GDI, который используют многие приложения. Это гарантирует, что будет выполняться меньше переводов, что приведет к расширению возможностей WYSIWYG и повышению производительности с приложениями, которые поддерживают escape-последовательности, реализованные с помощью расширенного драйвера. Выходные данные драйвера Enhanced (PCL XL) могут отличаться от выходных данных стандартного драйвера. Если вывод не соответствует ожидаемому, выберите стандартный драйвер (PCL5e).

Команды PCL 6 Enhanced созданы для оптимального соответствия требованиям графической печати для приложений с графическим интерфейсом. В большинстве случаев для каждой команды печати графики, которую хочет выполнить графический интерфейс, существует соответствующая команда PCL 6 Enhanced. Это уменьшает количество команд, необходимых для описания графической страницы. Каждая команда в PCL 6 Enhanced предназначена для минимальной передачи данных с хост-компьютера на принтер. Это уменьшает количество данных, необходимых для описания страницы.

Система печати Windows для большинства принтеров HP LaserJet содержит два отдельных драйвера: стандартный и расширенный. Драйвер Standard обеспечивает обратную совместимость, используя команды стандарта PCL 6 (PCL5e) для печати простого текста или страниц смешанного текста и графики. Драйвер Enhanced использует расширенные команды PCL 6, оптимизированные для печати сложных графических страниц.

## Редакции класса PCL 6 ##

#### Класс 1.1 ####

**Инструменты рисования:** Поддержка рисования линий, дуг/эллипсов/хорд, (скругленных) прямоугольников, многоугольников, контуров Безье, обрезанных контуров, растровых изображений, линий сканирования, растровых операций.
**Обработка цвета:** Поддержка 1/4/8-битных палитр, цветовое пространство RGB/серое. Поддержка пользовательских шаблонов полутонов (максимум 256 шаблонов).
**Сжатие:** Поддерживает RLE.
**Единицы измерения:** дюймы, миллиметры, десятые доли миллиметра.
** Работа с бумагой: ** поддержка настраиваемых или предопределенных наборов типов бумаги, включая обычные Letter, Legal, A4 и т. д. Можно выбрать бумагу из ручной подачи, лотков, кассет. Бумага может быть двусторонней по горизонтали или по вертикали. Бумага может быть ориентирована в книжной, альбомной ориентации или с поворотом на 180 градусов из первых двух.
**Шрифт:** Поддерживает растровые шрифты или шрифты TrueType, 8- или 16-битные кодовые точки. При выборе набора символов используется код набора символов, отличный от PCL 5. При использовании растрового шрифта многие команды масштабирования недоступны. При использовании шрифта TrueType дескрипторы переменной длины, блоки продолжения не поддерживаются. Контурный шрифт можно поворачивать, масштабировать или обрезать.

#### Класс 2.0 ####

**Сжатие:** добавлено собственное сжатие JPEG под названием JetReady.
**Обработка бумаги:** Носители можно перенаправлять в разные выходные лотки (до 256). Добавлены предустановленные размеры носителей A6 и B6 для японского языка. Добавлен пресет «Третья кассета», 248 источников внешнего лотка.
**Шрифт:** Текст можно писать вертикально.

#### Класс 2.1 ####

**Обработка цвета:** добавлена функция сопоставления цветов.
**Сжатие:** Добавлен ряд дельты.
**Обработка бумаги:** Ориентация и размер носителя не являются обязательными при объявлении новой страницы. Добавлены типы бумаги B5, JIS 8K, JIS 16K, JIS Exec.

#### Класс 3.0 ####

**Обработка цвета:** Разрешить использование различных настроек полутонов для векторной или растровой графики, текста. Поддерживает адаптивный полутон.
**Протокол:** поддерживает сквозную передачу PCL, позволяя использовать функции PCL 5 в потоках PCL 6. Однако при использовании этой функции некоторые состояния PCL 6 не сохраняются.
**Шрифт:** Поддерживает шрифты PCL.
**Просмотр/преобразователь:** PCLReader (бесплатное ПО) может просматривать, преобразовывать или печатать файлы PCL 6 любого уровня (включая JetReady) на любом принтере.

## Использованная литература ##

* [PCL — Википедия] (https://en.wikipedia.org/wiki/Printer_Command_Language)
