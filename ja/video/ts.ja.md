{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TS ファイル形式 - ビデオ トランスポート ストリーム ファイル",
  "keywords" :[ "ts", "flie", "extension", "extension", ".ts", "format" ],
  "description":"TS ファイルとは何か,および TS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## .TS ファイルとは何ですか?

拡張子が .ts のファイルは、データを DVD に保存するビデオ ストリームです。 MPEG-2 ([.mpeg](/video/mpg/)) 圧縮アルゴリズムを使用して、インターネット ストリーミングや放送などのさまざまなメディア タイプ間で最大の効率と互換性を実現します。 TS ファイル形式は、スマート TV などのインターネット接続が不十分なデバイスで再生できるように作成されました。

## TS ファイル形式 - 詳細情報

TS ファイルのデータは [MP4](/video/mp4/) ファイルに似ていますが、小さなチャンクに分割されています。各チャンクは、ビデオの小さな断片で構成され、その後にオーディオのビットとオプションのキャプションが続きます。 1 つの TS ファイルは、このような多くのチャンクで構成されています。ビデオ、オーディオ、キャプションに加えて、各チャンクには、チャンク内のエラーを検出するための追加データも含まれています。このため、TS ファイルのサイズはやや大きくなります。

### TS ファイル形式を使用する理由

では、TS ファイルのサイズが多少大きい場合、他のファイル形式の代わりにそれらを使用する利点は何ですか?ブロードキャストでは、ビデオとオーディオの小さなチャンクを通信メディア (有線または無線) を介してリアルタイムで送信できます。チャンク内の余分なデータは、エラーが発生しやすいチャンクをスキップするために受信者によって使用されます。

さらに、放送システムではストリーム全体を再生する必要がないため、TS ファイルが使用されます。伝送を拾うことができ、オーディオとビデオを組み立てることでリアルタイムで使用できます。

## TS ファイルの再生方法

TS ファイルは、無料でダウンロードできる人気の [VideoLAN VLC メディア プレーヤー](https://www.videolan.org/vlc/features.html) で開いて再生できます。

## 参照 ##

* [MPEG トランスポート ストリーム - ウィキペディア](https://en.wikipedia.org/wiki/MPEG_transport_stream)

