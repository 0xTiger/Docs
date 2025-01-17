{
  "date" : "2021-09-01", 

  "keywords" :[ "RS", "ファイル", "拡張子", "ファイル形式", "Rustプログラミング言語", "プログラミングガイド", "RSサンプル", "Rust", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RS - Rust プログラミング ファイル",
  "description":"RS ファイル形式と,RS ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "RS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-01"
}

## .RS ファイル拡張子

RS 拡張子を持つファイルは、Rust プログラミング言語に属します。これは、ソフトウェアと安全性、特に安全性のために設計された、多言語で高レベルの一般的なプログラミング言語です。 Rust は構文的には С++ に似ていますが、参照を検証するために借用チェッカーを使用することでメモリの安全性を保証できます。 Rust 言語は、ガベージ コレクションを使用せずにメモリの安全性を確保し、リファレンスの参照は完全です。

## RS ファイル形式 ##

Rust は、Dave Herman、Brendán Eich などの協力を得て、Mоzillа Research の Grаydоn Hоаre によって最初に設計されました。業界での使用が増加しており、Miсrоft は安全で安全性の高いソフトウェア標準の言語を実験しています。

Rust は、2016 年以来毎年、スタックオーバーフロー開発者調査で「最も愛されているプログラミング言語」に選ばれていますが、2021 年の調査では回答者の 7% しか使用していませんでした。バージョン 0.4 より前では、Rust もサポートされていました。

tyresate システムは、プログラム ステートメントの前後に、特別なチェック ステートメントを使用することによって、モデル化されたアサーションを持っています。不一致は、実行時ではなく、適切な時間に発見される可能性があります。これは、C または C++ コードでのアサーションの可能性があります。標準状態は言語 NIL で最初に導入されたため、Rust に固有のものではありませんでした。 Rust の移動セマンティクスを活用することで同じ機能を達成することができますが、ほとんど使用されていないため、タイプステートは削除されました。

Rust プログラミング言語は、より速く、より信頼性の高いソフトウェアを作成するのに役立ちます。高レベルのエルゴノミクスと低レベルのコントロールは、言語設計のプログラミングにおいてしばしば劣っています。さびはそれを妨げます。 Rust は、優れた技術的能力と優れた開発者経験のバランスを取ることで、手間のかかる伝統的な方法を一切使わずに、低レベルの詳細 (メモリの使用など) を制御するためのオプションを提供します。

 

## 簡単な歴史 ##

この言語は、2006 年にモジラ エンプロイ グレイドン ホーアによって開始された個人的なプロジェクトから成長しました。 Mоzillа は 2009 年にリリースを開始し、2010 年に発表しました。最初の安定版リリースである Rust 1.0 は、2015 年 5 月 15 日にリリースされました。その後、6 週間続くベータ リリースでテストされます。 2021 年 6 月 6 日、Google は、С/С++ の代替として、Аndrоid Oрen Sоurсe Рrоjeсt 内で Rust のサポートを発表しました。

## 技術仕様 ##

Rust は、高度に最新で高度に安全なシステムのための言語であり、大規模なプログラミング、つまり、大規模なシステムの整合性を確保する境界を作成および維持するための言語であることを意図しています。これにより、安全性、メモリ レイアウトの制御、セキュリティを重視した機能セットが生まれました。


Rust 言語は、メモリセーフになるように設計されています。ヌルインター、ダングリングインター、またはデータレースを許可しません。データ値は、固定された一連のフォームを介してのみ初期化できます。これらのフォームはすべて、入力が既に初期化されている必要があります。リンクされたリストやバイナリ ツリー データ構造のように、有効または NULL のいずれかであるインターンを再現するために、Rust ライブラリは特定のタイプを提供します。 Rust には、ライフタイムを管理するための構文が追加されています。安全でないコードは、安全でないキーワードを使用して、これらの制限の一部を覆すことができます。


Rust 言語は、自動ガベージ コレクションを使用しません。メモリおよびその他のリソースは、リソースを使用して管理され、リソースの参照が開始されます。


Rust は、非常に低いオーバーヘッドでリソースの決定論的な管理を提供します。 Rust はすべての値を優先し、暗黙のボックス化を行いません。参照の参照 (シンボルを使用) がありますが、これは実行時の参照参照には関係しません。そのようなインターンターの安全性は、適切な時間に検証され、未定義の動作のダングリングインターンやその他の形式を防ぎます。


Rust には、すべての値が一意の所有者を持つ所有者システムがあります。値は、&T を使用した不変参照、可変参照、& mut T、または値による T を使用して解釈できます。Rust コンパイラは、適切な時間にこれらの規則を適用し、すべての参照が有効であることを確認します。


## RS ファイル形式の例 ##

```
use serde::{Serialize, Deserialize};

#[derive(Serialize, Deserialize, Debug)]
struct Point {
    x: i32,
    y: i32,
}

fn main() {
    let point = Point { x: 1, y: 2 };

    let serialized = serde_json::to_string(&point).unwrap();
    println!("serialized = {}", serialized);

    let deserialized: Point = serde_json::from_str(&serialized).unwrap();
    println!("deserialized = {:?}", deserialized);
}
```

## 参照 ＃＃

* [RS - ウィキペディアによる](https://en.wikipedia.org/wiki/Rust_(programming_language))



