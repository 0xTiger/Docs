{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc","що таке файл arsc","як відкрити файл arsc", "розширення", "файл", "файл arsc","формат файлу arsc", "розширення файлу arsc" ,"приклад файлу arsc"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - файл таблиці ресурсів пакета Android",
  "description":"Дізнайтеся про формат файлу ARSC та API, які можуть створювати та відкривати файл ARSC.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Що таке файл ARSC?

Файл ARSC — це файл таблиці ресурсів Android, який містить список ресурсів програми у форматі таблиці. Він містить таку інформацію, як назви ресурсів, властивості та ідентифікатори. Файли ARSC є частиною пакетів APK, які використовуються для встановлення цих програм Android. Усі ресурси, такі як зображення, макети, стилі та рядки, у програмі Android перетворюються на двійкові файли під час створення файлу APK. Також одночасно створюється файл ARSC, який містить список усіх скомпільованих ресурсів програми та їх ідентифікатори.

## Формат файлу ARSC

Файли розширення .arsc — це двійкові файли, створені після того, як компілятор, наприклад ANT (Eclipse) або Gradle (AS), компілює код програми Android для створення файлу [APK](/uk/compression/apk/). Ви можете розпакувати файл APK за допомогою будь-якої утиліти архівування, наприклад WinZip, щоб переглянути його вміст, який є скомпільованими файлами класів Java, тобто classes.dex. На додаток до них, він також містить цей файл ARSC, який містить метаінформацію про:

* Вузли XML
* Атрибути
* Ідентифікатори ресурсів

Ресурси у файлі APK посилаються за ідентифікаторами ресурсів, тоді як атрибути перетворюються на значення під час виконання. Інструмент Android aapt збирає всі ресурси, визначені у файлах під час створення, і призначає їм ідентифікатори ресурсів. Після того, як скомпільованим ресурсам присвоєно ідентифікатори, з вихідного коду, а також з resources.arsc створюється файл R.java.

## Список літератури

* [Структура двійкової таблиці ресурсів](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

