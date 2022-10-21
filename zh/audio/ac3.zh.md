{
  "date" : "2019-12-13",
  "keywords" :["AC3","文件","扩展名","格式","音频编码","MPEG"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 AC3 文件格式和可以创建和打开 AC3 文件的 API。",
  "title" :"AC3 - 音频编解码器 3 文件",
  "linktitle" : "AC3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## 什么是一 .ac3 文件？

扩展名为 .ac3 的文件是由杜比实验室推出的 Audio Codec 3 文件。它是一种音频格式，最多可包含六个音频输出通道。该格式最初用于音频，但现在也用于其他应用，例如 HDTV 广播、DVD、蓝光光盘和游戏机。可以打开 AC3 文件的应用程序包括 Apple QuickTime player、Microsoft Windows Media Player、Winamp、MPlayer 等。

## AC3 文件格式

AC3 文件本质上是二进制文件，并且基于修正离散余弦变换 (MDCT)，这是一种有损压缩算法。杜比实验室使用 MDCT 算法和感知编码原理来开发 AC-3 音频格式。这导致 AC-3 格式在 1991 年作为杜比数字标准发布。该格式支持为正常范围扬声器提供五个通道（20 Hz - 20,000 Hz）和一个通道（20 Hz - 120 Hz）用于低音炮驱动低频效果。 AC3 支持高达 48 kHz 的采样率。

＃＃＃ 技术细节

杜比数字技术使用一种非常有效的方式来压缩多声道音频文件的大小，而不会影响音质。这种压缩导致更小的文件大小，这使得分发声音文件变得容易。使用杜比数字，可以在电影或 DVD 上包含完整的 5.1 声道音频混合。

＃＃＃＃ 规格
杜比数字规格如下。

|领域|规格|
---|---|
|通道 |1.0 到 5.1，离散|
|DVD 数据速率，5.1 声道音频| 384 或 448 kbps|
|蓝光光盘数据速率，5.1 声道音频|640 kbps|
|支持杜比元数据|是|
|连接 |S/PDIF、HDMI®、IEEE 1394|
|混合/流媒体功能|是|

#### 元数据参数

|元数据参数|信息|控制|
---|---|---|
|对话层次| |是|
|频道模式| |是|
|LFE 声道| |是|
|比特流模式|是|是|
|线模压缩| |是|
|射频模式压缩| |是|
|射频过调制保护| |是|
|中心缩混电平| |是|
|环绕下混电平| |是|
|杜比环绕模式| |是|
|音频制作信息|是||
|混合水平|是||
|房型|是||
|版权位|是||
|原始码流|是||
|首选立体声缩混| |是|
|Lt/Rt 中心缩混电平||是|
|Lt/Rt 环绕下混电平||是|
|Lo/Ro 中心缩混电平||是|
|Lo/Ro 环绕下混电平||是|
|杜比数字环绕 EX™ 模式||是|
|A/D转换器类型|有||
|直流滤波器||是|
|低通滤波器||是|
|LFE 低通滤波器||是|
|环绕声 3 dB 衰减||是|
|环绕声相移||是|

## 参考

* [AC3 - 维基百科提供](https://en.wikipedia.org/wiki/Dolby_Digital)
* [杜比数字 5.1](https://professional.dolby.com/tv/dolby-digital)
