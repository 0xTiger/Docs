{
  "date" : "2019-10-11",
  "keywords" :[ "gbr ファイル", "gbr ファイル形式", "gbr ファイルとは", "ファイル", "gbr の例", "gbr ファイル拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GBR ファイル形式 - PCB のガーバー ファイル形式",
  "description":"GBR ファイル形式と,GBR ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .GBR オプション番号

拡張子が .gbr のファイルは、プリント回路基板 (PCB) の設計データ転送を交換するためのガーバー イメージ ファイル形式です。ウカムコが開発した。 PCB 設計データは、製造業界が処理のために必要とする主要なコンポーネントです。 GRB ファイルには、銅層、はんだマスク、凡例、ドリルおよび配線データなどの PCB データが含まれています。標準化された形式で、厚さや仕上げなどの PCB 製造特性などのデータを転送するために使用できます。すべての PCB 設計システムは、PCB 製造システムで処理できる Gerber ファイルを出力します。 GBR ファイルは現在、プリント回路基板 (PCB) 設計データ転送の事実上の標準となっています。 Ucamco は、GBR ファイル形式を開いて表示するための [無料のオンライン ビューアー](https://gerber-viewer.ucamco.com/) を提供しています。

## GBR ファイル形式

GBR は人間が判読できる UTF-8 形式で、わずか 27 個のコマンドで構成されています。コマンドのリストが短くコンパクトであるため、GBR は簡単にデバッグできます。 Gerber のコアは、2D バイナリ イメージのオープンなベクター形式です。メタ情報は、属性を介して画像とともに転送されます。 1 つの GRB ファイルは 1 つのイメージを指定し、付随するファイルや外部パラメーターを解釈する必要はありません。 1 つのイメージに必要なファイルは 1 つだけです。仕様で定義されている印刷可能なすべてのコマンドと名前には、7 ビットの ASCII 文字が使用されます。これは完全な画像生成を完全にカバーしています。

### GBR ファイルの例

以下は、原点を中心とした直径 1.5 mm の円を作成するガーバー ファイルの例です。 1 行に 1 つのコマンドがあります。

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## 参考文献

* [ガーバー形式](https://www.ucamco.com/en/gerber)
