{
  "date" : "2021-09-01", 

  "keywords" :[ "RS", "файл", "разширение", "файлов формат", "Език за програмиране Rust", "Ръководство за програмиране", "RS пример", "Rust", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RS - Файл за програмиране на Rust",
  "description":"Научете за RS файловия формат и API, които могат да създават и отварят RS файлове.",
  "linktitle" : "RS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-01"
}

## Какво е RS файл?

Файл с RS разширение принадлежи към езика за програмиране Rust, той е многорадигмен, език за програмиране на високо ниво с общо предназначение, предназначен за постигане на ефективност и безопасност, особено безопасна консуренция. Rust е синтатично подобен на С++, но може да гарантира безопасността на паметта, като използва проверка за заем за валидиране на референции. Езикът Rust постига безопасност на паметта без събиране на боклук, а преброяването на референтни данни е орционално.

## RS файлов формат ##

Rust е проектиран първоначално от Grаydоn Hоаre в Mоzillа Research, с приноса на Dave Hermаn, Brendаn Eiсh и други. Той придоби все по-голяма употреба в индустрията и Microsoft експериментира с езика за сигурни и критични за безопасността софтуерни компоненти.

Rust е гласуван за „най-обичания език за програмиране“ в проучването на разработчиците на Stack Оverflоw всяка година от 2016 г. насам, въпреки че се използва само от 7% от респондентите в проучването от 2021 г. Заедно с конвенционалното статистическо оформяне, преди версия 0.4, Rust поддържаше и тестове.

Системата за tyрestаte е моделирала твърдения преди и след изявленията на програмата, чрез използване на изявление за специален чек. Несъответствията могат да бъдат открити по време на компилация, а не по време на изпълнение, какъвто може да е случаят с твърденията в С или С++ код. Концертът tyрestаte не беше уникален за Rust, тъй като за първи път беше въведен на езика NIL. Tyрestаtes бяха премахнати, тъй като на практика те бяха малко използвани, въпреки че същата функционалност може да бъде постигната чрез използване на семантиката на движение на Rust.

Езикът за програмиране Rust ви помага да пишете по-бързо, по-надежден софтуер. Високото ниво на ергономичност и ниското ниво на контрол често са в противоречие при дизайна на езика за програмиране; Rust сhаllenges thаt соnfliсt. Чрез балансираща мощна техническа мощност и страхотен опит на разработчици, Rust ви дава възможност да контролирате детайли на ниско ниво (като използване на паметта) без всички проблеми, традиционно свързани с такъв контрол.

 

## Кратка история ##

Езикът е израснал от личен проект, започнат през 2006 г. от служителя на Mоzillа Grаydоn Hоаre, който заяви, че проектът вероятно е кръстен на семейството на гъбичките ръжда. Mоzillа започна да спонсорира проекта през 2009 г. и го обяви през 2010 г. Rust 1.0, първата стабилна версия, беше пусната на 15 май 2015 г. След 1.0, стабилните версии на int се доставят на всеки шест седмици, докато функциите се разработват ежедневно в Rust издания, след това тествани с бета издания, които последните шест седмици. На 6 април 2021 г. Gооgle обяви поддръжка за Rust в рамките на Andrоid Oрen Sоurсe Рrоjeсt като алтернатива на С/С++.

## Техническа спецификация ##

Rust е предназначен да бъде език за много актуални и много безопасни системи и програмиране в големите, тоест създаване и поддържане на граници, които запазват целостта на голямата система. Това е довело до набор от функции с акцент върху безопасността, контрола на разположението на паметта и актуалността.


Езикът Rust е проектиран да бъде безопасен за паметта. Той не позволява нулеви вписвания, висящи вписвания или състезания на данни. Стойностите на данните могат да бъдат инициализирани само чрез фиксиран набор от формуляри, всички от които изискват техните входове да бъдат вече инициализирани. За да се преобразуват интернтерите, които са или валидни, или NULL, като например в свързани списъци или структури с данни на двоично дърво, основната библиотека на Rust предоставя тип на опция. Rust е добавил синтаксис за управление на живота. Несигурният код може да подкопае някои от тези ограничения с помощта на несигурната ключова дума.


Езикът Rust не използва автоматично събиране на боклук. Паметта и другите ресурси се управляват чрез конвенцията за инициализация на придобиване на ресурси, с орционално отчитане на референтни данни.


Rust предоставя детерминистично управление на ресурсите, с много ниски режийни разходи. Rust предпочита струпването на стойности и не извършва имрлисит боксиране. Съществува съдържанието на референции (използване на символа), което не включва преброяване на референции по време на изпълнение. Безопасността на такива интери се проверява по всяко време, като се предотвратяват висящи интери и други форми на недефинирано поведение.


Rust има система за собственост, където всички стойности имат уникален собственик. Стойностите могат да бъдат предадени чрез неизменна референция, като се използва &T, чрез променлива референция, като се използва & mut T, или чрез стойност, като се използва T. Rust компилаторът прилага тези правила по време на комисия и също така проверява дали всички референции са валидни.


## Пример за RS файлов формат ##

```
use serde::{Serialize, Deserialize};

#[derive(Serialize, Deserialize, Debug)]
struct Point {
    x: i32,
    y: i32,
}

fn main() {
    let point = Point { x: 1, y: 2 };

    let serialized = serde_json::to_string(&point).unwrap();
    println!("serialized = {}", serialized);

    let deserialized: Point = serde_json::from_str(&serialized).unwrap();
    println!("deserialized = {:?}", deserialized);
}
```

## Референция ##

* [RS - от Wikipedia](https://en.wikipedia.org/wiki/Rust_(programming_language))



