Sendagaya.rb #13

# 説明と自己紹介

* Sendagaya.rb の紹介としていままでの活動を振り返り
* お互い初めての人もいるので、各自自己紹介

# RailsにおけるRESTfulなURL設計勉強会の復習

資料を読み合わせつつ、前回の資料を踏まえての議論。

* [RESTful Web アプリの設計レビューの話](http://www.slideshare.net/t_wada/restful-web-design-review)
* [一周目のリソース設計](https://speakerdeck.com/u/moro/p/rails-resource-routing-design-bootstrap-ja)
* [リソースモデリングパターンの提案](http://www.slideshare.net/tkawa1/resource-modeling-pattern)

## [RESTful Web アプリの設計レビューの話](http://www.slideshare.net/t_wada/restful-web-design-review)

各スライドを見ながらみんなから出た意見など。

* slide 4
	* WEB+DB pressの連載はWEBを支える技術が包括しているから無理してさがないでいいよ。
	* DHHの発表は元スライドが見つからず、元資料も[web arcive](http://bit.ly/NDmRO7)しかなさそう。もし元スライドなどの情報があれば欲しいです。
	* RESTful Web Serviceの邦訳ひどいから原書がいいかも
* slide 5
	* [動画で配信！「現場で使えるREST」鼎談](http://gihyo.jp/dev/serial/01/rest)
* slide 8
	* RESTful Webサービスでも何度も出てくるお話。
	* URL設計 = 名前付けと考えがちだがそれは、ステップ3でようやく現れる。
	* 与えたい情報の設計から考える。
* slide 11
	* editはギリギリ名詞の意味もある。
	* newは形容詞。形容詞はURLにつかうのぎりok後ろに名詞が省略していると考える。
	* confirmationをactionとして捉えるか、resourceとしてとらえるか。大切なのは思想を統一すること
	* [kozo22](https://twitter.com/kozo002)さんがまさに今作っていて迷っているというお話。今度、おれの考えるconfirmation設計はこれだ！みたいなのをみんなでだしあってはどうかというお話。
* slide 12
	* cool URL 誰しも通る道、かもしれない
	* / で区切ったら階層を意識せよ。
* slide 13
	* 英単語探すのにシソーラス使うよねー
	* DBレコードにとらわれ過ぎないの大事。これはCRUDの重力と繋がるお話
* slide 14
	* リソースの意味としてリソースに複数の言語があるのであればURLに/jaが含まれてもよいのでは？
	* クライアントが複数の選択肢から選ぶなら?の右
	* URLってentriesを検索しているようにも見えるから、記事の言語がlang=jaで絞っているようにも見えるよね。確かに！そういう意味にもとれる。
* slide 15
	* CRUDの重力とは、URLをデータベースと1:1で紐付け過ぎな状態のこと。
	* N+1問題 = リソース分けすぎて、1ページで複数のリソースをajaxで取るようなこと。
	* N+1問題とは、posts#index で各postのlikes, commentsを別リソースとしてajaxで取るような感じ。
	* バランス感覚大事だね
	* resource - controller - model みたいにcontrollerは仲介役
* slide 18
	* ステータスコードを1つずつ確認。
	* よくPOSTした後、redirect_toすると302でリダイレクトするけど、あの用途はじつは307だ。ブラウザの対応があまりされてないので302使ってる。
* slide 19
	*　見せたくないプライベートリソースは存在すらバレるべきでないので404ってのは結構みんなみたい
* slide 20
	* 袋小路になっていない = 普通にHTMLでコーディングしてリンクでページをつなぐイメージ
* slide 21
	* 方針の話。プロジェクトで方針を統一するのが良さそう。
* slide 22
	* HTMLではリンクでページをつなぐ
	* XMLだとAtomとかに仕様がある
	* JSONには明確な仕様がないが接続性がある方が望ましい
* slide 24
	* 議論のポイントがどれも素晴らしい
	* 確認画面はまさに議論したい
	* プレビュー画面にどんな議論があるのか気になる
	* 207の誘惑とは、これ使いたくなるけど落ち着けよという意味と捉えよう
* slide 25
	* URLにid含まれるのよどうよ論。/users/:idだとユーザー数すぐバレるね。
	* セキュリティに関与するかどうかはそのリソースの性質による
* slide 26
	* あまり非同期に頼らない。とはいえ、JavaScriptをOFFにしても動く環境を担保しすぎるのも昨今現実的ではないのでは？
	* やっぱりバランス
	* twitterのリッチjsからの回帰は個人的には動作重くなったしもうちょい良い中間点があるのではないかと思う。

# [一周目のリソース設計](https://speakerdeck.com/u/moro/p/rails-resource-routing-design-bootstrap-ja)

ちょっと時間がなくて駆け足で振り返り。

* リソースをDBのテーブルと対応付け過ぎないことの大事さを1日に何度も聞けたのは良かった。


# [リソースモデリングパターンの提案](http://www.slideshare.net/tkawa1/resource-modeling-pattern)

* パターンで名付けることでコミュニケーションがしやすい
* パターンに当てはまらない場合に間違いを見つけやすい
* とはいえパターンに当てはまらないこともあるだろうからハマらないように
* サンプルを増やして書籍してはどうか
