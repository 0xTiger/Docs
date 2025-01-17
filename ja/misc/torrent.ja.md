{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"トレント ファイル形式 - BitTorrent ファイル",
  "description":"TORRENT ファイルと,TORRENT ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## トレントファイルとは何ですか?

TORRENT ファイルは、コンテンツのダウンロードと交換のために BitTorrent やその他の P2P (ピアツーピア) プログラムで使用されるテキスト ファイルです。ダウンロード可能なコンテンツには、ドキュメント、ビデオ、ゲーム、映画、およびインターネット上で利用可能なその他のメディアが含まれる場合があります。これには、ダウンロードするメディアのコンテンツと場所に関するメタデータ情報が含まれます。 BitTorrent のようなソフトウェアは、このファイルからの名前、ファイル サイズ、フォルダ構造などの情報を使用して、データをダウンロードします。トレント ファイルは、オンラインで [PDF](/pdf/) などの他のファイル形式に変換できます。

## トレントとは？データ交換用の TORRENT ファイル形式

トレントとは、BitTorrent ネットワークを使用したデータ ファイルの交換 (ダウンロードとアップロード) の概念です。他のユーザーがアクセスしてダウンロードできるようにデータがアップロードされる従来のサーバーとは異なり、トレント ファイルはトレント ネットワークを使用して取得および送信されます。ユーザーが BitTorrent などのアプリケーションで .torrent ファイルを開くと、ソフトウェアはファイルの内容をビットごとにダウンロードし始めます。複数のユーザーが同じファイルを持っている場合、BitTorrent はダウンロードをすべてのユーザーに分割して、ダウンロードのプロセスを高速化します。同時に、ファイルをダウンロードしているユーザーのコンピューターは、同じファイルをダウンロードしている他のユーザーに送信するためのファイルのソースにもなります。

### TORRENT ファイルの構造

トレント ファイルは、ファイルのリストと、ダウンロードするファイルのすべての部分に関するメタデータ情報の組み合わせです。次の情報がキーの形式で含まれています。

- `announce` — ファイルの可用性について通知するために他のピアにアナウンスされるトラッカーの URL
- `info` — これは、キーが 1 つ以上のファイルが共有されているかどうかに依存するディクショナリにマップします。
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `length` — ファイルのサイズ (バイト単位)。
- `path` — サブディレクトリ名に対応する文字列のリスト。最後は実際のファイル名
- `length` — ファイルのサイズ (バイト単位) (1 つのファイルが共有されている場合のみ)
- `name` — ファイルが保存されるファイル名
- `piece length` — ピースあたりのバイト数。これは通常、28 KiB = 256 KiB = 262,144 B です。
- `pieces` — 各ピースの SHA-1 ハッシュを連結したハッシュ リスト。

## トレントは安全で合法ですか?

P2P ユーザー間でデータを交換するためのトレント プロトコルは、あらゆる種類のファイルを共有するための単なる手段であるため、安全です。したがって、プロトコル自体は危険でも違法でもありません。ただし、ネットワーク経由で共有されるコンテンツには、共有ドキュメントの法的地位に違反する可能性のあるファイルまたはメディアが含まれている場合があります。そのような場合、そのようなデータの交換は、そのようなファイルの公の共有に関与する当事者に対して法的措置を講じる可能性があります。

## 参考文献

* [TORRENT ファイル - ウィキペディア](https://en.wikipedia.org/wiki/Torrent_file)

