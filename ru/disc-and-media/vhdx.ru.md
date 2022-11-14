{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Узнайте о формате файла VHDX и API-интерфейсах, которые могут создавать и открывать файлы VHDX.",
  "title" :"Формат файла VHDX — что такое файл VHDX?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## .VHDX вариант №

Файл VHDX представляет собой файл образа диска в формате файла Virtual Hard Disk v2. Он содержит целую операционную систему, которую можно загрузить и использовать как любую обычную машину для тестирования программного обеспечения или запуска программного обеспечения, для которого требуется определенная операционная система. VHDX, несмотря на то, что это полный образ диска, хранится в одном файле. Программное обеспечение виртуальной машины, такое как Parallels Desktop, Windows Virtual Machine и Virtual Box, может загружать и открывать образ диска.

Файл VHDX можно преобразовать в [VHD](/ru/disc-and-media/vhd/) с помощью диспетчера Hyper-V или в [VDI](/ru/disc-and-media/vdi/) с помощью VirtualBox.

## Формат файла VHDX — дополнительная информация

Подробная информация о формате файла VHDX полностью задокументирована и доступна в Интернете как [Спецификации формата файла VHDX] (https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477). ) в документации Microsoft. Это расширение формата VHD, включающее расширенные возможности. Формат файла VHDX предоставляет дополнительные функции, доступные на уровне файлов виртуального жесткого диска и виртуального жесткого диска. Он более оптимизирован и дает лучшие результаты для конфигурации и возможностей оборудования хранения. Файлы VHDX можно открыть

### Поддержка виртуальных жестких дисков в VHDX

Он поддерживает три типа виртуальных жестких дисков.

1. **Фиксированный виртуальный жесткий диск** — виртуальный жесткий диск с выделенным фиксированным объемом данных. Размер виртуального жесткого диска не меняется при добавлении или удалении данных.

1. **Динамический виртуальный жесткий диск** — виртуальный жесткий диск с динамическим размером диска. Его размер в любое время равен фактическим записанным в него данным и метаданным. Размер файла динамически увеличивается по мере добавления или удаления данных.

1. **Дифференциальный виртуальный жесткий диск** — представляет текущий объем виртуального жесткого диска в виде набора измененных блоков по сравнению с родительским файлом виртуального жесткого диска.

## использованная литература

* [Спецификации формата файлов VHDX] (https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - из Википедии](https://en.wikipedia.org/wiki/VHD_(file_format))
