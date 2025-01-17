{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKS ファイル形式",
  "keywords" :[ "mks", "matroska video", "mkv format", "file", "format", "video"],
  "description":"Matroska によってのみ作成された字幕の MKS ファイル形式と,MKS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## .MKS オプション番号

MKS ファイルは一般に、字幕のみを含む Matroska ファイルとして知られています。 Matroska は一般的なファイル コンテナーですが、特定の形式の情報を保持することは避けます。一部のオーディオまたはビデオ コンテナで字幕が使用されているため、Matroska はいくつかの一般的な字幕形式の保存に注意を払っています。これは、Matroska が成長率と一致するのに役立ちます。字幕を Matroska に保存するには、以下のポイントに従う必要があります。

- 「.mks」。拡張子は、Matroska ファイル (字幕のみを含む) で使用されます。
- **CodecPrivate** は、ストリーム全体にグローバルなすべてのコーデック関連情報を格納するために使用されています。
- タイムスタンプ ネイティブ ストレージ形式で使用されている開始タイムスタンプと停止タイムスタンプを削除します。代わりに、ブロックのタイムスタンプと期間を使用してください。
- ビデオを含む、透明なレイヤーを持つものなら何でも使用できます。

## 一般的な字幕フォーマット

以下は、Matroska に保存されているより一般的な字幕形式に関する簡単なメモです。

### 画像字幕
VobSub 字幕形式は、Matroska にインポートされる最初の画像字幕形式です。この形式は、DVD から字幕をエクスポートすることによって生成されます。 VobSub が複数のストリームのセットで構成されている場合、Matroska に保存する際にトラックを分離する必要があります。

### SRT 字幕
SRT は、すべての字幕形式の中で最もシンプルで基本的なものです。以下のように 4 つの部分で構成されています。
 



1. サブタイトルの順序を示す番号。
2. 字幕が画面に出たり消えたりする時間。
3. サブタイトルそのもの。
4. 次の字幕の開始を示す空白行。
 



### SSA/ASS字幕
Sub Station Alpha (SSA) は、人気のある字幕エディタ SubStation Alpha で使用されるファイル形式です。 SSA 字幕は、ファンサブバーによって広く使用されています。カラオケ、ポジショニング、スタイリングなど、最新の機能を表示する機能があります。
 



### WebVTT 字幕
World Wide Web Consortium (W3C) は、「Web Video Text Tracks Format」と略される WebVTT を開発しました。この形式は、HTML 要素に関連して外部テキスト トラック リソースをマークアップするために使用されています。

### HDMV プレゼンテーション グラフィック 字幕
HDMV プレゼンテーション グラフィックス サブタイトル フォーマット (HDMV PGS) は一連のビットマップであり、テキストとは言えません。言い換えれば、グラフィック イメージのタイミング シーケンスにすぎないと言えます。情報を抽出するには、PGS を SRT に変換する必要があります。

### HDMV テキスト字幕
HDMV テキストは、Blu-ray で使用されるテキスト字幕形式として知られています。 Matroska は、TextST 字幕を保存するときに UTF-8 文字セットのみを許可します。

### デジタル ビデオ放送 (DVB) 字幕
DVB サブタイトル形式は、TV 信号の複数言語の字幕の送信と表示を規制するために導入されました。典型的な字幕フォーマットでは、伝送システムのメーカーに関係なく、視聴者は誰でも DVB 字幕付き伝送を見ることができます。


## 参照 ##

- [マトロスカ字幕](https://www.matroska.org/technical/subtitles.html)

