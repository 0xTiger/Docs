---
date: 2019-12-09
keywords: arj,.arj,arj ファイル形式,arj ファイルの開き方,.arj 拡張子,arj 拡張子
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARJ ファイル形式
linktitle: ARJ
description: "ARJ ファイル形式と,ARJ ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## .ARJ オプション番号##

ARJ (Archived by Robert Jung) は、Robert K. Jung によって開発された高効率の圧縮アーカイブ ファイルです。 ARJ は、1990 年代初頭に DOS および Windows の初期バージョン用に開発されました。 ARJ ファイルは、すべてのファイルを追跡する必要がなく、処理するファイルが 1 つしかないため、多数のファイルをバックアップまたは共有する場合に便利です。 .arj 拡張子は、ARJ アーカイブ ファイルに使用されます。

## ARJ ファイル形式 ##

ARJ ファイルには、次の 2 種類のヘッダーが含まれています。

- メイン ヘッダー: アーカイブの先頭に 1 つのメイン ヘッダーがあります。
- ローカル ヘッダー: ローカル ヘッダーは各ファイルの前に存在します。

|オフセット|タイプ|カウント|説明|
|---|---|---|---|
|0000h|単語|1|ID=0EA60h|
|0002h|ワード|1|基本ヘッダーサイズ|
|0004h|バイト|1|ヘッダーのサイズ|
|0005h|byte|1|アーカイバのバージョン番号|
|0006h|byte|1|最低限必要なバージョン番号|
|0007h|バイト|1|ホストOS:</br> 0 - MS-DOS</br> 1 - プリモス</br>2 - UNIX</br> 3 - アミーガ</br>4 - MAC-OS (システム xx)</br> 5 - OS/2</br> 6 - アップルGS</br> 7 - アタリST</br> 8 - 次へ</br>9 - VAX VMS|
|0008h|byte|1|内部フラグ、ビットマップ:</br> 0 - パスワードなし / パスワード</br>1 - 予約済み</br>2 - ファイルは次のディスクに続きます</br>3 - ファイル開始位置フィールドが利用可能</br>4 - パスの変換 (「\」から「/」へ)|
|0009h|byte|1|圧縮方式:</br> 0 - 保存</br>1 - 最も圧縮</br>2 - 圧縮</br>3 - 高速圧縮</br>4 - 最速で圧縮|
|000Ah|バイト|1|ファイルの種類:</br> 0 - バイナリ</br>1 - 7 ビット テキスト</br>2 - コメント ヘッダー</br>3 - ディレクトリ</br>4 - ボリューム ラベル|
|000Bh|バイト|1|予約済み|
|000Ch|dword|1|MS-DOS 形式のオリジナル ファイルの日付/時刻|
|0010h|dword|1|圧縮ファイルのサイズ|
|0014h|dword|1|元のファイルのサイズ"|
|0018h|dword|1|元ファイルのCRC-32|
|001Ah|word|1|ファイル名のファイルスペック位置|
|001Ch|単語|1|ファイル属性|
|001Eh|word|1|ホストデータ|
|?|dword|1|拡張ファイルの開始位置|
|????h|dword|1|基本ヘッダーのCRC-32|
|????h|word|1|最初の拡張ヘッダーのサイズ|
|????h+"SIZ"+2|dword|1|拡張ヘッダーのCRC-32|
|????h+"SIZ"+6|byte|?|圧縮ファイル|

## 参照 ##

- [ARJ - ウィキペディア](https://en.wikipedia.org/wiki/ARJ)
