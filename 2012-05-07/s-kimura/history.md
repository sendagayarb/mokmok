# 初めてのiOSアプリケーション.pdf読破

* 最初から読んでおけばよかった感
* プロトコルについて学んだ
* 起動順序を再確認・整理
* Text Field > AttributesでCapitalizationをWordsで、キーボードのデフォルト変更
* Assistant Editorなんてあったのね
* TextFieldとHelloViewControllerをDelegateで接続ってどういう意味？？
* @synthesizeでのアンダースコアの意味

```
コード行で、userNameにアンダースコアをつけることにより、userNameプロパティに 対応するインスタンス変数の名前を_userNameとするよう、コンパイラに指示しています。クラスに _userNameというインスタンス変数を宣言していないので、このコード行はコンパイラに対し、この 変数宣言を合成するよう指示していることにもなります。規約により、インスタンス変数の先頭にアンダースコアをつけておけば、このインスタンス変数に直 接アクセスできないことになります。代わりに、合成したアクセサメソッドを使わなければなりませ ん(例外として、initメソッド内ではインスタンス変数を直接取得、設定できます)。```
## 今日の気づき
* デリゲートがよくわかっていない！！
## 次回以降

* デリゲートの勉強
* Instrumentsの把握
* NavigationBarやTabBar、TableViewの勉強と構築
* iOS アプリケーションプログラミング.pdfで勉強* iOS ツール ワークフロー ガイド_ios_development_workflow.pdfで単体テストの勉強
