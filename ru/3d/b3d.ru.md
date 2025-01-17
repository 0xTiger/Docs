{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файлов B3D; используется в играх blitz3d и API, которые могут открывать и создавать файлы B3D.",
  "title" :"B3D — файл модели объекта Blitz3D",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## .B3D вариант №

Файл с расширением .b3d — это файл модели, используемый Blitz3D, который может содержать модели видеоигр для персонажей, зданий, местности и других объектов. Blitz3D — это язык программирования, используемый для создания **blitz3d-игр**. Blitz3D — это мощный, гибкий и простой в использовании язык программирования, разработанный исключительно для написания видеоигр. Разработчики могут создавать насыщенные действием 3D-игры, 2D-головоломки, приключения, ролевые игры и многое другое, просто используя Blitz3D.

Blitz3D основан на языке программирования BASIC; который также прост в освоении и использовании. Все эти факты делают Blitz идеальным как для начинающих, так и для более опытных программистов. Хотя его функции считаются несколько устаревшими по сравнению с большинством современных 3D-движков, Blitz3D продолжает использоваться многими программистами игр по всему миру.

## Краткая история Blitz3D

Blitz3D был в основном выпущен для операционной системы Microsoft Windows в сентябре 2001 года, чтобы конкурировать с другими подобными языками разработки игр. Blitz3D был обновленной версией более раннего 2D-движка BlitzBasic, который расширил свой набор команд за счет добавления API для 3D-движка на основе DirectX 7. Пользователи Blitz3D также должны сравнить BlitzMax, который является более поздним движком от BlitzBasic. BlitzMax — это сложная, но более мощная версия Blitz3D, которая поддерживает объектно-ориентированные языки программирования. Это обновленный графический API, который лучше подходит для символов Unicode, OpenGL и экспорта в OSX и Linux, а не только в Windows.

## Пример B3D
Файл b3d, содержащий 1 чанк TEXS, 1 чанк BRUS и 1 чанк NODE, будет выглядеть следующим образом:

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
Простая, неанимируемая и нетекстурированная сетка будет выглядеть так:

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## использованная литература
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

