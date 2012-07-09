#【モクモクテーマ】モクモクすることを書く
* heroku dev center翻訳作業
 * https://github.com/herokaijp/devcenter/wiki/git

# もくもくの記録
## 今日できたこと
* fukajunさん による @suginoyさんの「Rails で十分に活用されていなくてもったいない ActiveRecord::Relation のメソッド TOP 10」訳をワイワイする。
http://d.hatena.ne.jp/suginoy/20120605/p3

下記のこれは使ってみたい。

###3位 scoping

scope メソッドを特定の Relation として使える。Rails のドキュメントにある次の例を検討してみよう。

```
Comment.where(:post_id => 1).scoping do
  Comment.first # SELECT * FROM comments WHERE post_id = 1
end
```

###2位 pluck
特定のレコードのカラムで配列にしたいことがないだろうか？私はこういうにを本当にたくさん見てきた。

```
published_book_titles = Book.published.select(:title).map(&:title)
```

代わりに pluck を使おう。

```
published_book_titles = Book.published.pluck(:title)
```

###1位 merge
これを使うと、結合( JOIN )ができて、結合されたモデルに対して名前付きスコープでフィルタができる。


```
class Account < ActiveRecord::Base
  # ...

  # Returns all the accounts that have unread messages.
  def self.with_unread_messages
    joins(:messages).merge( Message.unread )
  end
end
```
## Rmenu

Rmenuの下地さんからメールが入っていたので、返事のメール書き(^_^;;

RmenuはRubyで書かれた汎用機バッチ処理まわりの処理をJavaやPHPで書かれたものを移植したもので
非同期処理の管理にRindaが使われています。
http://www.onas.asia/rubyfuremuwaku
http://125.206.227.76/simoji/Rmenu/docs/main/


### 今日ハマったこと
* 日本語訳に時間がとれず(;_;)

## 個人のKPT
###Keep よかったー
* おもしろそうな個人のblogをみんなでワイワイやるのは楽しい。

###Problem ダメだったー
* 和訳

###Try 改善・挑戦するー
* ポジションペーパーをちゃんと作っておく。

