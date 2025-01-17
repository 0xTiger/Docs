{
  "date" : "2020-08-20",
  "keywords" :[ "woff ファイル", "woff ファイル形式", "woff ファイルとは", "ファイル", "woff の例", "woff ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Web Open File Format",
  "description":"WOFFファイルは,Web Open Font Formatで作成されたオープンフォント形式です。",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## .WOFF オプション番号

拡張子が .woff のファイルは、Web Open Font Format (WOFF) に基づく Web フォント ファイルです。 TrueType (.TTF) または OpenType (.OTT) フォント タイプに基づく、形式固有の圧縮コンテナーがあります。 WOFF は、Web フォントをデスクトップ アプリケーションで使用されるフォント ファイルと区別することを目的として導入されました。さらに、この形式は、ネットワークを介してサーバーからクライアントのコンピューターにフォントを転送する際の待ち時間を短縮することを目的としています。 WOFF ファイルを TTF やその他のフォント ファイル形式に変換できるツールがいくつかあります。

## **WOFF ファイル形式**

WOFF フォント形式は、TrueType、OpenType、Open Font Format などのさまざまなフォント タイプで使用されるテーブル ベースの sfnt 構造体のフォント データ テーブルを圧縮します。これは、これらのフォント タイプのコンテナーのようなものであり、コンテナーに含まれるフォントのメタデータと私用データを含める余地もあります。コンバーターは sfnt ファイルを使用して WOFF 形式のファイルにし、ユーザー エージェントはエンコードされたファイルを Web ドキュメントで使用するために復元します。復元されたフォント データは、すべての面で入力フォント形式と正確に一致することに注意してください。

WOFF ファイル ユーティリティには、グリフのサブセット化、検証、フォント機能の追加などの追加機能が含まれていることがよくありますが、必須ではありません。作成者と使用エージェントの両方が、基礎となるフォント データの有効性が保持されていることを確認する必要があります。

### WOFF ファイルの構造

WOFF ファイルの構造は、sfnt フォントの構造に似ています。これは、各フォント データ テーブルへの長さとオフセットを含むテーブル ディレクトリに基づいています。すべての表は、この初期情報の後に続きます。このファイルには、元のフォントと同じフォント データベースが含まれています。テーブルの順序も同じですが、それぞれが圧縮されている場合があります。ただし、元のテーブル ディレクトリは WOFF テーブル ディレクトリに置き換えられます。

WOFF ファイルは次のもので構成されます。

* WOFFHeader - 基本的なフォント タイプとバージョンを含むファイル ヘッダーと、メタデータおよびプライベート データ ブロックへのオフセット。
* TableDirectory - 元のサイズ、圧縮サイズ、および WOFF ファイル内の各テーブルの場所を示すフォント テーブルのディレクトリ。
* FontTables - 必要な帯域幅を削減するために圧縮された、入力 sfnt フォントからのフォント データ テーブル。
* ExtendedMetadata - 拡張メタデータのオプション ブロック。XML 形式で表され、WOFF ファイルに保存するために圧縮されます。
* PrivateData - フォント デザイナー、ファウンドリ、またはベンダーが使用するプライベート データのオプション ブロック。

### WOFFヘッダー
WOFF ヘッダーは、ファイルに含まれるデータの種類を示す識別署名で構成されます。 WOFF ヘッダーとそのフィールドは次のとおりです。

|タイプ|フィールド名|説明|
---|---|---|
|UInt32|署名 |0x774F4646 'wOFF' |
|UInt32| |flavor |入力フォントの「sfnt バージョン」。|
|UInt32|長さ |WOFF ファイルの合計サイズ。|
|UInt16| numTables |フォント テーブルのディレクトリ内のエントリ数。|
|UInt16|予約済み |予約済み;ゼロに設定。|
|UInt32| totalSfntSize |圧縮されていないフォント データに必要な合計サイズ。sfnt ヘッダー、ディレクトリ、およびフォント テーブル (パディングを含む) を含みます。|
|UInt16| majorVersion |WOFF ファイルのメジャー バージョン。|
|UInt16| minorVersion |WOFF ファイルのマイナー バージョン。|
|UInt32| metaOffset |WOFF ファイルの先頭からメタデータ ブロックまでのオフセット。|
|UInt32| metaLength |圧縮されたメタデータ ブロックの長さ。|
|UInt32| metaOrigLength |メタデータ ブロックの非圧縮サイズ。|
|UInt32| privOffset |WOFF ファイルの先頭からプライベート データ ブロックまでのオフセット。|
|UInt32| privLength |プライベート データ ブロックの長さ。|


## **参考文献**
* [w3 WOFF ファイル形式](https://www.w3.org/TR/WOFF/)

