#【ポジションペーパ】
かなり昔のRails勉強会の際の情報ですが流用→ http://goo.gl/qS13y

#【モクモクテーマ】OAuthの認証まわりの勉強
* tatekoto.herokuapp.com にtwitterやfacebookからOAuthでサイインできるようにしたい

# もくもくの記録
## 今日できたこと
* OAuthの基本 WEB+DB PRESS #63 作って学ぶOAuth認証 にシーケンス図があって
OAuth1.0とOAuth2.0の違いがよくわかる。

## 今日学んだこと
### 貯めていたブックマークなどおさらい

* APIアクセス権を委譲するプロトコル、OAuthを知る
http://www.atmarkit.co.jp/fsecurity/special/106oauth/oauth01.html

* 「OAuth」とは　日本のユーザー襲った“Twitterスパム”の正体 (1/2)
http://www.itmedia.co.jp/news/articles/0908/10/news015.html

### OAuth1.0から OAuth2.0 にバージョンが上がって簡略化された反面危険が存在することの注意は必要！
* 単なる OAuth 2.0 を認証に使うと、車が通れるほどのどでかいセキュリティー・ホールができる
http://www.sakimura.org/2012/02/1487/

* OAuth 2.0って知ってますかぁ？
http://kura-lab.hatenablog.com/entry/2012/02/29/013210

### Railsでdeviseと一緒に使うomniauth

* Rails + Devise + omniauthでTwitterの認証
http://d.hatena.ne.jp/tokyoster0907/20110715/1310717570

* Rails で Devise と OmniAuth を連携させる
http://blog.twiwt.org/e/14b25f

### omnioath記事
* Deviseとomniauthを使ってTwitterのOAuth認証
http://d.hatena.ne.jp/hellon999/20110818/1313683089

* OmniAuthでTwitter認証を作りインテグレーションテストも書く
http://goo.gl/g9lcR

### Ruby での OAuth
* RubyonRailsでOAuth経由でTwitterのタイムラインを取得する
http://tt-house.com/2010/06/rubyonrails-oauth-twitter.html


* OAuthのアクセストークンを、ブラウザなしで、Twitterのユーザ名およびパスワードのみを用いて取得する(通称：xAuth)ためのRubyのコード
http://blog.livedoor.jp/maraigue/archives/1109122.html

* rubytter と oauth を使う
http://randd.kwappa.net/2009/10/31/136

### Secret Keyなどの管理
* HerokuでEnv使う
http://hakolog.heroku.com/r7kamura/heroku%E3%81%A7env%E4%BD%BF%E3%81%86

リポジトリにgithubなど使う場合には、Secret Key等は公開されるファイルに保存せずに
環境変数経由でセットする。

## 今日ハマったこと
* README.mdをpushの際
自分のファイルを作成してpushする時に、なにげに強制pushしてしまい
リポジトリを退行させてしまいました。以後気をつけますorz

@fukajunさん 復旧にお世話になりました。


## 個人のKPT
###Keep よかったー
* PCスタンドにノートPCとiPadを乗せてAirDisplayで画面拡張し、別途 HHK で入力するというスタイルをやってみた。

###Problem ダメだったー
* Git push 注意

###Try 改善・挑戦するー
* Git力を高める！


