#【モクモクテーマ】モクモクすることを書く
* paper trailの使い方勉強します。

# もくもくの記録
## 今日できたこと
* paper trailsの各メソッドを試すためのrspecとfactory girls環境

## 今日学んだこと
* コレ学びました
paper trailで使えるようになるメソッド

https://github.com/airblade/paper_trail

* バージョン管理をするモデルに定義
```
has_paper_trail
```

* オブジェクトのバージョン全部取ってくる
```
.versions
```

* 次のバージョン
```
    .next_version
```

* 前のバージョン
```
    .previous_version
```

## 今日ハマったこと
* rspecを動かすための環境づくり
   enviroments/test.rb
に必要へ変数を書き忘れてた。
