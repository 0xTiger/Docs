{
  "date" : "2020-07-28",
  "keywords" :["HPGL","ファイル形式","開く","読み取る","作成する","CAD"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"HPGL ファイル形式と,HPGL ファイルを作成して開くことができる API について学びます。",
  "title" :"HPGL ファイル形式 - ファイル形式の専門家から学ぶ!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## .HPGL オプション番号

HPGFL(Hewlett-Packard Graphics Language) ファイルには、HP が開発したプロッター制御用の命令セットが含まれています。 HP プロッターは、このファイルを使用して、ベクターおよびラスター コンテンツを用紙に描画および印刷します。

### HPGL コマンド

HPGL コマンドは以下で構成されます。
※アルファベット2文字のコマンド部
* パラメータセクション
※ターミネーター部

複数のパラメータがある場合は、ファイル内の各パラメータをセパレータで区切る必要があります。

### HPGL コマンドの例

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### 座標系

座標系は、特定の場所を特定するための 2 次元測定インジケータで構成されています。 HPGL は、この目的のためにプロッター座標系とユーザー座標系の両方を使用します。

#### プロッタ座標系

この座標系は、プロッタの動きに基づいて図面をプロットするために使用されます。プロッタの最小移動の一般的な XY 単位は 0.025 mm です。プロッタの種類により、作図可能範囲が異なります。

#### ユーザー座標系

スケールと原点を使用して、ユーザー指定の座標系を設定できます。これらは、IP コマンドと SC コマンドを使用してプロッタ座標に変換されます。この変換が実行されない場合、プロッタ システム座標がデフォルトで使用されます。

## HPGL ファイル形式
HPGL ファイルは ASCII (テキスト ファイル) 形式で、いくつかのセットアップ コマンドで開始します。これにより、プロット用のプロッタの特定のパラメータが設定されます。典型的な HPGL ファイルは次のようになります。

|コマンド|意味
---|---|
|IN;|初期化、プロット ジョブを開始|
|IP;|スケーリング ポイント (P1 と P2) をデフォルトの位置に設定|
|SP1;|ペン 1 を選択|
|PU0,0;|ペンを持ち上げて、次のアクションの開始点に移動|
|PD100,0,100,100,0,100,0,0;|ペンを下に置き、次の場所に移動します (ページの周りにボックスを描きます)|
|PU50,50;|ペンを上げて X、Y 座標 50,50 に移動|
|CI25;|半径 25 の円を描く|
|SS;|標準文字セットを選択|
|DT*,1;|テキスト区切り文字をアスタリスクに設定し、それらを出力しません (1、「真」を意味します)|
|PU20,80;|ペンを持ち上げて 20,80| に移動します。
|LBHello World*;|ラベルを描く|

## 参考文献
* [ウィキペディアによる HPGL](https://en.wikipedia.org/wiki/HP-GL)
※【HPGLリファレンスガイド】(https://www.isoplotec.co.jp/HPGL/eHPGL.htm)
