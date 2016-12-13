# 中級課題 不完全なFizzBuzz
以下のような仕様を満たすプログラムがあります。
* 起動すると入力待ち状態になる
* 入力待ち状態から1を入力して、その次に整数を入力すると任意の文字列を表示する
  * 整数が3の倍数である場合はFizzと表示する
  * 整数が5の倍数である場合はBuzzと表示する
  * 整数が15の倍数である場合はFizzBuzzと表示する
  * 上記以外の整数の場合はその整数を表示する
* 入力待ち状態から2を入力すると、1を入力したときの機能の入力と出力の履歴を表示する
* 入力待ち状態から3を入力すると、入力と出力の履歴をファイルに保存する
* 入力待ち状態から4を入力すると、3で保存したファイルを読み込み、過去の履歴を表示する
* 入力待ち状態から0を入力すると、プログラムを終了する
* 入力待ち状態から0が入力されるまでは、プログラムを終了しない


このプログラムを題材に、以下の課題1、課題2、課題3のうちからいずれか1つのみ選択し解答してください。課題は複数解答しないでください。ただし、題材のプログラムは複数の言語で作られていますが、6つある言語の中からいずれか1つのみを選択して解答してください。


# 課題1 ソースコードのリファクタリング
本プログラムは仕様を満たす動作をしますが、ソースコードの品質が高いとは言えません。そこで、本プログラムの既存の挙動を壊すことなく、ソースコードを現状よりも高品質な状態に変更してください。必要に応じてディレクトリ構成の変更、ファイルのリネーム等も行ってください。  
プルリクエストには課題1を選択したことと、なぜその変更を行ったかをできるだけ詳しく記述してください。


# 課題2 足りないテストコードの追加
本プログラムは自動テストを利用したTDDで実装しています。しかし、不完全な形でTDDを実践したために、テストケースに抜け漏れがあります。そこで、本プログラムに足りないテストケースを追加してください。  
プルリクエストには課題2を選択したことと、なぜそのテストケースを追加したのかをできるだけ詳しく記述してください。


# 課題3 自由な機能追加/仕様変更
本プログラムは仕様を満たす動作を行っていますが、魅力的な品質を備えたプログラムとは言えません。そこで、このプログラムに対して「必要だ」と思う機能を自由に追加する、あるいは「問題がある」と思った機能の仕様を変更してください。 ただし、機能の追加に伴い、既存のテストコードが失敗する状態になった場合は、テストが成功する状態に修正してください。  
プルリプクエストには課題3を選択したことと、どんな機能を追加/変更したのかとなぜその機能を追加/変更したのかをできるだけ詳しく記述してください。


# 開発で利用した言語及びツールのバージョン
以下の言語及びツールのバージョンで実装を行っています。
* ruby 2.3.1、Bundler 1.13.1
* java 1.8.0_102、Gradle 3.2.1
* perl 5.20.2、carton 1.0.22
* php 7.0.9、Composer 1.2.2
* python 2.7.12
* go 1.7.3


# プログラムの起動方法
各言語の名前をつけているディレクトリ直下で以下のコマンドを実行してください。

## ruby
`$ ruby -Ilib lib/main.rb`

## java
`$ gradle run`

## perl
`$ carton exec perl -Ilib lib/Main.pl`

## php
`$ php lib/Main.php`

## python
`$ python src/main.py`

## go
※ GOPATHにカレントディレクトリを設定する必要があります
`$ go run src/main.go`


# 自動テストの利用方法
本プログラミング課題には自動テストを利用したTDDで実装しています。既存の振る舞いを壊していないことを保証するためにご利用ください。

## ruby
`$ bundle exec rspec`

## java
`$ gradle test`

## perl
`$ carton exec prove -Ilib t`

## php
`$ vendor/bin/phpunit test`

## python
`$ python run_test.py`

## go
※ GOPATHにカレントディレクトリとその直下のtestディレクトリを設定する必要があります  
`$ go test ./test/src/...`