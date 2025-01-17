{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "拡張子", "ファイル", "ファイル形式", "データベースファイルの種類", "データベースファイル形式", "データベースファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"LDF ファイル形式と,LDF ファイルを作成して開くことができる API について学びます。",
  "title" :"LDF - SQL Server マスター データベース ファイル形式",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .LDF オプション番号

拡張子が .ldf のファイルは、リレーショナル データベース管理システム (RDBMS) である Microsoft SQL Server によって維持されるログ ファイルです。プライマリ データベース ファイル ([MDF](/database/mdf/)) で実行されたすべてのトランザクション (挿入、更新、削除など) は、LDF ファイルに記録されます。 LDF ファイルは、あらゆるデータベースの重要なコンポーネントです。システム障害が発生した場合、ログ ファイルを使用してデータベースを一貫した状態に復元します。トランザクションが完全にコミットされていない場合、トランザクション ログ ファイルのサイズが大きくなる可能性があります。 LDF ファイルは、Microsoft SQL Server ソフトウェア アプリケーションで開くことができます。

## LDF ファイルに記録される操作

SQL ログ ファイルには、次の操作が記録されます。

* 各取引の開始と終了。

* 各データ データの変更 (挿入、更新、または削除)。これには、システム ストアド プロシージャまたはデータ定義言語 (DDL) ステートメントによる、システム テーブルを含む任意のテーブルへの変更も含まれます。

* すべてのエクステントおよびページの割り当てまたは割り当て解除。

* テーブルまたはインデックスの作成または削除。

## LDF ファイル形式

LDF ファイルは、ログ レコードの文字列として配置された SQL Server トランザクション レコードで構成されます。各ログ レコードには、前のレコードの LSN よりも大きいログ シーケンス番号 (LSN) があります。文字列は、ファイル内で互いに連結されます。最新の高速コンピュータにより、ログ ファイルの LSN1 の前に LSN2 が存在する場所にレコードを挿入できます。操作は連続して記録されるため、LSN2 で記述された変更は、ログ レコード LSN1 の後に実行されました。特定のトランザクションのレコードは、使用されるポインターを使用して逆方向にリンクされ、トランザクションのロールバックを高速化します。
 

## 参考文献

* [データベース ファイルとファイル グループ](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [トランザクション ログのアーキテクチャと管理ガイド](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server-ver15)

