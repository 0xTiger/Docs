{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "シェル スクリプト - Ubuntu および Linux で実行する方法",
  "description":"シェル スクリプトとは何か、およびそれを Ubuntu および Linux で実行する方法について学びます。",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-ja",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## シェルスクリプトとは何ですか?

シェル スクリプトには、**シェル スクリプト**と呼ばれるプレーン テキスト ファイルに一連のコマンドを記述することが含まれます。これらのスクリプトは、コマンドライン インタープリタであるシェルによって実行されます。最も一般的なシェルには次のものがあります。

1. バッシュ (ボーン・アゲイン SHell)
2. Zsh (Z シェル)
3. 魚。

シェル スクリプトは、単純なワンライナーから複雑なプログラムまで多岐にわたり、ファイル操作、システム管理、反復タスクの自動化など、さまざまなタスクを実行するために使用されます。

## シェルスクリプトの利点:

1.  **自動化:** シェル スクリプトを使用すると、ユーザーは反復的なタスクを自動化し、時間を節約し、人的エラーの可能性を減らすことができます。
    
2.  **カスタマイズ:** ユーザーは、特定のニーズに合わせたスクリプトを作成して、高度なカスタマイズを行うことができます。
    
3.  **バッチ処理:** シェル スクリプトは、複数のコマンドを順番に実行する必要があるバッチ処理タスクの処理に優れています。
    
4.  **システム管理:** シェル スクリプトは、バックアップ、ログのローテーション、ソフトウェアのインストールなどのシステム管理タスクによく使用されます。

## 単純なシェル スクリプトを作成します。

挨拶メッセージを出力する基本的なシェル スクリプトを作成してみましょう。テキスト エディタを開き、「greeting.sh」という名前のファイルを作成します。次の行を追加します。

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

ファイルを保存し、ターミナルで次のコマンドを実行して実行可能にします。

```
chmod +x greeting.sh
```

これで、スクリプトを実行できるようになります。

```
./greeting.sh
```

出力は次のようになります。

```
Hello, welcome to the world of shell scripting!
```

## Ubuntu および Linux でのシェル スクリプトの実行:

ここでは、**Ubuntu および Linux で .sh ファイルを実行する方法**について説明します。

1.  **スクリプトを実行可能にする:** シェル スクリプトを実行する前に、それが実行可能であることを確認してください。前に示したように `chmod` コマンドを使用します。
    
2.  **スクリプト ディレクトリに移動します:** ターミナルを開き、「cd」コマンドを使用してシェル スクリプトが含まれるディレクトリに移動します。
    
3.  **スクリプトを実行します:** ターミナルで「./scriptname.sh」と入力し、「scriptname」を実際のスクリプト名に置き換えてスクリプトを実行します。
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Bash コマンドの使用:** スクリプトが `#!/bin/bash` (**shebang** として知られる) で始まる場合は、`bash` コマンドを使用して実行することもできます。

```
bash greeting.sh
```

## シェルスクリプトの $@ は何を意味しますか?

シェル スクリプトでは、`$@` はスクリプトに渡されるすべてのコマンドライン引数を表します。引数のリストを別個のエンティティとして参照するためによく使用されます。 `$@` のように二重引用符内で使用すると、スペースや特殊文字を考慮して個々の引数が保持されます。

簡単な説明は次のとおりです。

- `$@`: スクリプトまたは関数に渡されるすべての位置パラメータ (引数) を表します。各引数は別個の単語として扱われます。
    
- `$@`: 二重引用符で囲むと、引数の分離が維持され、個々の引数内にスペースまたは特殊文字を含めることができます。
    

以下に簡単な例を示します。

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

たとえば、引数を指定してこのスクリプトを実行すると、次のようになります。

```
bash example.sh arg1 "argument 2" arg3
```

次のように出力されます。

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

ご覧のとおり、`$@` はすべての引数を表し、`$@` はスペースが含まれている場合でも個々の引数を保持します。

