{
  "date" : "2019-10-11",
  "keywords" :[ "shp ファイル", "shp ファイル形式", "shp ファイルとは", "ファイル", "shp の例", "shp ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - ESRI シェープファイル",
  "description":"SHP ファイル形式と,SHP ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## .SHP オプション番号

SHP は、ESRI Shapefile の表現に使用される主要なファイル タイプの 1 つのファイル拡張子です。これは、地理情報システム (GIS) アプリケーションで使用されるベクター データの形式で地理空間情報を表します。この形式は、ESRI と他のソフトウェア製品との間の相互運用性を促進するために、オープン仕様として開発されました。

## データ表現

前述のように、シェープファイル形式は、データ セットの地理空間情報をベクトル フィーチャとして記述します。これらのベクトル機能には次のものがあります。

*ポイント
* 行
* ポリゴン

これらのフィーチャを組み合わせることで、井戸、国境、空間ポイント、河川の流れ、湖など、ほぼすべてのタイプの形状を表すことができます。各ベクター フィーチャには、そのフィーチャの目的を実際に定義する属性を含めることができます。たとえば、ロサンゼルスの都市を含むシェープファイルには、空間データに意味のある表現を与える属性として都市名と気温を含めることができます。

## 関連ファイル

スタンドアロンの shp ファイルをソフトウェア アプリケーションで使用して、そこに含まれるデータを解釈することはできません。このようなファイルに含まれる情報を理解するために、シェープファイルは次の追加の必須ファイルを利用します。

* shx ファイル - インデックス ファイル
* dbf ファイル - 形状のすべての属性をメイン ファイルに格納する dBASE ファイル
* prj ファイル - ファイルのプロジェクト情報を保存します

メインファイルと同じ名前を共有する他のオプションファイルも存在する可能性があります。

## SHP ファイル形式の仕様

シェープファイルのオープン仕様は、[技術説明](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) の形式で ESRI からオンラインで入手でき、ファイルの全体的な構造が詳細に説明されています。メイン .shp ファイルの情報は、ヘッダーとレコードで構成されます。固定長ファイル ヘッダーの後に可変長レコードが続きます。すべてのレコードは、固定長レコード ヘッダーとそれに続く可変長レコード コンテンツで構成されます。

### メインの SHP ファイル ヘッダー

メインのファイル ヘッダーはファイルの先頭から始まり、長さは 100 バイトです。このメイン ファイル ヘッダーの構成と、バイト位置、値、型、およびバイト順を次の表に示します。


|バイト|フィールド|値|タイプ|バイト順
---|---|---|---|---|
|0-3|ファイル コード|9994|整数|ビッグ エンディアン
|4-23|未使用|0|整数|ビッグ エンディアン
|24-27|ファイルの長さ|ファイルの長さ|整数|ビッグ エンディアン
|28-31|バージョン|1000|整数|リトルエンディアン
|32-35|形状タイプ|形状タイプ|整数|リトルエンディアン
|36-67|最小外接長方形|Xmin、Ymin、Xmax、および Ymax|double|リトル エンディアン
|68-83|バウンディング ボックス|Zmin、Zmax|double|リトル エンディアン
|84-99|バウンディングボックス|Mmin, Mmax|double|

ファイル長の値は、ヘッダーを構成する 50 個の 16 ビット ワードも含む 16 ビット ワードで表したファイルの全長であることに注意してください。

#### 形状の種類

上記の表の形状タイプ フィールドの値は次のとおりです。


|値|形状タイプ
---|---|
|0|ヌル シェイプ
|1|ポイント
|3|ポリライン
|5|多角形
|8|マルチポイント
|11|PointZ
|13|PolyLineZ
|15|ポリゴンZ
|18|マルチポイントZ
|21|点M
|23|PolyLineM
|25|ポリゴンM
|28|マルチポイントM
|31|マルチパッチ

### データレコード ###

メイン ファイル ヘッダーの後に可変長レコードが続きます。各レコードは、固定長レコード ヘッダーとそれに続く可変長レコード コンテンツで構成されます。

#### レコード ヘッダー ####

レコード ヘッダーには、レコードのレコード番号とコンテンツの長さに関する情報が 8 バイトの固定長で含まれます。レコード ヘッダーの構成は次のとおりです。


|バイト|フィールド|値|タイプ|バイト順
---|---|---|---|---|
|0-3|レコード番号|レコード番号|整数|大
|4-7|レコード長|レコード長|整数|大

#### 記録内容 ####

シェープファイル レコードの内容は、形状タイプとそれに続くその形状のジオメトリ データで構成されます。形状タイプ 0 は、形状のジオメトリ データを持たない null 形状を表します。レコード内容の長さは形状パーツと頂点を反映したものです。 Point Shape タイプの例を取り上げて、そのような形状タイプに関する情報がレコードにどのように含まれているかを詳しく説明しましょう。

ポイントは、X、Y の順序で特定の地理的位置を表し、各座標は倍精度値で表されます。次の表は、ポイント形状タイプの配置を示しています。


|バイト|形状タイプ|値|タイプ|数値|バイト順
---|---|---|---|---|---|
|0-3|形状の種類|1|整数|1|小さい
|4-11|X|X|ダブル|1|リトル
|12-19|Y|Y|ダブル|1|リトル

他の形状タイプの例は、ESRI 技術説明ドキュメントに記載されています。

## 参照 ##

* [ESRI Shapefile Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) by ESRI

