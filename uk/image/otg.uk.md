{
  "date" : "2020-01-10",
  "keywords" :[ "файл otg", "формат файлу otg", "що таке файл otg", "файл", "приклад otg", "розширення файлу otg", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - формат файлу шаблону креслення OpenDocument",
  "description":"Дізнайтеся про формат файлу OTG та API, які можуть створювати та відкривати файли OTG.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Що таке файл OTG?

Файл OTG – це шаблон малюнка, який створюється за допомогою стандарту OpenDocument, який відповідає специфікації OASIS Office Applications [1.0](http://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0 -os.pdf). Він представляє стандартну організацію елементів малюнка для векторного зображення, яке можна використовувати для подальшого вдосконалення вмісту файлу. Файли OTF, як і будь-які інші файли на основі формату OpenDocument, засновані на форматі XML для представлення вмісту документа. Файли OTF можна переглянути, відкривши їх у будь-якому текстовому або стандартному редакторі XML.

## Специфікації формату файлу OTG ##

Формат файлу OTG базується на форматі OpenDocument XML, який має добре встановлену схему. Структура кожного компонента формату OpenDocument представлена елементом, який має пов’язані атрибути та є спільним для всіх типів документів, таких як текстовий документ, електронна таблиця або файл малюнка. OTG, будучи шаблоном малювання, широко використовує специфікації графічного вмісту, що включає:

* Розширені функції сторінки для графічних програм
* Малювання фігур
* Рамки
* 3D фігури
* Спеціальна форма
* Форми презентації
* Презентаційні анімації
* Анімація презентації SMIL
* Презентаційні події
* Наявність текстових полів
* Зміст презентаційного документа

### Розширені функції сторінки для графічних програм ###
#### Майстер роздаткового матеріалу ####

Елемент Handout Master — це шаблон для автоматичного створення сторінок роздаткового матеріалу для програм, які підтримують друк таких сторінок.
Атрибути, які можуть бути пов’язані з `<style:handout-master> ` є:

|Макет|Атрибут|Опис
---|---|---|
|Макет сторінки презентації|presentation:presentation-page-layout-name|Посилання на `<style:presentation-page-layout> ` атрибут
|Макет сторінки|`style:page-layout-name` | Визначає макет сторінки, який містить розміри, межі та орієнтацію шаблонної сторінки роздаткового матеріалу.
|Стиль сторінки|`draw:style-name`|Призначає додаткові атрибути форматування шаблонній сторінці роздаткового матеріалу, призначаючи стиль сторінки малюнка.|
|Заголовок декларації| `presentation:use-header-name`| Вказує ім’я оголошення поля заголовка, яке використовується для всіх полів заголовка, які відображаються на головній сторінці роздаткового матеріалу.
|Нижній колонтитул декларації| presentation:use-footer-name|Вказує ім’я оголошення поля нижнього колонтитула, яке використовується для всіх полів нижнього колонтитула, які відображаються на головній сторінці роздаткового матеріалу.
|Оголошення дати й часу|use-date-time-name|Вказує ім’я оголошення поля дати й часу, яке використовується для всіх полів дати й часу, які відображаються на головній сторінці роздаткового матеріалу.

### Малювання фігур ###
Формат OpenDocument підтримує декілька форм малюнка, які можна використовувати в будь-якому типі документа.

|Форма|Пов'язані атрибути| елементів
---|---|---|
Прямокутник - `<draw:rect> `|Позиція, розмір, стиль, шар, Z-індекс, ідентифікатор, ідентифікатор підпису, прив’язка тексту, фон таблиці, кінцева позиція малювання, закруглені кути|заголовок, довгий опис, слухачі подій, точки зчеплення, текст
Лінія `<draw:line> `|Стиль, шар, Z-індекс, ідентифікатор, ідентифікатор підпису та трансформація, прив’язка тексту, фон таблиці, кінцева позиція малювання, початкова точка, кінцева точка|заголовок, довгий опис, прослуховувачі подій, точки зчеплення, текст
Ломана `<draw:polyline> `| Позиція, розмір, поле перегляду, стиль, шар, Z-індекс, ідентифікатор, ідентифікатор підпису та трансформація, прив’язка тексту, фон таблиці, кінцева позиція малювання, точки| Заголовок, довгий опис, слухачі подій, точки зчеплення, текст
Багатокутник `<draw:polygon> `|Позиція, розмір, вікно перегляду, стиль, шар, Z-індекс, ідентифікатор, ідентифікатор підпису та трансформація, прив’язка тексту, фон таблиці, кінцева позиція малювання, точки|заголовок, довгий опис, слухачі подій, точки з’єднання, текст
|Правильний многокутник `<draw:regular-polygon> `|Позиція, розмір, стиль, шар, Z-індекс, ідентифікатор, ідентифікатор підпису та трансформація, прив’язка тексту, фон таблиці, кінцева позиція малювання, увігнутість, кути, чіткість|заголовок, довгий опис, слухачі подій, точки зчеплення, текст
|Paht `<draw:path> `|Положення, розмір, поле перегляду, стиль, шар, Z-індекс, ідентифікатор, ідентифікатор підпису та трансформація, прив’язка тексту, фон таблиці, кінцева позиція малювання, дані шляху| Заголовок, довгий опис, слухачі подій, точки зчеплення, текст

### Рамки ###
Рамка в документі креслення — це прямокутний контейнер, який містить текстові поля, зображення або об’єкти. Рамки підтримують додаткові функції, такі як контури, карти зображень і гіперпосилання. Кадр може містити як об’єкт, так і зображення, що дозволяє мати кілька відтворень об’єкта. Програми відтворюють відповідний елемент на основі найкращої підтримки.

Рамки можуть містити:
* Текстові поля
* Об’єкти, представлені у форматі OpenDocument або в окремому двійковому форматі
* Зображення
* Аплети
* Плагіни
* Плаваючі рамки

Рамка міститься в документі, як показано нижче.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## Посилання ##
* [Формат відкритих документів OASIS для офісних програм](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Формат OpenDocument – Вікіпедія](https://en.wikipedia.org/wiki/OpenDocument)
