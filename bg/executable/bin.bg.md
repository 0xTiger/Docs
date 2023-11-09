{
   "date":"2023-07-20",
   "keywords":[
      "BIN",
      "BIN File",
      "file",
      "BIN file extension",
      "extension",
      "file"
   ],
   "author":{
      "display_name":"Shakeel Faiz"
   },
   "draft":"false",
   "toc":true,
   "title":"BIN File Format - Unix Executable File",
   "description":"Научете за формата BIN и API, които могат да създават и отварят BIN файлове.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
         "parent":"executable"
      }
   },
   "lastmod":"2023-07-20"
}

## Какво е BIN файл?

BIN файлът е изпълним файл на базирани на Unix операционни системи като Linux или FreeBSD. Той съдържа компилирана програма, съставена от двоичен код, извлечен от изходния код, което го прави съвместим с основната системна архитектура. Unix Изпълними BIN файлове могат да бъдат сравнени с Windows .EXE файлове и macOS .APP файлове по отношение на тяхната роля като изпълними формати.

В областта на разработката на софтуер за Unix системи BIN файловете обикновено се използват от разработчиците за пакетиране и разпространение на програми. Те предлагат удобно средство за доставяне на софтуер на потребителите, което позволява лесно инсталиране и изпълнение. Наред с BIN файловете съществуват и други типове Unix изпълними файлове, включително [.ELF](/executable/elf/), .X86, [.RUN](/executable/run/) и .X86_64, всеки от които е пригоден за специфичен хардуер или Системни изисквания.

Когато става въпрос за вътрешната структура на BIN файл, той се състои от кодирани данни, които операционната система Unix използва за идентифициране, четене и изпълнение на приложената програма. Системата разчита на специфични файлови подписи или заглавки, за да разпознае BIN файла като изпълним файл, последвано от интерпретация и изпълнение на двоичните инструкции, съдържащи се в него.

BIN файловете често идват в комплект с придружаващ файл **INSTALL.TXT**, който предоставя подробни инструкции как правилно да инсталирате и настроите програмата. Тази документация гарантира, че потребителите могат да навигират успешно в инсталационния процес и да започнат да използват софтуера без усложнения.

## Как да отворя BIN файл?

BIN файловете не са предназначени за директно отваряне и разглеждане. Можете обаче да изпълните програмите или да извлечете данните, които съдържат. За достъп до съдържанието на BIN файл, следвайте тези стъпки в командния ред, като приемете, че името на BIN файла е "sample.bin":

1. **Осигурете изпълними разрешения:**

Преди да изпълните BIN файла, уверете се, че има необходимите разрешения, за да бъде стартиран като изпълним файл. Използвайте командата:

```
$ chmod +x sample.bin
```

Тази команда предоставя на файла изпълними привилегии.

2. **Изпълнете BIN файла:**

След като зададете разрешенията за изпълним файл, можете да стартирате BIN файла, като въведете следната команда:

```
$ ./sample.bin
```

**Внимание**

_Бъдете внимателни, когато работите с изтеглени или изпратени по имейл BIN файлове, тъй като те потенциално могат да бъдат използвани от киберпрестъпници за разпространение на зловреден софтуер. Изпълнявайте само BIN файлове от надеждни източници, за да намалите риска от злонамерени изпълними атаки._

## Други BIN файлове

Ето други типове файлове, които използват файловото разширение **.bin**.

- [BIN - MacBinary Encoded File](/compression/bin/)
- [BIN - Binary Disc Image File](/disc-and-media/bin/)
- [BIN - BlackBerry IT Policy File](/settings/bin/)
- [BIN - Sega Genesis Game ROM](/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/game/bin-pcsx/)

## Препратки

* [How to Execute Binary Files in Linux](https://linuxhint.com/execute-binary-files-in-linux/)
