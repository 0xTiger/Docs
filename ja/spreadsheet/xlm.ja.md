{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "ファイル", "拡張子", "ファイル形式", "Microsoft Excel マクロ ファイル", "スプレッドシート" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLM マクロ ファイルとは何か,および XLM ファイルを作成して開くことができる API を知るためのファイル形式ガイド。",
  "title" :"XLMファイルとは?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## .XLM オプション番号

XLM (Excel マクロ) は、マクロの保存に使用されるスプレッドシート ファイルの一種です。アプリケーションの観点から見ると、マクロはプロセスの自動化に使用される一連の命令です。マクロは、[XLS](/spreadsheet/xls/) ファイル形式で繰り返し実行される手順を記録するために使用され、マクロを再度実行することでアクションの実行を容易にします。マクロは、Microsoft の Visual Basic for Applications (VBA) を使用して Excel ワークブック内から Visual Basic Editor を使用してプログラムされ、そこから直接実行/デバッグできます。

## 簡単な歴史 ##

Microsoft Excel は、最初の公開以来、マクロのプログラミングをサポートしていました。マクロの機能は、新しい機能ごとに拡張された Excel の後続のバージョンでも同じままでした。 XLM は、Excel 4.0 までの Excel の既定のマクロ言語でした。 Excel 5.0 はデフォルトでマクロを VBA に記録しましたが、バージョン 5.0 では XLM 記録がオプションとして許可されていました。バージョン 5.0 以降、そのオプションは廃止されました。 Excel 2010 を含むすべてのバージョンの Excel で XLM マクロを実行できますが、Microsoft はその使用を推奨していません。

## XLM でのマクロの記録 ##

Excel には、マクロを記録するための使いやすい手順が用意されています。マクロを操作するには、開発者ツールがインストールされている必要があります。マクロの記録が開始されると、後で実行される各ユーザー アクションが記録されます。マクロの記録には、実際には、記録の開始後にユーザーが実行するすべての手順が含まれます。したがって、マクロの記録が開始された後に、セルのコンテンツを太字、斜体にし、テキストの位置揃えを設定すると、これらすべてのコマンドが記録されます。記録された各マクロには、後ですばやく再生するためのショートカットを割り当てることもできます。マクロの記録では、Visual Basic Editor (VBE) を使用して編集できるマクロの形式で VBA コードが生成されます。

## Excel オブジェクト モデル ##

マクロは、背後で VBA ルーチンを使用し、この目的のために [Excel オブジェクト モデル](https://docs.microsoft.com/en-us/office/vba/api/overview/excel/object-model) に従います。このモデルは、ユーザー定義のコマンド ツールバー、コマンド バー、またはメッセージ ボックスを介してスプレッドシートと対話するためのスプレッドシートのオブジェクトを識別します。たとえば、ワークブックのプロパティへのアクセスは Workbook オブジェクトで許可されます。同様に、ワークブックのワークシートをプログラムで操作するための Worksheet オブジェクトがモデルにあります。

## マクロとセキュリティ ##

VBA は、ファイル システムだけでなく、アプリケーションのすべての領域へのアクセスを許可し、同様に危険な場合があります。これは、自分の側でファイルを実行できるユーザーとワークブックを共有する場合に懸念を引き起こします。つまり、Microsoft Excel はそのようなファイルを開くことについて警告します。マクロは、他のユーザーが信頼できることを確認できるように、デジタル署名で証明できます。したがって、ソースの検証後にマクロを有効にすることができます。

## 参照 ##

* [[MS-XLS] - Excel バイナリ ファイル形式の構造](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [マクロプログラミング](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)
