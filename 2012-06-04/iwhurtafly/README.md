#【モクモクテーマ】モクモクすることを書く
* 引き続き、rails_tutorial_screencastsやります。
　前回の続き、lesson_06続きからやります。

## もくもくの記録
### 今日できたこと
* とにかくPaulが来ていてビックリして、最初の30分は何も手がつかず。。
* 落ち着いてからは、順調にlesson_06の半分まで勉強出来ました。

### 今日学んだこと
* gem annotate
* rails console --sandbox
* User.find(1)
　この場合、ID＝1が存在することが前提。
　存在しないと例外エラー。
　User.find_by_id(3)
　ならエラーにならないで、nilを返す。
　User.find_by_email("XXXX@XXX.com")
　User.first、User.last、User.all
* user.update_attributes(:name => "aa", :email => "bbb")
　これを実行可能にするには。。
　class User < ActiveRecord::Base
　　attr_accessible :name, :email
　end

　39minのRspec

### 今日ハマったこと
* 何か上手くgitにコミット出来ない。。

## 個人のKPT
###Keep よかったー
* 皆でモクモク
* DoorKeeperの裏側見れた
* 外国の方の参加

###Problem ダメだったー
* 仕事が詰まってると、Heroku Dev Centerから参加出来ない。
　（出来ないときは平日の朝とかにやります。）

###Try 改善・挑戦するー
* rails_tutorial_screencasts以外に何か出来ることないかを探りたい。


