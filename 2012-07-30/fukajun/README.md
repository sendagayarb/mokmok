# 今日のテーマ                                                                                                                                                                                                 
* RESTful勉強会の振り返り（復習）

# やったことの記録
「RailsにおけるRESTfulなURL設計勉強会」の資料を、みながら参加者の方々と復習をしました。
参加者の皆さんありがとうございました。
[togetter](http://togetter.com/li/347613)

[zusaar](http://www.zusaar.com/event/347006)

## twadaさんの発表資料 での復習
 [RESTful Web アプリの設計レビューの話](http://www.slideshare.net/t_wada/restful-web-design-review)
僕は前半1時間くらい遅れて参加だったので、終了後に@ppworksさんが親切に教えてくれたことを書きます。
   
  
 * slide4. WEB+DB pressの連載はWEBを支える技術が包括している
 * slide5. RubyKaigi06でのDHHのRESTについての発表まとめ
   ちょっと長いみたいだけど読むと勉強になる。
   [Discovering a world of Resources on Rails](http://web.archive.org/web/20081020154812/http://techno.hippy.jp/rorwiki/?RubyKaigi2006)
 
 * 動画でRESTについて学べるみたいgihyoさんのサイト
  [「現場で使えるREST」](http://gihyo.jp/dev/serial/01/rest)

 * slide8. RESTful URL設計 = 名前付けと考えがちだがそれは、ステップ3でようやく現れる。与えたい情報の設計から考える。

 * slide11. editはギリギリ名刺の意味もある。newは形容詞。形容詞はURLにつかうのぎりok後ろに名刺が省略していると考える

 * slide12. 階層構造が存在しないのに / で区切るのは奇妙なURL

 * slide13. URL設計で名前を探すときには「シソーラス」が便利、類語でしっくり来るものを探す。

 * slide15. テーブルと１：１になっているようなリソースはCRUDの重力に引かれてしまっている可能性がある。N+1問題にぶつかってしまう可能性が高い。

 * slide18. ステータスコードについて
  [StudyingHttp.net](http://www.studyinghttp.net/status_code)

 * slide19. 見せたくないプライベートリソースは存在することをバレてはいけいないのでステータスコード404を返す。参加者は意外にやってる人多かった。

 * slide20. ユーザーがURLを組み立てないといけないのはよくない。関連してその後に使うようなリソースのURLもレスポンスに含めて返してあげる必要がある。JSONみたいに画面ではないけどデータとして返す場合でも同じで、普通だったら画面に存在するようなリンクが必要。

## moroさんの資料での復習
 [一周目のリソース設計](https://speakerdeck.com/u/moro/p/rails-resource-routing-design-bootstrap-ja)

* なによりもURLを定義することが目的ではなく、「アプリケーションが扱う情報を整理するのが先」ということが大切

* Railsで作るのだったらやっぱりRESTの上に乗っかったほうが、いろんな手間を解消できる。url_forとかform_forとか

* テーブルに1:1で対応するような画面は、マスター管理になってる「RailsAdmin」でよい

* resourcesのアクションは、選んで使おう

* 見えにくいリソースをさがすことですっきりとURL設計できる。関連テーブルとか
 
## t_kawaさんの資料 での復習

 [リソースモデリングパターンの提案](http://www.slideshare.net/tkawa1/resource-modeling-pattern)

 * 覚えておくと自分の設計がRESTの上に乗れているかわかるので便利

 * もう少し例など増やして本だしてほしい
 
