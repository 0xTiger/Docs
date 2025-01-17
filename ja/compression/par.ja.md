{
"日付":"2023-07-18",
   "keywords":[
"パー",
"PARファイル",
"par ファイルを開く方法",
"ファイル",
"PAR ファイル拡張子",
"拡大",
"ファイル"
],
   "author":{
"display_name":"シャキール・ファイズ"
},
"draft": "false",
"toc": true,
"title":"PAR ファイル形式 - アーカイブ インデックス ファイル",
   "description":"PAR 形式と,PAR ファイルを作成して開くことができる API について学びます。",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
"parent":"compression"
}
},
"lastmod":"2023-07-18"
}

## .PAR ファイルとは何ですか?

Parchive (PAR) アーカイブ内の .par ファイルは、パリティ ボリュームまたはパリティ ブロックのグループを含むインデックス ファイルを指します。このインデックス ファイルは、アーカイブ内の 1 つ以上のファイルが失われたり破損したりした場合に、エラーの検出と回復の目的で使用されます。

通常、Parchive アーカイブは、元のデータ ファイルと対応するパリティ ボリュームの両方で構成されます。パリティ ボリュームは、リードソロモン誤り訂正アルゴリズムを使用して作成されます。これらのパリティ ボリュームには、元のデータ ファイルを回復するために使用できる冗長情報が含まれています。

.par ファイルはパリティ ボリューム セットとも呼ばれ、アーカイブ内のパリティ ボリュームの構造と場所に関する情報が含まれています。これは、回復プロセスのインデックスまたはマップとして機能します。 .par ファイルを使用することにより、専用の PAR ソフトウェアは、どのパリティ ボリュームが必要か、また、欠落または破損したファイルを再構築するためにどのようにパリティ ボリュームを使用するかを決定できます。

Parchive アーカイブ内の 1 つ以上のファイルがアクセスできなくなったり破損したりした場合、.par ファイルを利用可能なパリティ ボリュームと組み合わせて利用して、失われたデータを回復できます。 PAR ソフトウェアは .par ファイルを読み取り、欠落または破損したファイルを特定し、パリティ ボリュームを使用してそれらのファイルを再構築します。

## PAR ファイルを開くにはどうすればよいですか?

.par ファイルを開いて使用するには、専用の PAR ソフトウェアが必要です。 .par ファイルを処理できる一般的なソフトウェア オプションをいくつか紹介します。

- **QuickPar:** QuickPar は、Windows 用に広く使用されている PAR ソフトウェアです。これにより、PAR ファイルを作成、検証、修復できます。 QuickPar で .par ファイルを開いて整合性を確認したり、Parchive アーカイブ内の破損または欠落したファイルを修復するために使用したりできます。

- **MultiPar:** MultiPar は、Windows で利用できるもう 1 つの人気のある PAR ソフトウェアです。 PAR と PAR2 の両方のファイル形式をサポートし、アーカイブを作成、検証、修復するための高度な機能を提供します。 MultiPar は、.par ファイルを開いて、提供されたパリティ ボリュームに基づいてエラー検出および回復操作を実行できます。

- **MacPAR deLuxe:** MacPAR deLuxe は、macOS 専用に設計された PAR ソフトウェアです。 PAR および PAR2 ファイル形式をサポートし、QuickPar および MultiPar と同様の機能を提供します。 MacPAR deLuxe は .par ファイルを開き、アーカイブの検証と破損または欠落したファイルの回復を支援します。

## PAR ファイル形式 - 詳細情報

一般に Parchive と呼ばれる PAR ファイル形式は、パリティ データを作成し、ファイル アーカイブ内でエラー検出と回復を実行するために使用される特定のファイル形式です。 PAR ファイル形式は通常、PAR、PAR2、PAR3 の 3 つのタイプで構成されます。

- **PAR:** PAR1 としても知られるオリジナルの PAR ファイル形式は、Parchive プロジェクトによって開発されました。これには、元のデータ ファイルから生成されたパリティ データが含まれます。 PAR ファイルは基本レベルのエラー検出と回復を提供しますが、エラー修正機能に関しては制限があります。

- **PAR2:** PAR2 は、PAR ファイル形式の改良版です。より高度なエラー修正機能と強化された回復機能を提供します。 PAR2 ファイルは通常、アーカイブ内の紛失または破損したファイルを回復できるパリティ データを作成するために使用されます。 PAR2 ファイルはデータ破損に対する保護が強化されており、ファイルのアーカイブ目的で広く使用されています。

- **PAR3:** PAR3 は PAR ファイル形式の最新バージョンであり、エラー修正と回復がさらに強化されています。 PAR2 と比較して、さらに高いレベルの冗長性とエラー訂正機能を提供します。 PAR3 ファイルは、アーカイブに保存されているデータに対して、より堅牢な保護と回復のオプションを提供するように設計されています。

PAR2 と PAR3 のファイル形式はどちらも PAR ソフトウェアで広くサポートされており、アーカイブ内のファイルの整合性を検証し、失われたデータや破損したデータを回復する機能を提供します。 PAR および PAR2 ファイルは依然として一般的に使用されていますが、PAR3 ファイルは強化されたエラー修正機能により徐々に採用されてきています。

## 参考文献
* [Parchive](https://en.wikipedia.org/wiki/Parchive)

