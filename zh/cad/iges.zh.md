{
  "date" : "2020-03-16",
  "keywords" :["IGES 文件","文件格式","CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 IGES 文件格式和可以创建和打开 IGES 文件的 API。",
  "title" :"IGES 文件格式",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## 什么是一 .IGES 文件？

扩展名为 .iges 的文件用于在计算机辅助设计 (CAD) 应用程序之间交换设计信息。 IGES 代表初始图形交换规范。使用 IGES 交换的信息包括电路图、线框、自由曲面或实体建模表示。 IGES 在传统工程绘图、模型分析和制造功能中都有应用。该格式可以在 CAD 程序之间交换 2D 或 3D 设计信息。 IGES 文件可以用 Autodesk 和 CADSoftTools ABViewer 等多种 CAD 应用程序打开。还有几个 API 可用于以编程方式打开和转换 IGES 文件。

## IGES 文件格式

IGES 文件为 ASCII 文本格式，可以在任何文本编辑器中打开以查看文件内容。 IGES 文件中的文本信息以“Hollerith"格式表示。一个普通的 IGES 文件可以包含数千行来表示可以按照这种格式交换的 2D 或 3D 信息。 IGES 文件分为五个部分，由第 73 列中的特定大写字母表示。这些部分是“开始"(S)、“全局"(G)、“数据输入"(D)、“参数数据"(P) 和“终止"(T) 部分。数据输入和参数数据部分通常分别缩写为 DE 和 PD。

### IGES 文件头

开始和全局部分包含有关以下方面的基本信息：
* 文件名及其来源
* 参数数据部分的分隔符
* 文件作者和其他一般信息。

Wikipedia 上示例文档中的 Start 和 Global 部分如下所示。
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
可以看出，开始字段包含文件的人类可读描述，并且我在第 1-72 列中有任何字符，行以节标题和节行号结尾。 Start 部分必须至少有 1 行。全局部分包含预处理器数据。它还必须存在于文件中并以 G000000# 格式结尾。

### 数据输入 (DE) 和参数数据 (PD) 部分

#### 数据输入部分
一个 IGES 文件由几个实体组成，这些实体包含有关 IGES 文件格式的基本数据的信息。实体包含有关 IGES 数据格式的不同元素的信息并用于绘图。更常用的实体包括：
* 圆弧
* 复合曲线
* 圆锥弧
* 飞机
* 线

这些只是其中的一小部分，在 IGES 中大约有 150 个不同的实体。每个实体都由一个类型编号标识，例如：
* 圆弧（100 型）
* LINE（110 型）

##### 实体属性

每个声明的实体都具有以下属性。

|字段名称|描述|
---|---|
|实体类型 |这是所描述的实体的类型。例如，116 描述了一个 Point 实体。|
|PD 指针 |这给出了该实体数据在参数数据部分中的位置。此位置只是 PD 部分内的行号，它具有此实体数据的第一行。|
|结构 |零或指向定义实体的指针。不适用于大多数实体|
|线条字体样式|数字或指向线条字体图案实体的指针。数字表示：* 0 未指定图案（默认）* 1 实线 * 2 虚线 * 3 虚线 * 4 中心线 * 5 虚线|
|等级|指定要与此实体关联的级别。允许实体出现在多个级别|
|查看|指定查看选项。它们是： 0 表示所有视图中的可见性和特征相同。指向可以从中查看的视图实体（类型 410）的默认指针 参考视图可见关联实体（类型 402，表格 3）
|变换矩阵指针|引用变换矩阵实体（类型 124）或默认为零（无变换）|
|标签显示关联性|引用定义实体标签显示方式的标签显示关联性（类型 402，表格 5）。
|状态编号|包含两个数字的四个部分。 1-2：空白状态。 00 表示正常或 01 表示消隐。 3-4：从属实体切换：00表示独立，01表示物理依赖，02表示逻辑依赖，03表示两者。 5-6：实体使用标志：00 表示几何，01 表示注释，02 表示定义，03 表示其他，04 表示逻辑，05 表示 2D 参数，06 表示构造几何。最后，7-8为层次结构，其中00表示全局自顶向下（使用本实体的特征），01是全局延迟（不使用本实体的特征），02是使用层次属性（使用层次实体（Type 406，Form 10）确定层次分组的特征）。
|序号|由 D# 指定，其中 # 是此部分的行号（不是从文件顶部开始）。这也用于指向此数据输入实体。|
|实体类型|每个实体列表指定两次|
|线宽编号|显示实体时指定厚度。最小为1，默认为0|
|色号|指定实体颜色。允许的整数值为： 0 无颜色（默认） 1 黑色 2 红色 3 绿色 4 蓝色 5 黄色 6 品红色 7 青色 8 白色|
|参数行计数|指定此实体在参数数据部分中占用的行数|
|表格编号|表示该实体的形式或表示。更改参数数据的解释方式。默认为 0|
|保留字段|未使用|
|保留字段|未使用|
|实体标签|应用程序指定标识符 - 右对齐|
|下标号|实体标签的数字限定符。两者共同构成实体的唯一标识符|
|序列号见上文。 |这将是 D#+1，因为每个实体在两行中指定。|

#### 参数数据部分
数据条目部分之后是参数数据部分。它列出了每个相应条目的数据，并根据 Global 部分中指定的分隔符列出实体的参数（通常用逗号分隔参数，用分号结束列表）。


## 参考
* [维基百科的 IGES](https://en.wikipedia.org/wiki/IGES)

