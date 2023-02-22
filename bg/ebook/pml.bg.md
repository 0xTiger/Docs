{
  "date" : "2021-03-08",
  "keywords" :[ "PML", "eReader", "разширение", "формат", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете повече за PML файловия формат, Palm Markup Language и API, които могат да създават и отварят PML файлове.",
  "title" :"PML - Palm Markup Language File",
  "linktitle" : "PML",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Какво е PML файл?

Palm Inc представи файловия формат PML, който означава Palm Markup Language File. Целта му е да създава документи за eReader, което е устройство за четене на електронни книги, подобно на таблетния компютър. PML файлът дава оформлението на [PDB](/bg/ebook/pdb/) файл (съдържащ различни файлове с данни) за показване на Palm устройство.

## Технически подробности за PML файловете

Структурата на PML файловете се състои от тагове за създаване на настройка на електронна книга, включително параграфи, заглавия, отстъпи и препратки. Той също така позволява етикети за форматиране, като Bold, Small Caps и Superscript. Разработчиците могат също да добавят изображения към електронните книги.

### Palm Markup Language
Следната таблица определя PML командите:

|Команда|Описание|
---|---|
| \p | Нова страница |
| \x | Нова глава; също предизвиква нов прекъсване на страницата. Оградете заглавието на глава (и всякакви стилови кодове) с \x и \x |
| \Xn | Нова глава, n нива с отстъп (n между 0 и 4 включително) в диалоговия прозорец Глава; не предизвиква прекъсване на страницата. Оградете заглавието на глава (и всякакви стилови кодове) с \Xn и \Xn |
| \Cn="Заглавие на глава" | Вмъкнете „Заглавие на глава“ в списъка с глави с ниво n (като \Xn). Текстът не се показва на страницата и не налага прекъсване на страницата. Това понякога може да бъде полезно за вмъкване на знак за глава в началото на въведение към главата, например. |
| \c | Центрирайте този блок от текст; затворете с \c в началото на реда |
| \r | Дясно подравняване на текстов блок; затворете с \r в началото на реда |
| \i | Курсив блок; затворете с \i |
| \u | Блок за подчертаване; затворете с \u |
| \o | Overstrike блок; затворете с \o |
| \v | Невидим текст; затворете с \v (може да се използва за коментари) |
| \t | Блок с отстъп. Започнете в началото на ред, затворете с \t в края на ред |
| \T="50%" | Прави отстъп в определения процент от ширината на екрана, в този случай 50%. Ако текущата позиция на чертеж вече е след определеното местоположение на екрана, този етикет се игнорира. |
| \w="50%" | Вградете хоризонтална линия с даден процент ширина на екрана, в този случай 50%. Този таг предизвиква прекъсване на ред преди и след него. Правилото е центрирано. Знакът за процент е задължителен. |
| \n | Превключете към "нормален" шрифт, който е зададен от потребителя |
| \s | Превключете към stdFont; затворете с \s, за да се върнете към нормален шрифт |
| \b | Превключете към boldFont; затворете с \b, за да се върнете към нормален шрифт (отхвърлен; вместо това използвайте \B) |
| \l | Превключете към largeFont; затворете с \l, за да се върнете към нормален шрифт |
| \B | Маркирайте текста като удебелен. За разлика от тага \b, \B не променя шрифта, така че можете да имате голям удебелен текст. Не можете да смесвате \b и \B в един и същи PML файл. |
| \Sp | Маркирайте текста като горен индекс. Не трябва да се смесва с други стилове като удебелен шрифт, курсив и т.н. Оградете надписния текст с \Sp. |
| \Sb | Маркирайте текста като долен индекс. Не трябва да се смесва с други стилове като получер, курсив и т.н. Оградете текста с индекси \Sb. |
| \k | Направете оградения текст с малки главни букви; затворете с \k. Всички символи, затворени в \k тагове (включително тези с ударения), се правят с главни букви и се изобразяват с по-малък размер на точка от обикновените главни букви. |
| \\ | Представлява една обратна наклонена черта |
| \aXXX | Вмъкнете не-ASCII знак, чийто Windows-1252 код е десетичен XXX. Вижте таблицата със знаци на PML за подробности. |
| \UXXXX | Вмъкнете не-ASCII знак, чийто Unicode код е шестнадесетичен XXXX. Вижте разширената PML таблица със знаци за подробности. |
| \m="име на изображение.png" | Вмъкнете изображението с име. Вижте раздела за изображения по-долу. |
| \q="#linkanchor"Малко текст\q | Позоваване на котва за връзка, която е на друго място в документа. Низът след спецификацията на котва и преди завършващия \q е подчертан или по друг начин показан като връзка, когато преглеждате документа. |
| \Q="linkanchor" | Посочете котва за връзка в документа. |
| \- | Поставете меко тире. Меко тире се показва само ако е необходимо да се прекъсне дума в ред. |
| \Fn="бележка под линия1"1\Fn | Свържете „1“ към бележка под линия, чието име е бележка под линия 1, маркирана в края на PML документа. Вижте раздела за бележки под линия и странични ленти по-долу. |
| \Sd="sidebar1"Странична лента\Sd | Свържете текста „Sidebar“ към странична лента, чието име е sidebar1, маркирана в края на PML документа. Вижте раздела за бележки под линия и странични ленти по-долу. |
| \I | Маркирайте като референтен индексен елемент. Оградете индексния елемент (и всички стилови кодове) с \I и \I.|
 


## Препратки

* [Език за маркиране на Palm - от MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [Електронен четец - от MobileRead](https://en.wikipedia.org/wiki/E-reader)
