# MongoDB のSharding 環境を作る
* ローカルとVMの2台構成で mongodb を sharding させてみる

# もくもくの記録
## 今日できたこと
* upstart で mongos、 mongo sharding config、 mongodb(shard) サーバーを立てる
* VM上にmongodb(shard) を立てる
* それらのサーバーで mongo sharding を作成

## 今日学んだこと
* mongodb の sharding には2つ以上の shard、1つ以上の mongos、1つか3つのconfig プロセスが必要

## 今日ハマったこと
* mongodb のデフォルトの config だと bind_ip が 127.0.0.1 になっていて外部から接続できない。 0.0.0.0 にする必要がある。
