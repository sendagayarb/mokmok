# 自己紹介

http://ppworks.info を見て下さいお願いします。

#【モクモクテーマ】OAuthの相談会したい
iOSアプリ作っていて、web api使う際の認証どうしようと悩んでおります。OAuthの理解を深めそのあたりの指針を定めたいです。

* OAuthについて理解を深める
  * [認証と認可の違い](http://www.itmedia.co.jp/enterprise/articles/0804/22/news044.html)
  * [OAuth 2.0 Implicit Flowをユーザー認証に利用する際のリスクと対策方法について](http://d.hatena.ne.jp/ritou/20120206/1328484575)
  * [非技術者のためのOAuth認証(?)とOpenIDの違い入門](http://www.sakimura.org/2011/05/1087/)
* 認証・認可を意識したiosからのweb api利用について考える
* 相談事項
  * iOSからweb api利用する際のベストプラクティスは？
  * webからログイン出来るかどうかで違いはあるのか？
  * ユーザーの利便性とセキュリティのバランスを考えるには？
  * いわゆるOAuth使ってるログインってどうなの？



## もくもくの記録
---
スマートフォン ネイティブアプリからの OAuth 認証についての悩み

iOSアプリを開発していて、自分のweb apiにアクセスする際の認証・認可の方法を考えている。


# 解決策

## 1. web api 認証にOAuth providerのid, tokenを使いまわす

* token はしっかり守っていないといけないのでは？
* 本来、OAuth provider 認可に利用するtokenを自分のweb api認証・認可に使いまわすのはだめじゃない？

## 2. web api 認証にサイト独自tokenを利用する

### どのように行うか

1. web view を用いて、そこでOAuth providerへ認証・認可を求めるフローをはじめる
1. browser を裏で開く
1. 第三の案は以下

### facebookのパターン

1. facebook sdkで認証終了後、web apiにtokenを渡し、web apiからfacebook apiを /meを叩く。
1. その結果のfacebook uidと照らし合わしユーザーを確認。その後web apiでtokenを発行し、以後そのtokenでweb apiとやりとりする。

### 今日できたこと
* 議論出来た

### 今日学んだこと
* OAuthむずい

### 今日ハマったこと
* OAuth

## 個人のKPT
###Keep よかったー
* 時間意識してる
* 濃ゆい議論出来た

###Problem ダメだったー
* 毎回やることぶれてる

###Try 改善・挑戦するー
* 毎回違うことやって自分探し
* 結果出す


