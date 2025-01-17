{
  "date" : "2019-10-11",
  "keywords" :["emf 文件","emf 文件格式","什么是 emf 文件","文件","emf 示例","emf 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF - 增强的元文件格式",
  "description":"了解 EMF 文件格式和可以创建和打开 EMF 文件的 API。",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .emf 文件？

**增强的元文件格式 (EMF)** 独立于设备存储图形图像。 EMF 的元文件由按时间顺序排列的可变长度记录组成，可以在任何输出设备上解析后呈现存储的图像。这些可变长度记录可以是封闭对象的定义、绘图命令和对准确渲染图像至关重要的图形属性。当设备使用自己的图形环境打开 EMF 图元文件时，无论打开设备平台如何，原始图像的比例、尺寸、颜色和其他图形属性都保持不变。

## 历史简介 ＃＃

1990 年，Microsoft 为 Microsoft Windows 设计了一种图像文件格式 Windows Metafile ([WMF](/zh/image/wmf/))。 Windows 图元文件是 16 位格式，可能包含一些位图组件。WMF 可能由矢量图形组成，旨在保持不同应用程序之间的可移植性。 1993 年，Win32/GDI 发布了增强型元文件 (EMF)，这是一个具有增强的灵活性和可扩展性的新版本。 EMF 还用作图形语言命令来运行打印机驱动程序。 Microsoft 现在推荐使用增强的图元文件格式 (EMF) 而不是 Windows 格式 (WMF)。引入 Windows XP 时，发布了增强型元文件格式 Plus (EMF+) 版本。这个较新的版本通过序列化 GDI+ API 调用找到自己的方式，同样 WMF/EMF 记录对 GDI 的调用。存在一个 gzip 压缩版本的 EMF，称为 EMZ。

## EMF 元文件格式##

以下是增强的元文件格式的基本元素：

* 一个 EMR_HEADER（版本、大小、创建时图片的分辨率）
* GDI 对象表
* 保留调色板（可选）
* 以数组结构排列的元文件记录（属性设置、定义对象、绘图命令）
* EMR_EOF 记录（EMF 元文件中的最后一条记录）

## EMF 版本 ##
* **原始**：原始版本指定了保留原始图像并保持其设备独立性所需的记录。此外，还支持包含图形对象和绘图命令的记录。
* **版本 1**：EMF 的第二个版本通过添加像素格式记录和使用 OpenGL 命令的规定提高了灵活性和设备独立性。
* **第 2 版**：第三版通过添加公制系统来测量设备表面距离来提高准确性，使记录更具可扩展性。

## 增强的元文件记录##

元文件记录以数组的形式排列。这些记录具有 ENHMETARECORD 结构并且长度可变。 ENHMETARECORD 指定定义 GDI 函数以使用增强的图元文件格式创建图片的数据。 **ENHMETAHEADER** 结构始终是这种格式的第一条记录。此 EMF 标头包含以下信息。

增强元文件的每条记录在开始时都有两个 EMR 成员（提供基本结构）。第一个成员识别 GDI 函数（参数用于记录），该函数确定记录的类型，称为 iType。另一个成员 nSize 定义每条记录的大小。其余参数（如果有）和其他数据紧挨着 nSize 排列。紧随标题之后可能会出现可选的文本描述。图片和作者的名称记录在该文本描述中。其存在是一个选项的调色板指定在增强的图元文件创建中使用的颜色。用于指定图片创建中必不可少的 GDI 功能的其他记录。

每个元文件中至少应存在一个 EMF 记录。从一个记录到另一个记录的遍历信息依赖于 EMF 记录，因此这些记录必须相邻排列。在除 EOF_record 之外的元文件中的任何给定记录处，该特定记录的长度定义为移动到下一条记录。

## 增强的元文件创建##

**CreateEnhMetaFile** 函数用于创建增强的元文件。此函数参数用于在磁盘/内存上对图片进行尺寸和存储。此外，此功能需要首先出现图片的设备（参考设备）的尺寸和参考设备的上下文（DC）。因此，在调用 **CreateEnhMetaFile** 函数时必须提供处理此 DC 的参数。函数的语法如下：
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** 参考设备的句柄。

**lptoFilename:** 指向文件名的指针。

**lprc:** 指向椭圆结构的指针以毫米为单位指定图片尺寸。

**lpDesc:** 指向图片标题和创建图片的应用程序名称的字符串的指针。

## 增强的元文件操作##

以下是可以使用增强元文件句柄完成的作业。

*显示和编辑存储的图片。
* 生成增强的元文件副本。
* 检索增强型元文件的 EMF 标头、可选描述和二进制版本的副本
* 重述调色板中的颜色。

## 图形对象##

在绘图和绘画操作中，可以通过对象创建记录创建图形对象，并可以保存以备后用。 `EMR_SELECTOBJECT` 记录可以使用播放设备上下文检索这些图形对象。钢笔、调色板、画笔、色彩空间、字体和常用对象是一些可重用的对象类型。

## 字节排序##

Little-endian 格式用于将数据存储在元文件记录中。

## 版本控制##

EMF 文件格式已修改两次。更改的版本是原始版本、扩展 1 和扩展 2。扩展版本提供了 OpenGL 记录和内部像素格式的可选描述符。为显示的尺寸添加了以毫升为单位的测量设备。

## 参考 ＃＃

* [增强格式元文件 | Microsoft Docs](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [增强的元文件格式和规范](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

