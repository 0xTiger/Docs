{
  "date" : "2019-10-11",
  "keywords" :[ "apng ファイル", "apng ファイル形式", "apng ファイルとは", "ファイル", "apng の例", "apng ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APNG ファイル形式 - アニメーション ポータブル ネットワーク グラフィック ファイル",
  "description":"APNG ファイル形式と,APNG ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## APNG ファイルとは何ですか?

拡張子が .apng (Animated Portable Network Graphics) のファイルはラスター グラフィック形式であり、Portable Network Graphic ([PNG](/image/png/) ) の非公式な拡張子です。これは、アニメーション シーケンスを表す複数のフレーム (それぞれの PNG イメージ) で構成されます。これにより、[GIF](/image/gif/) ファイルと同様の視覚化が得られます。 APNG ファイルは、24 ビット イメージと 8 ビット透明度をサポートします。 APNG は、非アニメーション GIF ファイルと下位互換性があります。 APNG ファイルは同じ .png 拡張子を使用し、Mozilla Firefox、APNG をサポートする Chrome、iOS 10 用の iMessage アプリなどのアプリケーションで開くことができます。

## 簡単な歴史

* APNG 仕様は、アニメーション PNG 画像のサポートを提供するために 2004 年に作成されました
* APNG デコーダーは、PNG デコーダーの背面を使用して、はるかに小さいサイズで開発されました。
※継続審議の結果、拡張子を.apngから.pngに変更したまま、新しいMIMEタイプのimage/apngを策定
* APNG は、2007 年 4 月 20 日に PNG グループによって正式に拒否されました。これは、PNG 画像に統一されていると同時に仕様が異なるためです。

## APNG ファイル形式

APNG ファイルは、バイナリ ファイルとしてディスクに保存され、アニメーション イメージに PNG の拡張仕様を使用します。 APNG ファイルの最初のフレームは、表示用に PNG デコーダーで読み取ることができる通常の PNG ストリームです。 APNG ファイル形式は PNG 仕様に従い、データはチャンクと呼ばれるセグメントに格納されます。ただし、APNG は次の新しいチャンクを導入しました。

`Animation Control Chunk (acTL)` - このファイルが通常の PNG ファイルではなく、アニメーション PNG ファイルであることを示します。これはマーカーとして機能し、IDAT チャンクの前に来ます。また、フレーム数とアニメーションをループする時間に関する情報も含まれています。

「フレーム コントロール チャンク」 - 各フレームの開始時に発生し、サイズ、位置、透過性アプリケーション、終了後の前または次のフレームによる置換情報などのメタデータ情報。

`Frame Data Chunk` - フレームの内容を格納し、シーケンス番号で始まります。このシーケンス番号は、デフォルト イメージの IDAT チャンクと同じ構造を持っています。

{{< figure src="../APNG.png" alt="アニメーション PNG - APNG ファイル形式" >}}

ラテラルの仕様は、PNG ファイルを読み取るアプリケーションが理解できないチャンクを単純に無視するように設計されているため、APNG は PNG と下位互換性があります。ビット深度、色の種類、圧縮、フィルター、インターレース方式、パレット情報などの仕様は、デフォルトの PNG 形式と同じです。

## APNG vs GIF

GIF はすでに導入され、長期間にわたって使用されているため、APNG が GIF とどう違うのか疑問に思うかもしれません。以下は、APNG と GIF の一連の比較で、両方のファイル形式の概要を示しています。

||APNG|GIF|
---|---|---|
|発行|2004|1987|
|色深度|24 ビット|8 ビット|
|フレーム レート|無制限|毎秒 10 フレーム|
|透明性|完全および部分的|完全|
|圧縮|非常に良い|良い|

## 参考文献

※【APNGファイル形式】(https://en.wikipedia.org/wiki/APNG)
※【公式PNGフォーマット仕様書】(https://www.w3.org/TR/PNG/)

