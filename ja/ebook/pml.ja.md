{
  "date" : "2021-03-08",
  "keywords" :[ "PML", "eReader", "extension", "format", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"PML ファイル形式,Palm マークアップ言語,および PML ファイルを作成して開くことができる API について学びます。",
  "title" :"PML - Palm マークアップ言語ファイル",
  "linktitle" : "PML",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## .PML オプション番号

Palm Inc は、Palm Markup Language File を表す PML ファイル形式を導入しました。その目的は、タブレット コンピューターに似た電子書籍読み取りデバイスである eReader 用のドキュメントを作成することです。 PML ファイルは、[PDB](/programming/pdb/) ファイル (さまざまなデータ ファイルを含む) にレイアウトを与えて、Palm デバイスに表示します。

## PML ファイルの技術的詳細

PML ファイルの構造は、段落、見出し、インデント、参照など、eBook セットアップを作成するためのタグで構成されています。また、太字、小文字、上付き文字などの書式タグも使用できます。開発者は、電子ブックに画像を追加することもできます。

### Palm マークアップ言語
次の表に、PML コマンドを示します。

|コマンド|説明|
---|---|
| | \p |新しいページ |
| | \x |新しい章;また、新しい改ページが発生します。章のタイトル (および任意のスタイル コード) を \x および \x | で囲みます。
| | \Xn |新しいチャプター、チャプター ダイアログで n レベル (n は 0 から 4 まで) インデントされています。改ページは発生しません。章のタイトル (およびスタイル コード) を \Xn および \Xn | で囲みます。
| | \Cn="章のタイトル" |チャプター リストに「チャプター タイトル」をレベル n (\Xn など) で挿入します。テキストはページに表示されず、改ページは強制されません。これは、章の導入部の冒頭に章記号を挿入する場合などに便利な場合があります。 | |
| | \c |このテキスト ブロックを中央揃えにします。行頭を \c で閉じる |
| | \r |テキスト ブロックを右揃えにします。行頭の \r で閉じる |
| | \i |ブロックをイタリック体にします。 \i | で閉じます。
| | \u |下線ブロック; \u | で閉じます。
| | \o |オーバーストライクブロック; \o | で閉じます。
| | \v |目に見えないテキスト; \v で閉じます (コメントに使用できます) |
| | \t |インデント ブロック。行頭から開始し、行末で \t で終了 |
| | \T="50%" |画面幅の指定された割合 (この場合は 50%) をインデントします。現在の描画位置が指定された画面位置をすでに超えている場合、このタグは無視されます。 | |
| | \w="50%" |画面の特定のパーセンテージ幅 (この場合は 50%) の水平線を埋め込みます。このタグは前後で改行します。ルールは中央です。パーセント記号は必須です。 | |
| | \n | | ユーザーによって指定された「通常の」フォントに切り替えます。
| | \s | stdFont に切り替えます。 \s で閉じると通常のフォントに戻ります |
| | \b | boldFont に切り替えます。 \b で閉じると、通常のフォントに戻ります (推奨されません。代わりに \B を使用してください) |
| | \l | largeFont に切り替えます。 \l で閉じると通常のフォントに戻ります |
| | \B |テキストを太字にします。 \b タグとは異なり、\B はフォントを変更しないため、大きな太字のテキストを使用できます。 \b と \B を同じ PML ファイルに混在させることはできません。 | |
| | \Sp |テキストを上付き文字としてマークします。太字、斜体などの他のスタイルと混在させないでください。上付き文字のテキストは \Sp で囲みます。 | |
| | \Sb |テキストを下付きとしてマークします。太字、斜体などの他のスタイルと混在させないでください。下付きテキストは \Sb で囲みます。 | |
| | \k |囲まれたテキストを小文字にします。 \k で閉じます。 \k タグで囲まれたすべての文字 (アクセント付きの文字を含む) は大文字になり、通常の大文字よりも小さいポイント サイズでレンダリングされます。 | |
| | \\ |単一のバックスラッシュを表します |
| | \aXXX | Windows-1252 コードが 10 進数の XXX である非 ASCII 文字を挿入します。詳細については、PML 文字テーブルを参照してください。 | |
| | \UXXXX | Unicode コードが 16 進数の XXXX である非 ASCII 文字を挿入します。詳細については、拡張 PML 文字テーブルを参照してください。 | |
| | \m="画像名.png" |名前付き画像を挿入します。以下の画像のセクションを参照してください。 | |
| | \q="#linkanchor"テキスト\q |ドキュメント内の別の場所にあるリンク アンカーを参照します。ドキュメントを表示すると、アンカー指定の後、末尾の \q の前の文字列に下線が引かれるか、リンクとして表示されます。 | |
| | \Q="リンクアンカー" |ドキュメントにリンク アンカーを指定します。 | |
| | \- |ソフトハイフンを挿入します。ソフト ハイフンは、単語を改行する必要がある場合にのみ表示されます。 | |
| | \Fn="footnote1"1\Fn | "1" を、PML ドキュメントの最後にタグ付けされた footnote1 という名前の脚注にリンクします。以下の脚注とサイドバーのセクションを参照してください。 | |
| | \Sd="sidebar1"サイドバー\Sd | 「Sidebar」テキストを、PML ドキュメントの最後にタグ付けされた sidebar1 という名前のサイドバーにリンクします。以下の脚注とサイドバーのセクションを参照してください。 | |
| | \私 |参考索引項目としてマークします。 \I と \I で索引項目 (およびすべてのスタイル コード) を囲みます。
 


## 参考文献

* [Palm マークアップ言語 - MobileRead による](https://wiki.mobileread.com/wiki/EReader)
* [電子リーダー - MobileRead による](https://en.wikipedia.org/wiki/E-reader)

