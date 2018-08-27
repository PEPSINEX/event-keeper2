Event-keeper
========

## Description
[@now_cold](https://twitter.com/now_cold?lang=ja)が作成したイベント管理アプリ。DIVE INTO CODEでの卒業課題です。

スクールでイベントを開催する際、主催者の負担を出来るだけ減らすべく作成しました。

## Requirement
- Ruby 2.5.1
- Rails 5.1.0
- PostgreSQL 10.3
- Bootstrap 3

## Function
- イベント作成CRUD処理
- 開催予定イベント、過去イベントの一覧機能
- ログイン管理機能
- マイページ機能
- イベント参加、キャンセル機能
- 主催したイベントに動きがあった時、主催者への告知メール送信(選択式)
- イベントへの質問・コメント機能

## Usage
複数の利用者が必要なイベント投稿管理という性質上、ローカルでの使用は想定していません。以下のherokuにデプロイしたアプリを使用して頂ければ幸いです。
https://event-keeper2.herokuapp.com/

## Advice
Read meに書くべきではないかもしれませんが、卒業課題のアプリ制作のでの反省点と今後アプリを初めて作る人へのアドバイスを記述します。

結論を先に述べます。アプリ作成の際には機能を絞り込み、出来るだけ具体的に利用シーンを想定しましょう。また、時間の区切りを設けましょう。

例えば今回のイベント管理アプリですが、doorkeeperやconnpassを見本にしました。ただ、5W1Hに基いた利用シーンを想定していませんでした。そのため、案件定義もうまく出来ず、実装時に仕様が大きく変わりました。また、時間の区切りはつけるべきです。アプリを作成していくと、追加機能や見栄え良くしたいという気持ちがいくらでも湧いてきます。その全てを実現しようとするといくら時間があっても足りません。

なので、「スクールでイベントを開催する際、主催者の負担を出来るだけ減らす」という具体的な目的において、残り時間からどのようなアプリなら実装可能かを見積もってこのアプリを作成しました。イベントは企画したら他の人に見てもらえるように自動的にトップ画面に一覧表示され、その後の管理が楽になるように工夫しました。例えば、Webアプリは常に画面を開いている訳でないので、連絡の見逃しがあるかもしれない。それならば、イベントにアクションがあった時、必要に応じて通知をすればいいのでは？イベントに対して、複数人から同じような質問がくるかもしれない。それならば、掲示板形式にすれば重複は回避できる、非同期通信を用いればリアルタイムのコメントもやりやすいかなという思いで実装しました。

このように具体的な利用シーンを想定することで、設計や実装機能が見えてくるはずです。また、時間の区切りを設けることで、本当に必要な機能から実装していくはず。

拙い文ですが、以後初めてアプリを作成する人の力に少しでもなればいいなと思い書きました。以上です。

## Issue
これもRead meに書くべきではないかもですが、アプリ作成して今後勉強していきたいことを以下に記述します。

- Fat Controllerによるリファタリング
- テスト
- Rubyメソッドを用いたデータの抽出や加工。それのメソッド化
- validation。必要なものがあまり想定出来ていない。
- 案件定義。具体的な利用シーンを想定していなかったため、無駄が多い。
- タグ付けをgemに頼らず実装したいなぁ
- 読みやすいコード

とりあえず思いつくのはこのくらい。他に学んだ方がいいものとかあれば是非教えてください。

## ER Diagram
![event-keeper-er-diagram](https://github.com/KazuhiroObama/image/blob/master/images/%E5%8D%92%E6%A5%AD%E6%A1%88%E4%BB%B6ER%E5%9B%B3.png)

## Licence
[MIT](https://github.com/tcnksm/tool/blob/master/LICENCE)

## Author
[KazuhiroObama](https://github.com/KazuhiroObama)
