{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу BML - файл мови розмітки Bean",
  "description":"Дізнайтеся про формат файлу BML та API, які можуть створювати та відкривати файли BML.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Що таке файл BML?

Файл із розширенням .bml — це файл мови розмітки Bean, який зберігає класи Java для підтримки програм Java. Це дозволяє отримати доступ до об’єктів і методів Java і не потребує створення нових функцій за допомогою класів Java. Він визначає, як компоненти з’єднані один з одним для виконання корисних завдань. BML був розроблений IBM alphaWorks для опису зв’язків структур і компонентів. Файли BML можна відкривати та переглядати за допомогою будь-якого текстового редактора, такого як веб-браузери, Microsoft Notepad і Notepad++.

## Формат файлу BML

Веб-сайт IBM alphaworks надав дві реалізації BML. Перша реалізація — це інтерпретатор, який «відтворює» сценарій BML для генерації бажаної ієрархії компонентів. Друга реалізація — це компілятор, який компілює будь-який сценарій BML у код Java без відображення. Це вигідно в тому сенсі, що дозволяє отримувати міжкомпонентну структуру програми за допомогою мови, розробленої для цієї конкретної мети, з доданою можливістю компілювати її в «звичайний» код Java.

## Теги BML

Нижче наведено пояснення деяких тегів, які використовуються в мові BML:

### The<bean> тег:

The<bean> елемент використовується для створення нових компонентів або для пошуку компонентів за назвою. The<bean> тег має такий формат:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
«ID» у тегу пов’язано з реєстром об’єктів для JavaBean.

### The<string> тег

Існує два способи використання рядкового тегу:

1. Щоб створити непорожній рядок:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Щоб створити порожній рядок:

```
<string/>
```
## Список літератури

* [Об’єктно-орієнтований обмін повідомленнями з XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Мова фізичної розмітки](http://web.mit.edu/mecheng/pml/standards.htm)


