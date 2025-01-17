{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "файл", "файлов формат", "Език за описание на страницата", "Скалар" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за SVG файловия формат и API, които могат да създават и отварят SVG файлове.",
  "title" :"Какво е SVG файл?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Какво е SVG файл? ##

SVG файлът е файл със скаларна векторна графика, който използва базиран на XML текстов формат за описание на външния вид на изображение. Думата мащабируем се отнася до факта, че SVG може да бъде мащабиран до различни размери, без да губи никакво качество. Текстовото описание на такива файлове ги прави независими от резолюцията. Това е един от най-използваните формати за изграждане на уебсайт и печат на графики с цел постигане на мащабируемост. Форматът обаче може да се използва само за двуизмерна графика. SVG файловете могат да се разглеждат/отварят в почти всички съвременни браузъри, включително Chrome, Internet Explorer, Firefox и Safari.

## Кратка история ##

SVG спецификациите са достъпни като отворен стандарт от World Wide Web Consortium (W3C) от 1999 г. Преди това подобни спецификации на файлов формат в шест различни формата бяха изпратени на W3C до 1998 г. Актуализация беше приложена към спецификациите през 2011 г. и беше версия 1.1 . През 2016 г. SVG 2 беше публикуван като по-нова версия, включваща функции в допълнение към тези в SVG 1.1.

## Спецификации на файловия формат ##

SVG Document Object Model (DOM) полага основите за всички спецификации и интерфейси, които съответстват на конкретните раздели на спецификациите. SVG зрителите трябва да внедрят SVG DOM интерфейсите, както е дефинирано в спецификациите на W3C. Неговият DOM излага няколко интерфейса за различни типове данни и елементи.

### SVG форми ###

SVG има някои предварително дефинирани фигурни елементи, които могат да се използват от разработчиците:

* Правоъгълник<rect>
* Кръг<circle>
* Елипса<ellipse>
* Линия<line>
* Полилиния<polyline>
* Многоъгълник<polygon>
* Пътека<path>

Въз основа на тези форми и спецификации функционалните области на SVG са както следва.

**Пътища** - Пътищата се използват за представяне на прости, както и на сложни контури на фигури. Кодирането се използва за определяне на естеството на операцията. Например M се използва за Преместване към, L се използва за Линия към, Z се използва за затваряне на път и т.н.

**Основни фигури** - Могат да се чертаят праволинейни пътеки и пътеки, съставени от поредица от свързани сегменти с права линия (полилинии), както и затворени многоъгълници, кръгове и елипси. Правоъгълниците и правоъгълниците със заоблени ъгли също са стандартни елементи.

**Текст** - Текстовото представяне се изразява като XML знакови данни, където могат да се приложат много визуални ефекти към текста. Спецификациите позволяват обработка на двупосочен текст, вертикален текст и знаци по извита траектория.

**Рисуване** - Формите могат да бъдат запълнени и/или очертани с цвят, градиент или шарка, което позволява възможността да се направи непрозрачно или да има всякаква степен на прозрачност. Характеристики в края на линията, като върхове на стрелки или символи, появяващи се във върховете на многоъгълник, са представени от маркери.

**Цвят** - SVG спецификациите позволяват да се прилагат цветове към всички видими SVG елементи, директно или чрез запълване, щрих и други свойства. Могат да се използват различни цветови кодове за уточняване като черно или синьо, шестнадесетично представяне, десетично или като проценти от формата RGB.

**Градиенти и шарки** - Формите в SVG файл могат да бъдат запълнени или очертани с плътни цветове, градиенти или повтарящи се шарки.

**Ефекти на филтъра** - Това всъщност е поредица от графични операции, които се прилагат към дадена изходна векторна графика, за да се получи модифициран резултат.

**Интерактивност** - Потребителите могат да взаимодействат със SVG файлове чрез промяна на фокуса, щракване на мишката, превъртане или мащабиране на изображението. Интерактивността позволява на SVG изображенията да взаимодействат с потребителите по много различни начини, както беше споменато по-горе.

**Свързване** - Възможно е SVG изображенията да имат хипервръзки към други документи. Това се постига чрез XML Linking Language или XLink. Това позволява създаване на специфични състояния на изглед, които се използват за увеличаване/намаляване на конкретна област или за ограничаване на изгледа до конкретен елемент.

**Скриптове** - Подобно на HTML, всички аспекти на SVG документ са достъпни за манипулиране с помощта на скриптове. SVG DOM обектите предоставят насоки за постигане на това с помощта на SVG елемент и атрибут. Скриптовете са затворени в елементи на таг `script` и могат да се изпълняват в отговор на показалец, клавиатура или събития в документа, ако е необходимо.

**Анимация** - DOM елементите<animate> ,<animateMotion> и<animateColor> ви позволява да включите анимация за SVG съдържание. Разбира се, това не е постижимо без използване на скриптове и вградени таймери. Тези анимации могат да бъдат непрекъснати и могат да се поставят на цикъл, както и да се повтарят, като в същото време отговарят на потребителски събития.

**Шрифтове** – Текстът в SVG може да препраща към външни файлове с шрифтове, като например системни шрифтове. При липса на такива шрифтове текстът в SVG няма да бъде изобразен в изхода. Това може да се преодолее чрез включване на необходимите глифове в такъв файл като шрифт, който след това се изобразява с помощта на<text> елемент.

## Примери ##
Следващите редове показват как кръгът е представен с помощта на SVG скрипта.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Следващите редове код показват как да използвате<text> блок за изобразяване на текст в SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Препратки ##

* [W3C SVG спецификации](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG – Уикипедия](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

