{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :["SWF","ファイル","拡張子","形式","動画形式","SWFファイルとは","swfファイル形式","swfファイルプレーヤー","swfファイルの開き方"] ,
  "title" :"SWF ファイル - Shockwave Flash ムービー ファイル形式",
  "description":"SWF ファイルとは何か,および SWF ファイルを作成して開く方法を示す API について学びます。",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## SWF ファイルとは何ですか?

SWF ファイルは、Adobe Flash で作成されたアニメーション ファイルです。アニメーションを作成するために、テキスト、ベクター画像、ラスター画像、アクションスクリプト、円、線、正方形、長方形などのオブジェクトなど、さまざまなタイプの要素を含めることができます。 SWF ファイルは、これらのマルチメディア アイテムを、さまざまなフレーム/秒 (fps) で再生できるフレームに配置します。 SWF は Short Web File を意味しますが、Shockwave 形式を持つことも知られています。

*SWF ファイルを開く**ことができるアプリケーションには、Adobe Flash Player (現在は廃止されています) と Eltima Elmedia Player が含まれていました。

## SWF ファイル形式 - 詳細情報

SWF ファイルは、バイナリ ファイルとしてディスクに保存されていました。 SWF ファイル形式は、Web サイトに埋め込んだり、単独で再生したりできるアニメーションやゲームの開発に使用されました。また、インタラクティブなマルチメディア アプリケーションを作成するための多くの選択肢を開発者に与えるビデオとサウンドもサポートしていました。 SWF ファイルは、Adobe Shockwave がインストールされている Web ブラウザーで再生できます。 Adobe Flash は、不具合とセキュリティ上の問題により、2020 年 12 月に廃止されました。

## SWF ファイル形式の歴史

SWF ファイル形式は、もともと FutureWave Software によって設計されたもので、ファイル サイズを小さく保ちながら、ネットワーク接続が低速なシステム上のプレーヤー ソフトウェアで実行することを意図してアニメーションを表示します。 1996 年 12 月、Macromedia は FutureWave を所有し、Macromedia Flash 1.0 に切り替えました。

2005 年、Adobe は Macromedia を買収しました。Adobe は、2008 年にオープン ソース プロジェクトの一部として SWF を発表しました。同年、Adobe は、世界で人気のある Web エンジンに SWF ファイルのクロールとインデックス作成を可能にするコードをリリースしました。ただし、SWF ファイルが Flash コンテンツをインターネット上で公開するための標準形式になりつつあるため、SWF は Small Web Format を意味するように改訂されました。

## SWF ファイルの構造

パスは SWF の基本的なグラフィカル要素であり、単純な線からベジエ曲線に至る基本要素の一連のセグメントです。これらの単純な要素は、立方体、楕円、さらにはテキストなど、他の追加のプリミティブを作成するのにも役立ちます。 SWF のグラフィック プリミティブは、SVG や MPEG-4 BIFS などの他の形式のグラフィック要素と類似しています。

リストの表示と、すでに定義されている要素の再利用/名前の変更も、この形式で許可されています。 SWF のバイナリ ストリーム形式は、タグ、サイズ、およびペイロードの点で類似している QuickTime アトムと比較できます。バイナリ ストリーム形式により、古いプレーヤーはサポートされていないコンテンツをスキップできます。 SWF の元のバージョンはベクター グラフィックスと画像の提供に限定されていましたが、新しいバージョンではオーディオとビデオのコンテンツも許可されます。

「Stage3D」という名前の Flash Player の新しい低レベル 3D API がバージョン 11 で導入されました。この API は、OpenGL または Direct3D に対応するものとして想定されていました。 Stage3D は、Adobe Graphics Assembly Language (AGAL) と呼ばれる低レベル言語で色を定義します。以下は、SWF ファイル形式のいくつかの基本的なデータ型です。

### 座標

SWF ファイル形式の XY 座標は整数として格納され、twip と呼ばれる単位で測定されます。 twip は、論理ピクセルの 1/20 で構成されます。ファイルを 100% にスケーリングせずに再生すると、論理ピクセルと画面ピクセルは同じになります。

### 整数型とバイト順

SWF ファイル形式では、8、16、32、および 64 ビットの符号付きおよび符号なしの整数型を使用できます。整数値の格納にはリトルエンディアンのバイト順が使用されます。バイト内ですが、ビットオーダーはビッグエンディアンで格納されます。すべての整数値はバイト単位で整列する必要があります。符号付き整数は、従来の 2 の補数のビット パターンを使用して表されます。

### 固定小数点数

SWF ファイル形式では、32 ビットと 16 ビットの 2 種類の固定小数点数がサポートされています。

### 浮動小数点数

SWF 8 以降のバージョンでは、浮動小数点型の IEEE 標準 754 と互換性のある 3 種類の浮動小数点数 (FLOAT、FLOAT 16、DOUBLE) を使用します。

### エンコードされた整数

エンコードされた整数の 1 つのタイプは、可変バイト数で SWF 9 以降でサポートされています。

## 参考文献

* [SWF ファイル形式](https://en.wikipedia.org/wiki/Swf)

