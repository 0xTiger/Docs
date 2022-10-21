{
  "date" : "2021-03-08",
  "keywords" :["RB","Nuvo Media 的 Rocket 电子书设备","文件","扩展名","格式","电子书"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 Nuvo Media 的 Rocket 电子书设备的 RB 文件格式以及可以创建和打开 RB 文件的 API。",
  "title" :"RB - 火箭电子书文件",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## 什么是一 .rb 文件？

扩展名为 .rb 的文件包含 Rocket 电子书的内容。 Rocket 电子书实际上是 Nuvo Media 制造的设备；他们在 1998 年发布了这款设备。虽然 Rocket 电子书能够显示图像，但只能以黑白显示。它在 4.5 x 3 英寸的触摸屏上具有 106 dpi 或 480 x 320 像素的屏幕。 Rocket 电子书通过串口连接到计算机，以下载 RB 文件格式的电子书。 RB 文件能够使用 DRM，但现代电子书并未使用该技术。 RB 文件通常包含一个带有图像的 HTML 文件和一个带有所有元数据 (.info) 的伪 OPF 文件。

## RB 文件格式的技术规范##

一个幻数（十六进制）出现在文件的前 4 个字节中：B0 0C B0 0C。

接下来的两个字节似乎是一个版本号，如“02 00"，代表主要版本 2 和次要版本 0。

接下来的四个字节包含文本“NUVO"，然后是 4 个字节的 00h。

下一个 4 字节是这本书的创建日期，编码为 int16。这使我们处于偏移量 0Eh。 ORocketLibrary 的旧版本编码了年份的完整值（即，1999 是“CF 07"，2000 是“D0 07"）。在最近的版本中，tm_year 是逐字存储的，即 100 表示 2000 年（“64 00"）。一年之后是一个表示相对于 1 的月份编号的 int8 和一个表示月份中的某天的 int8。

接下来的 6 个字节是 00h。对于时间设置，这些可以保留。

“目录"的绝对偏移量包含在偏移量 18h 处的 int32 中。

之后是一个包含 .rb 文件长度的 int32。这用于确定文件是否完整。

这整个字节块（20h 到 128h）似乎只有经过加密的标题才需要。在未加密的标题中，它们始终为零。

在大多数情况下，目录如下（偏移 128 处）。它以 ToC 中“页面"条目（.rb 文件部分）的数量的 int32 计数开始。每个条目包含一个名称（零填充到 32 个字节），后跟 3 个 int32：数据段的长度、.rb 文件中的位置和该条目的标志。截至今天，已知值为：1（加密）、2（信息页）和 8（放气）。这些名称都是根据需要量身定制的，以确保它们都是唯一的。

## 参考

* [电子阅读器 - 通过 MobileRead](https://en.wikipedia.org/wiki/E-reader)
