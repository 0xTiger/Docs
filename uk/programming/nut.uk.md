{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "file", "extension", "file format", "NUT рrоgrаmming lаnguаge", "Programming Guide", "NUT example", "NUT file format", "squirrel language", ".nut extension file ", "файли NUT"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - мовний файл Squirrel",
  "description":"Дізнайтеся про формат файлів NUT та API, які можуть створювати та відкривати файли NUT.",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## Що таке файл NUT?

NUT відноситься до файлу формату відкритого контейнера NUT. Цей формат файлу NUT належить до мови програмування, відомої як Squirrel. Це об’єктно-орієнтована мова програмування високого рівня та імперативна, яка використовується переважно у вбудованих системах та відеоіграх.

Мова squirrel вважається легкою мовою сценаріїв, яку можна легко налаштувати відповідно до розміру та пропускної здатності. Це включає перевагу автоматичного підрахунку посилань і керування сміттям у пам’яті.

Синтаксис мови squirrel приваблює розробників, оскільки він схожий на C і включає особливості мови сценаріїв. Але все-таки він має значно менше переваг порівняно з іншими більш популярними мовами програмування для цієї мети.



## Коротка історія ##

Він був розроблений Альберто Демікелісом у 2003 році. Однак стабільна версія цієї мови була випущена в 2016 році. Вона була розроблена за ліцензією zlib/libpng. У 2010 році ліцензія була змінена і передана MIT. Ця мова вважається натхненною версією [LUA](/uk/programming/lua/) (мова програмування). На веб-сайті, розробленому Альберто, є список пропозицій щодо попередньої мови, щоб зробити її більш вигідною.


## Технічна специфікація ##

Особливостей і характеристик білчиної мови багато. Він забезпечує можливість динамічного типування, властивість делегування, кілька варіантів використання класів та інтерфейсів. Синтаксис цієї мови має схожість із синтаксисом мови Сі. Такі програми, як Enduro/X (кластерний сервер програм), використовують цю мову. Оскільки Squirrel також використовується для відеоігор, деякі з них OpenTTD, GTA IV тощо.

Стабільний випуск мови – 3.0.7. Набір інструментів, відомий як MirthKit, використовує мову програмування Squirrel, щоб створити кросплатформену програму з відкритим кодом для двовимірних ігор. Природа цієї мови є динамічною, а більшість функцій подібні до [Python](/uk/programming/py/), LUA тощо. Вона також передбачає реалізацію віртуальної машини на основі реєстру. Продуктивність Squirrel нижча порівняно з LUA.

Існує також інший тип файлу з розширенням ".nut", тому вам слід подивитися на розмір файлу, щоб дізнатися, який файл NUT у вас є. NUT-файли сценарію Squirrel здебільшого менші за 1 МБ, тоді як відео NUT-файли зазвичай більші за 1 МБ.


## Приклад формату файлу NUT ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## Посилання ##

* [NUT - Вікіпедія](https://en.wikipedia.org/wiki/Squirrel_(programming_language))


