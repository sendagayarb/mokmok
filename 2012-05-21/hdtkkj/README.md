#【モクモクテーマ】モクモクすることを書く
* とりあえず空気に慣れる
* fluentのソース周りをみていく
* とりあえず実験用の環境を用意する

## もくもくの記録
### 今日できたこと
* supervisor.rbのメイン処理はよんだ
* td-agenetマルチプロセスでforward構成を組んだ

~~~
 access_log -> td-agemnt1 ---+
                             |
                             +-->
                                   td-agent2 -> apache_log
                             +-->
                             |
 error_log  -> td-agemnt2 ----
~~~

### 今日学んだこと
* rubyの正規表現が全然わかってないこと

### 今日ハマったこと
* とくになし

## 個人のKPT
###Keep よかったー
* いきなり参加できたこと

###Problem ダメだったー
* もう少し他の人とコミュニケーション取る

###Try 改善・挑戦するー
* fluent plugin 書く


