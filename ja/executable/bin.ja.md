{
"日付":"2023-07-20",
   "keywords":[
"置き場",
"BIN ファイル",
"ファイル",
"BIN ファイル拡張子",
"拡大",
"ファイル"
],
   "author":{
"display_name":"シャキール・ファイズ"
},
"draft": "false",
"toc": true,
"title":"BIN ファイル形式 - Unix 実行可能ファイル",
   "description":"BIN 形式と,BIN ファイルを作成して開くことができる API について学びます。",
"linktitle": "BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
"parent":"executable"
}
},
"lastmod":"2023-07-20"
}

## .BIN ファイルとは何ですか?

BIN ファイルは、Linux や FreeBSD などの Unix ベースのオペレーティング システム上の実行可能ファイルです。ソース コードから派生したバイナリ コードで構成されるコンパイル済みプログラムを保持し、基盤となるシステム アーキテクチャとの互換性を確保します。 Unix 実行可能 BIN ファイルは、実行可能形式としての役割の点で、Windows .EXE ファイルおよび macOS .APP ファイルと比較できます。

Unix システムのソフトウェア開発の分野では、開発者がプログラムをパッケージ化して配布するために BIN ファイルが一般的に使用されます。これらはユーザーにソフトウェアを配信する便利な手段を提供し、簡単なインストールと実行を可能にします。 BIN ファイルの他に、[.ELF](/ja/executable/elf/)、.X86、[.RUN](/ja/executable/run/)、.X86_64 などの他の種類の Unix 実行可能ファイルが存在し、それぞれが特定のハードウェアまたはハードウェアに合わせて調整されています。システム要求。

BIN ファイルの内部構造は、Unix オペレーティング システムが同封されているプログラムを識別、読み取り、実行するために利用するエンコードされたデータで構成されています。システムは、特定のファイル署名またはヘッダーに基づいて BIN ファイルを実行可能ファイルとして認識し、その後、その中に含まれるバイナリ命令を解釈して実行します。

BIN ファイルには、**INSTALL.TXT** ファイルがバンドルされていることがよくあります。このファイルには、プログラムを適切にインストールしてセットアップする方法についての詳細な手順が記載されています。このドキュメントにより、ユーザーはインストール プロセスをスムーズに進め、複雑な作業なくソフトウェアの利用を開始できるようになります。

## BINファイルを開くには?

BIN ファイルは、直接開いて表示するように設計されていません。ただし、プログラムを実行したり、プログラムに含まれるデータを抽出したりすることはできます。 BIN ファイルの内容にアクセスするには、BIN ファイルの名前が「sample.bin」であると仮定して、コマンド ラインで次の手順に従います。

1. **実行可能権限を確認します:**

BIN ファイルを実行する前に、実行可能ファイルとして実行するために必要な権限があることを確認してください。次のコマンドを使用します。

```
$ chmod +x sample.bin
```

このコマンドは、ファイルに実行権限を付与します。

2. **BIN ファイルを実行します。**

実行可能権限を設定した後、次のコマンドを入力して BIN ファイルを実行できます。

```
$ ./sample.bin
```

**警告**

_ダウンロードまたは電子メールで送信された BIN ファイルを扱う場合は、サイバー犯罪者がマルウェアを配布するために使用する可能性があるため、注意してください。悪意のある実行可能ファイルによる攻撃のリスクを軽減するために、信頼できるソースからの BIN ファイルのみを実行してください。

## その他の BIN ファイル

**.bin** ファイル拡張子を使用する他のファイル タイプは次のとおりです。

- [BIN - MacBinary エンコード ファイル](/ja/compression/bin/)
- [BIN - バイナリ ディスク イメージ ファイル](/ja/disc-and-media/bin/)
- [BIN - BlackBerry IT ポリシー ファイル](/ja/settings/bin/)
- [BIN - セガジェネシスゲームROM](/ja/game/bin/)
- [BIN - PSX PlayStation BIOS イメージ](/ja/game/bin-pcsx/)

## 参考文献

* [Linux でバイナリ ファイルを実行する方法](https://linuxhint.com/execute-binary-files-in-linux/)

