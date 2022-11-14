{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "файл amf", "формат файла amf", "формат файла", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файла AMF и API-интерфейсах, которые могут открывать и создавать файлы AMF.",
  "title" :"AMF - Файл аддитивного производства",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .AMF вариант №
Файл AMF состоит из руководств по описанию объектов для использования в процессах аддитивного производства. Он содержит открытие<amf> XML-тег и заканчивается</amf> элемент. Этому предшествует строка объявления XML, указывающая версию XML и кодировку файла. Объявления могут включать информацию о единицах измерения, а при отсутствии такой информации в качестве единицы измерения по умолчанию используются миллиметры.


## Формат файла AMF

Формат файла аддитивного производства (**AMF**) определяет открытые стандарты описания объектов для использования в процессах аддитивного производства, таких как 3D-печать. Программы САПР используют формат файла AMF, используя такую информацию, как геометрия, цвет и материал объектов. Формат AMF отличается от формата STL, поскольку латеральный формат не поддерживает цвет, материалы, решетки и созвездия.

### Элементы файла AMF

Пять элементов верхнего уровня, определенные с помощью<AMF> теги описаны ниже. Наличие одного элемента объекта является обязательным для полнофункционального файла AMF.

`<object> ` — элемент объекта определяет объем или объемы материала, каждый из которых связан с идентификатором материала для печати. В файле должен присутствовать хотя бы один объектный элемент. Дополнительные объекты необязательны.

`<material> ` — необязательный элемент материала определяет один или несколько материалов для печати с соответствующим идентификатором материала. Если элемент материала не включен, предполагается один материал по умолчанию.

`<texture> ` — необязательный элемент текстуры определяет одно или несколько изображений или текстур для отображения цвета или текстуры, каждое из которых имеет соответствующий идентификатор текстуры.

`<constellation> ` — необязательный элемент созвездия иерархически объединяет объекты и другие созвездия в относительный шаблон для печати.

`<metadata> ` — необязательный элемент метаданных указывает дополнительную информацию об объекте (объектах) и элементах, содержащихся в файле.

## Пример AMF

Ниже приведен пример файла AMF, который можно скопировать в файл [text](/ru/word-processing/txt/) и сохранить как сжатый файл [zip](/ru/compression/zip/) для открытия.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## использованная литература

* [AMF - Википедия](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [Спецификации AMF по ISO] (https://www.iso.org/standard/67472.html)
