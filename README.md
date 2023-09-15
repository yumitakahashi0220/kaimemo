# kaimemo

## ■サービス概要
日常的に利用しているモノの買い忘れを防ぐサービスです。

## ■ このサービスへの思い・作りたい理由
自分自身、日常生活で調味料が切れた、洗剤やトイレットペーパーがなくなって困ることがよくあります。
対策としてメモアプリで管理していましたが、他にもほしい機能がたくさんあるので自分で作りたいと思いました。
また、一緒に住んでいる人にLINEで頼んでも会話で流れてしまい忘れられてしまうこともある＆商品を間違って買ってきてしまうことがあるため
買い物を頼むこと1つとってもとても労力を使います。
仕事や子育てが忙しいときは丁寧に買い物の依頼をすることも大変なので、このサービスを使ってもらうことで、定常タスクを一括管理することによって無駄なやりとりを減らして、自分にも相手にもストレスフリーな日常生活が送ってもらえるようにしたいです！

### 欲しいと思った機能
・なくなりそうな時期に事前にリマインドがくる（1週間後にしょうゆなくなりそうですよ！など）
・前回買った価格を記載して比較ができる（前回より安かったらお得だからストックのため買うという判断もあり）
・ストックも記録しておける（棚にしまい込んで、ないと思って重複して買ってしまうのを防ぐ）
・一緒に住んでいる人に買い物メモを共有して買ってきてもらいたい（リマインド機能があれば連絡漏れもなくなる）
・もし誰かに買ってきてもらうときに買って欲しい商品を明確に伝えたいので、Amazonなどで商品検索できて画像をつけれるようにしたい（例：オムツならなんでもいいわけではなく、「パンパース おむつ テープ M（6～11kg）1パック（64枚入）はじめての肌へのいちばん」じゃないとだめなど）
・ネットでの価格も確認できて、お店の価格と比較できる（ネットの方が安ければネット買うなどの選択肢を増やす）

## ■ ユーザー層について
共同生活をしている人or一人暮らしで日用品を買い忘れることが多い人
→頭で記憶するだけだと忘れてしまうのと、自分自身が共同生活をしていて、生活用品の備品がなくなったことを共有してほしいと思ったためです

## ■サービスの利用イメージ
* 日常生活で日々利用している消耗品がなくなったら買い物メモとして登録
* 買い物メモを共有することで一緒に住んでいる人が代わり買うことができ、買ったことの通知も自動でされる
* 買い物メモにリマインド機能をつけられるので無くなる前にリマインド通知で検知することができる
* ネット価格も確認できるのでスーパーで値段を確認して比較してネット、スーパーどちらで買うか決められる


## ■ ユーザーの獲得について
Twitterでのシェア

## ■ サービスの差別化ポイント・推しポイント
### 推しポイント1：値段の比較ができる
メモやLINEでのやりとりだけだと値段の比較はできませんが、このサービスを利用すればネットの価格も確認できるのでより安いところで購入ができるようになる
類似サービスとしてAmazonの「定期おトク便」があるが、定期購入のため金額の比較はできない

### 推しポイント2：買ってきてほしい商品の詳細を伝える工数がなくなる
LINEなどのやり取りで明確な商品を伝えるとなると、商品名と商品の画像を検索してスクショをとり、そのスクショを添付して「この商品をかってきてほしい」と伝える必要がありますが、1度商品を登録すれば、それ以降その工数を0にすることができます。
もし使っていたオムツのサイズが変更になったとしても、商品を変更することで明確に伝達することができます。

### 推しポイント3：リマインド通知
なくなったら困るトイレットペーパーや洗剤などの商品もリマインド機能があることで買い忘れを防ぐことができます。毎回買うのが大変だから買いだめしようと思っても家のスペースは無限じゃない。リマインド機能を利用してなくなりそうになったら買う。そうすることによって家のスペースもより活用できる


## ■ 機能候補
### MVP
* 会員登録
* ログイン
* 買い物メモ一覧
* 買い物メモの登録
* 買い物メモのリマインド設定
* 買い物メモのシェア機能
* 買い物メモのLINE通知

### その後の機能
* 買い物メモの画像登録（Amazon,楽天などから画像を引用できるようにする）
* 買い物メモの共有
* 買い物メモの価格記録
* 登録した買い物メモの検索機能

## ■ 機能の実装方針予定
### バックエンド
* Ruby: 3.0系
* Rails: 7.0系
* データベース: PostgreSQL (version: 13.4)
### フロントエンド
* JavaScript: ES6
* フレームワーク: Stimulus
### インフラストラクチャ
* ホスティング: Heroku
* 画像ストレージ: Amazon S3
### API & サードパーティ
* 商品検索・画像取得: Amazon Product Advertising API
* LINE通知: LINE Messaging API
### その他ライブラリ
* オートコンプリート: Stimulus Autocomplete (for Rails 7)
* 通知: WebSocket通信・ActionCable (Rails標準)
* LINE通知: LINE Messaging API SDK for Ruby


### 画面遷移図
Figma：https://www.figma.com/file/7rDmjfvV2IsPv6pTgUknl5/kaimemo?type=whiteboard&node-id=0%3A1&t=LFtZ2ACzjBsCfjPT-1