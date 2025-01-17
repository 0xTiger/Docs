{
  "date" : "2019-12-13",
  "keywords" :[ "pptx файл", "pptx файлов формат", "какво е pptx файл", "файл", "pptx пример", "pptx файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за файловия формат PPTX и API, които могат да създават и отварят PPTX файлове.",
  "title" :"PPTX – файлов формат за презентация на PowerPoint",
  "linktitle" : "PPTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е PPTX файл?

Файловете с разширение PPTX са презентационни файлове, създадени с популярно приложение Microsoft PowerPoint. За разлика от предишната версия на формата на презентационния файл PPT, който беше двоичен, форматът PPTX се основава на отворения XML презентационен формат на Microsoft PowerPoint. Презентационният файл е колекция от слайдове, където всеки слайд може да съдържа текст, изображения, форматиране, анимации и други медии. Тези слайдове се представят на публиката под формата на слайдшоу с персонализирани настройки за представяне.

## Кратка история

Файловият формат PPTX беше въведен през 2007 г. и използва стандарта Open XML, адаптиран от Microsoft през 2000 г. Преди PPTX, често използваният файлов формат беше PPT, който беше чист двоичен файлов формат. Новият тип файл има добавени предимства на малки размери на файлове, по-малко промени на корупция и добре форматирано представяне на изображения. Беше в началото на 2000 г., когато Microsoft реши да направи промяната, за да приспособи стандарта за **Office Open XML**. До 2007 г. този нов файлов формат стана част от Office 2007 и се поддържа и в новите версии на Microsoft Office.

## Спецификации на файлов формат PPTX

Файловете, генерирани с Office Open XML файлов формат, са колекция от XML файлове заедно с други файлове, които осигуряват връзки между всички съставни файлове. Тази колекция всъщност е компресиран архив, който може да бъде извлечен, за да видите съдържанието му. За да направите това, просто преименувайте файловото разширение PPTX с zip и го извлечете, за да наблюдавате съдържанието му (Вижте [спецификации на файловия формат PPTX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/ efd8bb2d-d888-4e2e-af25-cad476730c9f) от Microsoft).

Следващите раздели хвърлят малко светлина върху всеки един от тях.

### [Content_Types].xml

Това е единственият файл, който се намира на базово ниво при извличане на zip. Той изброява типовете съдържание за частите в пакета. Всички препратки към XML файловете, включени в пакета, са посочени в този XML файл. Следва тип съдържание за част от слайд:

```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```

Ако трябва да се добавят нови части към пакета, това може да стане чрез добавяне на новата част и актуализиране на всички връзки в рамките на .rels файловете. Трябва да се има предвид, че за такава промяна трябва да се актуализира и Content_Types.xml.

### \_rels (папка) ###

Връзките между другите части и ресурсите извън пакета се поддържат от частта за връзки. Папката Relationships съдържа един XML файл, който съхранява връзките на ниво пакет. Връзките към ключовите части на PPTX файловете се съдържат в този файл като URI. Тези URI идентифицират типа връзка на всяка ключова част с пакета. Това включва връзката с основния офис документ, разположен като ppt/presentation.xml и други части в рамките на docProps като основни и разширени свойства.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```

Всяка част от документа, която е източник на една или повече релации, ще има своя част за релации, където всяка такава част за релации се намира в подпапка \_rels на частта и се наименува чрез добавяне на '.rels' към името на част. Частта с основното съдържание (presentation.xml) има своя част за връзки (presentation.xml.rels). Той съдържа връзки с други части на съдържанието, като slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, както и URI за външни връзки.

#### Изрична връзка ####

За изрична връзка ресурсът се препраща с помощта на атрибута Id на a<Relationship> елемент. Тоест идентификаторът в източника се свързва директно с идентификатор на елемент на връзка с изрична препратка към целта.

Например един слайд може да съдържа хипервръзка като тази:

```
<a:hlinkClick r:id#"rId2">
```

r:id#"rId2" препраща към следната връзка в рамките на частта за връзки за слайда (slide1.xml.rels).

```
<Relationship Id#"rId2" Type#"http://. . ./hyperlink" Target#"http://www.google.com/" TargetMode#"External"/>
```

#### Неявна връзка ####

За неявна връзка няма такава директна препратка към `<Relationship> ID`. Вместо това препратката се разбира.

### ppt папка ###

Това е основната папка, която съдържа всички подробности за съдържанието на презентацията. По подразбиране има следните папки:

* \_rels
* тема
* слайдове
* slideLayouts
* slideMasters

и следните xml файлове:

* презентация.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Препратки ##

* [[MS-PPTX] - PPTX файлов формат](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-pptx/efd8bb2d-d888-4e2e-af25-cad476730c9f)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

