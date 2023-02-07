{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"OSZ ファイル形式と,OSZ ファイルを作成して開くことができる API について学びます。",
  "title" :"OSZ ファイル - osu! ビートマップ ファイル形式",
  "linktitle" : "OSZ",
  "menu" : {
    "docs" : {
      "identifier":"game-osz",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## .OSZ オプション番号

OSZ ファイルは、リズムゲーム osu! で使用される圧縮ファイル形式です。ビートマップデータを保存します。ビートマップは基本的にゲームのレベルであり、曲、ビートのタイミング、ゲーム画面上のヒット オブジェクトの配置などの情報が含まれます。 OSZ ファイルを使用すると、ビートマップを簡単に配布できます。通常は、インターネットからダウンロードしてゲームにインポートします。おす！ [OSR](/ja/game/osr/) ファイル形式もあり、これはゲーム リプレイ ファイルであり、ゲーム プレーヤーがリプレイできます。

**OSR ファイル形式の MIME タイプ:** x-osu-replay

## OSZ ファイル形式

OSZ ファイル タイプの内部ファイル形式の詳細は公開されていません。 [ZIP](/ja/compression/zip/) で圧縮されたデータが含まれており、音楽を再生したり、グラフィックを表示したり、プレイヤーがゲームを操作する必要がある場合のイベントに関する情報をプレイヤーに表示したりします。

## OSZ ファイルの作成方法

おす！ [OSZ の作成](https://osu.ppy.sh/wiki/en/Client/File_formats#creating-.osz-and-.osk-files)の詳細な手順があります。
) および OSK ファイル。次の手順を使用して、OSU! を使用して OSZ ファイルを作成できます。

1. エディターでビートマップを開きます。
1. トップ メニューから、[ファイル] > [パッケージのエクスポート...] を選択します。
1. .osz アーカイブは、osu 内の Exports フォルダーに配置されます。フォルダ。

## 参考文献

※【押忍！リズムゲーム】(https://osu.ppy.sh/home)
* [OSZ ファイル形式](https://osu.ppy.sh/wiki/en/Client/File_formats/Osz_%28file_format%29https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format %29#データ型)
