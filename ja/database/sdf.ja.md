{
  "date" : "2021-05-03",
  "keywords" :[ "SDF","sdf ファイル","sdf ファイルとは","sdf ファイルの開き方","拡張子","ファイル","sdf ファイル形式","データベース ファイルの種類","データベース ファイル形式" , "データベースファイル" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"SDF ファイル形式と,SDF ファイルを作成して開くことができる API について学びます。",
  "title" :"SDF - SQL Server Compact データベース ファイル",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## .SDF ファイルとは?
拡張子が .sdf のファイルには、コンパクト リレーショナル データベースとも呼ばれる Microsoft SQL Server Compact (SQL CE) データベースが含まれています。モバイル デバイスおよびデスクトップ用に作成されたアプリケーション用に Microsoft によって作成されました。 32 ビットと 64 ビットの両方のオペレーティング システムをサポートし、データベースの完全なコンテンツが 1 つの SDF ファイルに含まれ、4GB 以上のディスク容量を占有する可能性があります。セキュリティ上の目的で、.sdf ファイルを 128 ビット暗号化で暗号化できます。 SQL CE ランタイムは、.sdf ファイルへの並列マルチユーザー アクセスを解決します。 SDF ファイルは、**QuickOnce** を介してコピーするか、単にシステム展開の宛先にコピーすることができます。

## SDF ファイル形式
SDF ファイルには、通常コンパクト リレーショナル データベースと呼ばれるデータベースが含まれています。 SDF ファイルにはすべてのデータベース関連情報が含まれており、SQL Server Compact は軽量で無料のデータベース エンジンであり、.sdf ファイルの管理に使用されます。 .sdf ファイルのサイズは、4 GB のサイズの制限を超えてはなりません。 SDF ファイルには、ストアド プロシージャ、トリガー、またはビューに関する情報は保存されません。 SQL CE データベースを使用するアプリケーションは、ADO.NET 接続文字列で SDF ファイルへのパスを指定する必要はありません。代わりに、アプリケーションのアセンブリ マニフェストで定義されているデータ ディレクトリを定義する |DataDirectory|\database_name.sdf として指定できます。
.sdf 命名規則はオプションであり、任意の拡張子を使用してファイルを保存できます。データベース ファイルのパスワードの設定は、オプションの手順です。データベースを圧縮または修復するには、**圧縮/修復済みデータベース**のオプションを使用してファイルを保存する必要があります。

## 参考文献

* [SQL Server Compact - ウィキペディア](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [ASP.NET Web アプリケーションに SQL Server Compact を使用する](https://learn.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


